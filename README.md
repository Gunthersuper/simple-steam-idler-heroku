# simple-steam-idler-heroku
24/7 Steam ingame time idler with Heroku (simple version)

**Requirements:**

1. Install Git: https://git-scm.com/downloads
2. Install Heroku CLI: https://devcenter.heroku.com/articles/heroku-cli
3. Register at https://heroku.com
4. Connect your account to the SDA: https://github.com/Jessecar96/SteamDesktopAuthenticator/releases/tag/1.0.10

**Setting up:**
1. Open PowerShell (or teminal) in any folder you want. Enter:
    - `git config --global user.email YOUR EMAIL `
    - `git clone https://github.com/Gunthersuper/steam-idle-bot`
2. A new folder `simple-steam-idler-heroku` will appeared in this directory. Go to this folder.
3. Open `index.js`. Fill the needed information: 
   ```
   var username = '';
   var password = '';
   var shared_secret = '';

   var games = [730, 440, 570];  // Enter here AppIDs of the needed games
   var status = 1;  // 1 - online, 7 - invisible
   ```
4. Deploy the bot:
    - `git add .`
    - `git commit -m 'commit'`
    - `heroku login`
Then login in your browser
    - `heroku create`
    - `git push heroku main`
    - `heroku ps:scale web=0`
    - `heroku ps:scale bot=1`
    
To restart the bot go to Heroku (https://dashboard.heroku.com/apps), select your app, `More`, `Restart al dynos`
