Creating Github Repo with the help of Github MCP Server and VSCode.

1. Adding mcp server in Preferences: Open User Settings (JSON) in vscode

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

2. creating Personal Access token in github for authentication with limited access needed for operation.

  - Classic tokens under developer setting from Github Setting

3. Start the docker in local 

4. Use Github copilot extension in vscode as an mcp client to do the operation.

  - 
    create_repository
    name: MCP-Server

    The repository named MCP-Server has been successfully created in your GitHub account. You can access it at the following URL: MCP-Server Repository. Let me know if you need help with anything else, such as pushing code to this repository or setting it up further!