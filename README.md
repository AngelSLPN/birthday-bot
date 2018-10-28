birthday-bot
===

NodeJS based bot to inform chat (channel) members about someone's birthday.


# Tech Stack

## Microsoft Azure Bot Service v4
- https://docs.microsoft.com/en-us/azure/bot-service/?view=azure-bot-service-4.0

### Using JavaScript/NodeJS approach
- https://docs.microsoft.com/en-us/azure/bot-service/javascript/bot-builder-javascript-quickstart?view=azure-bot-service-4.0

### Channels
- https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-skype?view=azure-bot-service-4.0
- https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-telegram?view=azure-bot-service-4.0
- https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-facebook?view=azure-bot-service-4.0

## Node CSV ?
- https://github.com/adaltas/node-csv

## JS XLX ?
- https://github.com/SheetJS/js-xlsx

## MongoDB ?

# Production URLs
- https://telegram.me/StoLatBot
- https://join.skype.com/bot/948e14b4-e88a-42b0-9cbc-95c02ef6cccb


# LUIS (Microsoft) vs. NLP (Facebook) vs. Cortna (Microsoft)

## LUIS
- https://docs.microsoft.com/en-us/azure/cognitive-services/luis/what-is-luis
> Once the LUIS app is published, a client application sends utterances (text) to the LUIS natural language processing endpoint API and receives the results as JSON responses.

- https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-v4-luis?view=azure-bot-service-4.0&tabs=cs
- `luisgen` requires/depends `dotnet`
- https://docs.microsoft.com/en-us/dotnet/core/macos-prerequisites?tabs=netcore2x
- https://www.luis.ai/applications - My LUIS Apps main page
- https://aka.ms/luis-endpoint-apis

## Cortana
- https://docs.microsoft.com/en-us/cortana/skills/overview
- https://my.knowledge.store/workspace - Manage Cortana Skills?

## NLP


# From Yeoman "botbuilder" generator

https://docs.microsoft.com/en-us/azure/bot-service/javascript/bot-builder-javascript-quickstart?view=azure-bot-service-4.0
Generated by `generator-botbuilder`


# To run the bot
- Install modules and start the bot
    ```bash
    npm i & npm start
    ```
    Alternatively you can also use nodemon via
    ```bash
    npm i & npm run watch
    ```

# Testing the bot using Bot Framework Emulator
[Microsoft Bot Framework Emulator][2] is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the Bot Framework emulator from [here][3]

## Connect to bot using Bot Framework Emulator **V4**
- Launch Bot Framework Emulator
- File -> Open Bot Configuration
- Select `birthday.bot` file

# Bot state
A key to good bot design is to track the context of a conversation, so that your bot remembers things like the answers to previous questions. Depending on what your bot is used for, you may even need to keep track of conversation state or store user related information for longer than the lifetime of one given conversation.

In this example, the bot's state is used to track number of messages.

 A bot's state is information it remembers in order to respond appropriately to incoming messages. The Bot Builder SDK provides classes for [storing and retrieving state data][4] as an object associated with a user or a conversation.

    - Conversation properties help your bot keep track of the current conversation the bot is having with the user. If your bot needs to complete a sequence of steps or switch between conversation topics, you can use conversation properties to manage steps in a sequence or track the current topic. Since conversation properties reflect the state of the current conversation, you typically clear them at the end of a session, when the bot receives an end of conversation activity.

    - User properties can be used for many purposes, such as determining where the user's prior conversation left off or simply greeting a returning user by name. If you store a user's preferences, you can use that information to customize the conversation the next time you chat. For example, you might alert the user to a news article about a topic that interests her, or alert a user when an appointment becomes available. You should clear them if the bot receives a delete user data activity.

# Deploy this bot to Azure
You can use the [MSBot][5] Bot Builder CLI tool to clone and configure the services this sample depends on.

To install all Bot Builder tools -

Ensure you have [Node.js](https://nodejs.org/) version 8.5 or higher

```bash
npm i -g msbot chatdown ludown qnamaker luis-apis botdispatch luisgen
```

To clone this bot, run
```
msbot clone services -f deploymentScripts/msbotClone -n myChatBot -l <Azure-location> --subscriptionId <Azure-subscription-id>
```

# Further reading
- [Azure Bot Service Introduction][6]
- [Bot State][7]
- [Write directly to storage][8]
- [Managing conversation and user state][9]


[1]: https://www.npmjs.com/package/restify
[2]: https://github.com/microsoft/botframework-emulator
[3]: https://aka.ms/botframework-emulator
[4]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-v4-state?view=azure-bot-service-4.0&tabs=js
[5]: https://github.com/microsoft/botbuilder-tools
[6]: https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0
[7]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-storage-concept?view=azure-bot-service-4.0
[8]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-v4-storage?view=azure-bot-service-4.0&tabs=jsechoproperty%2Ccsetagoverwrite%2Ccsetag
[9]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-v4-state?view=azure-bot-service-4.0&tabs=js
[10]: https://dev.botframework.com
 
