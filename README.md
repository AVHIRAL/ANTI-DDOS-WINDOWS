# ANTI-DDOS-WINDOWS 10 / 11

 `DDoS_Monitor.ps1` : Vous pouvez le placer dans un répertoire de votre choix, comme votre dossier "Documents" ou "Desktop".

Pour exécuter automatiquement le script au démarrage de Windows 11, vous pouvez utiliser le Planificateur de tâches. 

Voici les étapes pour créer une tâche planifiée qui exécute le script au démarrage:

1. Appuyez sur `Win` + `R`, tapez `taskschd.msc` et appuyez sur `Enter` pour ouvrir le Planificateur de tâches.
2. Dans le volet gauche, cliquez avec le bouton droit sur "Bibliothèque du Planificateur de tâches" et choisissez "Nouveau dossier". Nommez le dossier "CustomTasks" ou quelque chose de similaire.
3. Sélectionnez le nouveau dossier, puis cliquez avec le bouton droit dans le volet central et choisissez "Créer une tâche".
4. Dans l'onglet "Général", donnez un nom à la tâche, par exemple "Run DDoS Monitor Script". Cochez la case "Exécuter avec les autorisations maximales" et sélectionnez "Windows 11" dans le menu déroulant "Configurer pour".
5. Allez à l'onglet "Déclencheurs" et cliquez sur "Nouveau...". Dans les paramètres de déclenchement, choisissez "Au démarrage" dans le menu déroulant "Commencer la tâche" et cliquez sur "OK".
6. Allez à l'onglet "Actions" et cliquez sur "Nouveau...". Dans les paramètres d'action, choisissez "Démarrer un programme" dans le menu déroulant "Action". Pour "Programme/script", tapez `powershell.exe`. Dans "Ajouter des arguments (facultatif)", tapez `-ExecutionPolicy Bypass -File "C:\path\to\your\DDoS_Monitor.ps1"`, en remplaçant `C:\path\to\your` par le chemin d'accès réel du script. Cliquez sur "OK".
7. Cliquez sur "OK" pour fermer la fenêtre "Créer une tâche".

Le script PowerShell sera exécuté automatiquement à chaque démarrage de Windows 11. 
