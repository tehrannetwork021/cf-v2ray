راهنمای استفاده از ورکر Cloudflare
برای استفاده از اسکریپت Vless در Cloudflare Worker، مراحل زیر را به دقت دنبال کنید. 🔧

1️⃣ ساخت ورکر جدید در Cloudflare
وارد حساب کاربری خود در Cloudflare شوید.

به بخش Workers بروید و یک ورکر جدید بسازید.

کد موجود در فایل  Cloudflare_vless__worker.js را در ورکر خود کپی کنید 
تغییرات را ذخیره کنید.

2️⃣ اضافه کردن UUID و Proxy IP به بخش "Variables and Secrets"
برای اینکه ورکر شما به درستی کار کند، باید مقادیر خاصی را به تنظیمات ورکر خود اضافه کنید:

به بخش Settings ورکر خود بروید.
در قسمت Variables and Secrets، روی Add کلیک کنید.
موارد زیر را وارد کنید:
Variable name: proxyip
Value: ts.hpc.tw
Type: txt
برای افزودن UUID خود:
از ابزارهای آنلاین یا برنامه‌های تولید UUID(خودv2rayng) استفاده کنید.
در قسمت Variable name: uuid وارد کنید.
در قسمت Value، UUID خود را وارد کنید.
نوع (Type) را همچنان روی txt بگذارید.

3️⃣ وصل کردن ساب دامنه به ورکر
برای اتصال راحت‌تر به ورکر و استفاده از آن، باید یک ساب دامنه به ورکر خود اضافه کنید:

وارد بخش Settings ورکر شوید.
در قسمت Domains & Routes، روی Add کلیک کنید.
Custom domain را انتخاب کنید.
ساب دامنه دلخواه خود را وارد کنید (مثلاً v2.google.com یا دامنه خودتان).
در اینجا فرض می‌کنیم که شما دامنه google.com را در Cloudflare دارید، پس آن را وارد کنید.
پس از افزودن ساب دامنه، از این به بعد می‌توانید با ساب دامنه خود به ورکر دسترسی پیدا کنید.

4️⃣ استفاده از UUID برای باز کردن ورکر
پس از انجام مراحل بالا، برای دسترسی به ورکر خود، از URL زیر استفاده کنید:

bash
Copy
Edit
v2.google.com/db7dfe45-b10c-457c-81d2-0c934f3b0100
در اینجا db7dfe45-b10c-457c-81d2-0c934f3b0100 UUID شما است.


5️⃣ تنظیمات بیشتر (اختیاری)
اگر به مشکل برخوردید یا سرعت اتصال کم بود:

می‌توانید از آدرس‌های IP تمیز یا سایت‌های مختلف کلود فلر استفاده کنید.
سایت‌های پیشنهادی:
zula.ir
www.speedtest.net
iranserver.com
توجه داشته باشید که در بخش Address، باید نام ساب دامنه‌ای که به ورکر متصل کرده‌اید را وارد کنید و هیچ تغییری در Host ایجاد نکنید. 🔑

⚠️ نکات مهم:
اگر با مشکل اتصال مواجه شدید یا سرعت پایین بود، می‌توانید از آدرس‌های مختلف یا آی‌پی‌های تمیز استفاده کنید.
دقت کنید که URL ورکر خود را به درستی وارد کنید تا مشکلی در دسترسی به آن نداشته باشید.
📝 توجه:
این اسکریپت در ابتدا به زبان چینی بود و توسط تیم تهران نتورک به زبان انگلیسی ترجمه و خواناتر شده است. 🙌

با این مراحل ساده، شما می‌توانید به راحتی از تنظیمات Vless سریع و امن در Cloudflare Worker استفاده کنید. 🚀
