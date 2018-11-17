---
published: false
layout: post
---
## Un bloc note dans une page PHP

```
<?
// Update post-it.txt
if ($_REQUEST[postit]){
$fp = fopen("post-it.txt","r+");
fwrite($fp,$_REQUEST[postit_text]);
ftruncate($fp,strlen($_REQUEST[postit_text]));
fclose($fp);
}

// Recupération du post-it.txt
$fp = fopen("post-it.txt","r");
$postit_text = fread($fp,filesize("post-it.txt"));
$postit_text = stripslashes($postit_text);
fclose($fp);
?>

<form name="form1" method="post" action="">
Notes:<br>
<textarea name='postit_text' style='background-color:#F9FFA2;scrollbar-base-color:#F9FFA2;scrollbar-arrow-color:black;border:1px solid #CCC;font-family:verdana;font-size:10px' rows='8' cols='42'>
<?php echo $postit_text; ?>
</textarea>
<br>
<input name="postit" type='submit' style='background-color:#F9FFA2;border:1px solid #999;font-family:verdana;font-size:10px' value='post-it!' />
</form>
```
