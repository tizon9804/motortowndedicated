# 🚀 SteamCMD in Docker optimized for AWS
This Docker container installs SteamCMD and downloads the game specified via environment variables. It is optimized for use with Unraid but should also work in other environments with Docker.

> 🧩 This container is designed to work in AWS ec2 t3.xlarge.

## 🛠️ Example Env params for **Motor Town: Behind The Wheel** 
| Name | Value | Example |
| --- | --- | --- |
| GAME_ID | the ID of the game of steam in this case the tool of motor town server dedicated. | 2223650 |
| GAME_ID_ARGS | Additional args to pass the steamcmd client (i.e. for betas) | -beta test -betapassword motortowndedi |
| GAME_PARAMS | Values to start the server the name of the map | Jeju_World?listen? -server -log -useperfthreads |
| STEAM_USERNAME | This game need an account with the game, leave blank for anonymous login. | steamuser |
| STEAM_PASSWORD | This game need an account with the game, leave blank for anonymous login. | steampassword |
| STEAMCMD_DIR | Folder for SteamCMD | /serverdata/steamcmd |
| SERVER_DIR | Folder for gamefile | /serverdata/serverfiles |
| UID | User Identifier | 99 |
| GID | Group Identifier | 100 |
| VALIDATE | Validates the game data | validate +exit |

> 💡 **Note:** The environment variables shown above should be set in a `.env` file.  
> You can start by copying the provided `.env.example` to `.env` and then customizing the values as needed.

## 📦 Usage Example
1. Clone the repository:
    ```bash
    cd /mnt/user/appdata/<folderWithDocker>
    git clone <this repo>
    cd motortowndedicated
    ```

2. Copy and configure the environment variables:
    ```bash
    cp .env.example .env
    ```

3. Run the container from the terminal:
    ```bash
    docker compose up -d --build 
    ```

## 🔎 Notes


## 🙏 Credits
This Docker is forked from sazquatch17, mattieserver, ich777, nodiaque, thank you for this wonderfull Docker.
