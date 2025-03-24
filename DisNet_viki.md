**DisNet**

DisNet is a modified version of the discord.py library designed for creating online games or applications. This library does not require a host or any other complicated setup, making it easy to use for simple bot development.

**Installation**

To install DisNet, run the following command:

pip install DisNet

**Basic Example**

Here’s an example of how to use DisNet to create a simple Discord bot:

import DisNet.DisNet as ds
# You can set the permissions yourself or use the built-in ones.
bot = ds.bot
# Bot token
TOKEN = 'YOUR_DISCORD_BOT_TOKEN'

@bot.event
async def on_ready():
    await ds.messagesManager.setup()
    await ds.sendData.sendData(1351879148343263352, 'Hello, there')

bot.run(TOKEN)

**Methods**
sendData.sendData(chanell, message)

Sends a message to the specified channel.

    chanell: Channel ID.
    message: The message to send.

getData.getData(chanell, packedDataLength=2)

Fetches messages from the specified channel.

    chanell: Channel ID.
    packedDataLength: Number of messages to fetch.

messagesManager.clearMessages(chanell, messagesLength=1)

Clears messages in the specified channel.

    chanell: Channel ID.
    messagesLength: Number of messages to delete.

messagesManager.aditMessages(chanell, messagesLength=None, messagesNum=None, newMessage=None)

Edits a message in the specified channel.

    chanell: Channel ID.
    messagesLength: Number of messages to edit.
    messagesNum: The number of the message to edit.
    newMessage: The new message content.
