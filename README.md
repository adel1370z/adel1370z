import telebot

# Replace 'YOUR_BOT_TOKEN' with your actual bot token
bot_token = 6421101585:AAEIxRqFiaO1wcf7MXbGSG_U9I1T0prKDno

telebot.TeleBot (bot_token
bot = telebot.TeleBot(bot_token)

# Handle /start command
@bot.message_handler(commands=['start'])
def start(message):
    bot.reply_to(message, "Hello! I am your Tabchi bot.")

# Handle echo messages @bot.message_handler(func=
@bot.message_handler(func=lambda message: True)
def echo(message):
    bot.reply_to(message, message.text)

# Start the bot
bot.polling()
