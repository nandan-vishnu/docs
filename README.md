# Work Samples
## Teams AI library quick start guide - Python sample


Get started with Teams AI library using the sample, which is designed to help you through the process of creating apps that can control lights, such as turning them on and off using Teams AI library. The bot uses the gpt-3.5-turbo model to chat with Microsoft Teams users and respond in a polite and respectful manner, staying within the scope of the conversation.

### Prerequisites
To get started, ensure that you have the following tools:

Visual Studio Code
Teams Toolkit
Git
Node.js
Microsoft Teams
OpenAI or Azure OpenAI
Microsoft Edge (recommended) or Google Chrome
Microsoft 365 developer account

If you've already run the samples before or encountered a runtime error, follow these steps to start fresh:
* Check all the .env and env/.env.*.* files in the sample and delete any automatically populated values to ensure that Teams Toolkit generates new resources for you.
* If you don’t want Teams Toolkit to generate the app ID and password, update the BOT_ID and BOT_PASSWORD in the .env file with your own values.
* Remove values or leave the values blank for SECRET_BOT_PASSWORD and TEAMS_APP_UPDATE_TIME in the .env file to avoid conflicts.

Teams Toolkit automatically provisions BOT_ID and BOT_PASSWORD resources. If you want to use your own resources, you need to manually add them to the .env file. Teams Toolkit doesn't auto-generate the following resources:

* An Azure OpenAI or OpenAI key
* A database or similar storage options

### Build and run the sample app
Get started with Teams AI library using the sample. It enables your computer’s localhost to quickly execute a Teams AI library-based sample.

1. Go to the sample.

2. Run the following command to clone the repository:

    Windows Command Prompt
    
    Copy
    git clone https://github.com/*****/****
3. Go to Visual Studio Code.

4. Select File > Open Folder.

5. Go to the location where you cloned samples repo and select the sample folder.

6. Select Select Folder.

7. Select View > Terminal. A terminal window opens.

8. In the terminal window, run the following command to go to the js folder:

    Copy
    cd .\js\
    Run the following command to install dependencies:
    
    terminal
    
    Copy
    yarn install


    Run the following command to build dependencies:
    
    terminal
    
    Copy
    yarn build

9. After the dependencies are installed, select File > Open Folder.

10. Go to samples folder and select Select Folder. All the files for the sample are listed under the EXPLORER section in Visual Studio Code.

11. Update the following steps based on the AI services you select.

    OpenAI key
    Azure OpenAI
    Go to the env folder and update the following code in ./env/.env.local.user file:
    
    text
    
    Copy
     SECRET_OPENAI_KEY=<your OpenAI key>
    Go to the infra folder and ensure that the following lines in the azure.bicep file are commented out:
    
    Bicep
    
    Copy
        // {
        //   name: 'AZURE_OPENAI_KEY'
        //   value: azureOpenAIKey
        // }
        // {
        //   name: 'AZURE_OPENAI_ENDPOINT'
        //   value: azureOpenAIEndpoint
        // }
12. From the left pane, select Teams Toolkit.

13. Under ACCOUNTS, sign-in to the following:

    Microsoft 365 account
    Azure account
    To debug your app, select the F5 key.

14. A browser tab opens a Teams web client requesting to add the bot to your tenant.

15. Select Add.

    A chat window opens.

16. In the message compose area, send a message to invoke the bot.



