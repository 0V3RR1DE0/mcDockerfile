```
version: '3.7'

services:
  minecraft_server:
    image: itzg/minecraft-server
    environment:
      EULA: "TRUE" # You must accept the Minecraft EULA
      TYPE: "FABRIC" # Specify the server type as Fabric
      MOTD: "A Fabric Minecraft Server" # Message of the Day
      DIFFICULTY: "hard" # Set the difficulty level
      WHITELIST: |
        user1
        user2
        user3 # Whitelist of players
      OPS: |
        admin1
        admin2 # List of ops/administrator players
      MAX_PLAYERS: 20 # Max number of players
      VIEW_DISTANCE: 25 # Server-side viewing distance
      ENABLE_RCON: "true" # Enable RCON
      RCON_PASSWORD: "your_rcon_password" # Set RCON password
      ENABLE_QUERY: "true" # Enable query protocol
      # MAX_WORLD_SIZE: 10000 # Max world size
      ALLOW_NETHER: "true" # Allow Nether
      ENABLE_COMMAND_BLOCK: "true" # Enable command blocks
      FORCE_GAMEMODE: "false" # Force default gamemode
      GENERATE_STRUCTURES: "true" # Generate structures
      HARDCORE: "false" # Hardcore mode
      SNOOPER_ENABLED: "false" # Disable snoop
      SPAWN_ANIMALS: "true" # Spawn animals
      SPAWN_MONSTERS: "true" # Spawn monsters
      SPAWN_NPCS: "true" # Spawn NPCs
      RESOURCE_PACK: "" # Custom resource pack link
      RESOURCE_PACK_SHA1: "" # Resource pack SHA1 checksum
      LEVEL: "world" # Level/world save name
      ONLINE_MODE: "FALSE" # Enable online mode
      ALLOW_FLIGHT: "TRUE" # Disable flight
      FABRIC_LAUNCHER_VERSION: "0.97.0" # Specify Fabric launcher version
      FABRIC_LOADER_VERSION: "0.15.10" # Specify Fabric loader version
    ports:
      - "25565:25565" # Minecraft default port
    volumes:
      - ./data:/data

volumes:
  - ./data:/data
```

```
wget https://cdn.modrinth.com/data/qmeKRMsC/versions/pX46DHKC/no-trial-chambers-1.2.jar

```
