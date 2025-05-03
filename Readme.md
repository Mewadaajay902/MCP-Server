# Creating Github Repo with the help of Github MCP Server and VSCode.

> **_NOTE:_**  This repository was created with the help MCP Server

## steps
### 1. Adding mcp server in Preferences: Open User Settings (JSON) in vscode

```json
    {
     "mcp": {
       "inputs": [
         {
           "type": "promptString",
           "id": "github_token",
           "description": "GitHub Personal Access Token",
           "password": true
         }
       ],
       "servers": {
         "github": {
           "command": "docker",
           "args": [
             "run",
             "-i",
             "--rm",
             "-e",
             "GITHUB_PERSONAL_ACCESS_TOKEN",
             "ghcr.io/github/github-mcp-server"
           ],
           "env": {
             "GITHUB_PERSONAL_ACCESS_TOKEN": "${input:github_token}"
           }
         }
       }
     }
   }
```

### 2. creating Personal Access token in github for authentication with limited access needed for operation.

         Classic tokens under developer setting from Github Setting

### 3. Start the docker in local environment

### 4. Use Github copilot extension in vscode as an mcp client to do the operation.

#### example:

```plaintext
    create_repository
    name: MCP-Server

    The repository named MCP-Server has been successfully created in your GitHub account. You can access it at the following URL: MCP-Server Repository. Let me know if you need help with anything else, such as pushing code to this repository or setting it up further!
```





### Adding some Sreenshot from the practical


<img width="1046" alt="Screenshot 2025-05-03 at 1 52 31 PM" src="https://github.com/user-attachments/assets/dbe9b876-2d1b-4fa8-a95c-4076e515d022" />
<img width="1046" alt="Screenshot 2025-05-03 at 1 51 58 PM" src="https://github.com/user-attachments/assets/74073c80-e938-4525-8193-d35bbb159496" />
<img width="592" alt="Screenshot 2025-05-03 at 2 07 34 PM" src="https://github.com/user-attachments/assets/9a077abb-5ec0-48e0-b46b-0ea58e8d624e" />

<img width="806" alt="Screenshot 2025-05-03 at 2 52 08 PM" src="https://github.com/user-attachments/assets/8450f794-c204-42fb-a4d4-f809514ea6d9" />
<img width="503" alt="Screenshot 2025-05-03 at 4 32 31 PM" src="https://github.com/user-attachments/assets/d9b142b7-7c0d-454f-ba0c-4b31ed86640c" />
<img width="1467" alt="Screenshot 2025-05-03 at 4 34 11 PM" src="https://github.com/user-attachments/assets/be8e5f39-0dbc-45c6-9622-3fa6e20d8f85" />
<img width="1467" alt="Screenshot 2025-05-03 at 6 06 36 PM" src="https://github.com/user-attachments/assets/48319ebe-2134-4cd8-9f41-6c140bd51b30" />

    
