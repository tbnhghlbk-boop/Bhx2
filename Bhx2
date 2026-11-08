from telegram import Update, InlineKeyboardButton, InlineKeyboardMarkup
from telegram.ext import Application, CommandHandler, CallbackQueryHandler, ContextTypes

TOKEN = "9026877062:AAFOxcYVAO-KCh6jcrtkuh_5yzWYap_Vi7A"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    keyboard = [
        [InlineKeyboardButton("المميزات", callback_data="features")]
    ]
    reply_markup = InlineKeyboardMarkup(keyboard)

    await update.message.reply_text(
        "اهلا بك في BOT BHX TEAM 🔥\n"
        "ادخل كودك للتفعيل\n"
        "او كلم المطور لشراء الكود : @BHX_TEAM",
        reply_markup=reply_markup)

async def button(update: Update, context: ContextTypes.DEFAULT_TYPE):
    query = update.callback_query
    await query.answer()
    if query.data == "features":
        await query.edit_message_text("""شرحالخدمات 🤖:
▪️ كشف الاستعادة: لمعرفة البريد المربوط بالحساب.
▪️ كشف روابط: لمعرفة جميع الروابط المربوطة.
▪️ بوت رمز الأمان: يخمن رمز الأمان تلقائيا.
▪️ تجربة رمز الأمان: لتجربة الرموز يدويا.
▪️ إضافة/تغيير/إلغاء الاستعادة: لإدارة البريد.
▪️ حرق التوكن: لتسجيل الخروج من البوت.
▪️ سبام تسجيل دخول: لعمل سبام على الحساب.
▪️ دخول لحساب مبند""")

app = Application.builder().token(TOKEN).build()
app.add_handler(CommandHandler("start", start))
app.add_handler(CallbackQueryHandler(button))

print("البوت شغال...")
app.run_polling()
