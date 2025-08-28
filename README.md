from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

# Функция, которая будет вызываться при команде /start
def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('Привет! Я ваш бот.')

# Функция для команды /help
def help_command(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('Список команд:\n/start - начать общение\n/help - помощь')

def main() -> None:
    # Замените 'YOUR_TOKEN' на токен вашего бота
    updater = Updater(8231739787:AAGNG9TpCz-Ji9XT0XFuHJSQaTtwXzeGnP4

    # Получаем диспетчер для регистрации обработчиков
    dispatcher = updater.dispatcher

    # Регистрация команд
    dispatcher.add_handler(CommandHandler("start", start))
    dispatcher.add_handler(CommandHandler("help", help_command))

    # Запуск бота
    updater.start_polling()

    # Ожидание завершения работы
    updater.idle()

if __name__ == '__main__':
    main()
