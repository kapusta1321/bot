import telebot
from telebot import types
from telebot.types import ReplyKeyboardRemove
bot=telebot.TeleBot('6394916866:AAHOs9UrY2vxF9af4Z9vgj6-DZc6RibXWPk')
@bot.message_handler(commands=["start"])
def start(m, res=False):
    markup=types.ReplyKeyboardMarkup(resize_keyboard=True)
    bot.send_message(m.chat.id, 'привет! с радостью поможем вам заказать одежду и обувь, а также оформить подписку на интерсующий сервис', reply_markup=markup)
    item1=types.KeyboardButton("заказать одежду или обувь")
    item2=types.KeyboardButton("оформить подписку")
    item3=types.KeyboardButton("оставить отзыв")
    markup.add(item1)
    markup.add(item2)
    markup.add(item3)
    bot.send_message(m.chat.id, 'подскажите, пожалуйста, что вы хотели бы сделать через наш бот.', reply_markup=markup)
@bot.message_handler(content_types=["text"])
def message_reply(message):
    if message.text == "заказать одежду или обувь":
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
        bot.send_message(message.chat.id,'наш бот сейчас в стадии разработки, из-за чего, к сожалению, пока не может принимать заказы, поэтому просим оставить вашу заявку на новый предмет гардероба через [google форму](https://docs.google.com/forms/d/e/1FAIpQLScYzXV7ICz4HYiMh4iimJwH4faY192pq1GE37vARUqI3cCq5w/viewform?usp=sf_link)', parse_mode='Markdown', reply_markup=telebot.types.ReplyKeyboardRemove())
    elif message.text == "оформить подписку":
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
        bot.send_message(message.chat.id, 'наш бот сейчас в стадии разработки, из-за чего, к сожалению, пока не может принимать заказы, поэтому просим оставить вашу заявку на оформление подписки через [google форме](https://docs.google.com/forms/d/e/1FAIpQLScp8bp0kWE1daHIbh6s5sClZGchgiVujYQHdHwlgZbBkfjnHA/viewform?usp=sf_link)', parse_mode='Markdown', reply_markup=telebot.types.ReplyKeyboardRemove())
    elif message.text=="назад":
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
        item1 = types.KeyboardButton("заказать одежду или обувь")
        item2 = types.KeyboardButton("оформить подписку")
        item3 = types.KeyboardButton("оставить отзыв")
        markup.add(item1)
        markup.add(item2)
        markup.add(item3)
        bot.send_message(message.chat.id, 'хотите заказать одежду или обувь? нажмите "заказать одежду или обувь". \nхотите оформить подписку? нажмите "оформить подписку". \nхотите оставить отзыв? нажмите "оставить отзыв"', reply_markup=markup)
    elif message.text=="отзыв":
        bot.send_message(message.chat.id,'если вы остались неудовлетворены нашим сервисом, пожалуйста, сообщите нам. если вы хотите похвалить нас, не стесняйтесь', reply_markup=telebot.types.ReplyKeyboardRemove())

bot.polling(none_stop=True, interval=0)
