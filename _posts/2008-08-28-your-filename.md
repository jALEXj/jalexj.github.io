---
published: true
layout: post
title: Windows / MsDOS - Suppression des fichiers temporaires de tous les utilisateur
---
Très utile notamment sur un serveur Terminal Serveur

Clean_Users_Profiles.bat
```
%SYSTEMDRIVE%
cd "\Documents and Settings"
for /D %%g IN ("*") DO del /F /S /Q "\Documents and Settings\%%g\Local Settings\Temporary Internet Files\*"
for /D %%g IN ("*") DO del /F /S /Q "\Documents and Settings\%%g\Local Settings\Temp\*"
pause
```
