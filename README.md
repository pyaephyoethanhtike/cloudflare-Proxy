# golafzani-panel 📡
Persian EDtunnel - GolafzaniPanel: a serverless cloudflare worker used for unbreak the filternet!

GitHub Repository for https://github.com/zizifn/edgetunnel
Github Repository for sample: https://github.com/3Kmfi6HP/EDtunnel

ask question and cloudflare ips: https://t.me/moeinnetworkchat
our official channel: https://t.me/moeinnetwork

See YouTube Video:

https://www.youtube.com/watch?v=8I-yTNHB0aw

#  فارسی 🇮🇷 📡 نحوه نصب پنل گل افزانی بر روی ورکر کلودفلر در صورت نیاز به خواندن متن انگلیسی به آخر متن فارسی مراجعه کنید

این استقرار مخزن را در صفحات cloudflare کلون کنید.

# در worker.dev مستقر کنید
کد _worker.js را از اینجا کپی کنید.

همچنین، می‌توانید روی دکمه زیر کلیک کنید تا مستقیماً مستقر شود.

# مستقر در Cloudflare Workers

تنظیمات UUID (اختیاری)
هنگام استقرار در صفحات cloudflare، می توانید uuid را در فایل wrangler.toml تنظیم کنید. نام متغیر UUID است. فایل wrangler.toml نیز پشتیبانی می شود. (توصیه می شود) در صورت استقرار در صفحات وب، نمی توانید uuid را در فایل wrangler.toml تنظیم کنید.

هنگام استقرار در worker.dev، می توانید uuid را در فایل _worker.js تنظیم کنید. نام متغیر userID است. فایل wrangler.toml نیز پشتیبانی می شود. (توصیه می شود) در صورت استقرار در صفحات وب، نمی توانید uuid را در فایل wrangler.toml تنظیم کنید. در این حالت می توانید uuid را در متغیر محیطی UUID نیز تنظیم کنید.

توجه: UUID همان uuid است که می‌خواهید تنظیم کنید. روش pages.dev و worker.dev همه آنها پشتیبانی می شود، اما به روش استقرار شما بستگی دارد.

مثال تنظیم UUID
متغیر محیطی تک uuid

UUID = "uuid here you want to set"
چند متغیر محیطی uuid

UUID = "uuid1,uuid2,uuid3"
توجه: uuid1، uuid2، uuid3 با کاما از هم جدا می شوند. هنگامی که چندین uuid را تنظیم می کنید، می توانید از https://edtunnel.pages.dev/uuid1 برای دریافت پیوند clash و vless:// استفاده کنید.

اشتراک vless:// لینک (اختیاری)
برای دریافت لینک اشتراک، به https://edtunnel.pages.dev/uuid مجموعه خود مراجعه کنید.

از https://edtunnel.pages.dev/sub/uuid مجموعه خود بازدید کنید تا محتوای اشتراک با uuid مسیر تعیین شده خود را دریافت کنید.

توجه: uuid مجموعه شما همان uuid است که در محیط UUID یا فایل wrangler.toml، _worker.js تنظیم می کنید. وقتی چند uuid تنظیم می‌کنید، می‌توانید از https://edtunnel.pages.dev/sub/uuid1 برای دریافت محتوای اشتراک با مسیر uuid1 استفاده کنید. (فقط از اولین uuid در مجموعه uuid چندگانه پشتیبانی کنید)

از https://edtunnel.pages.dev/sub/uuid your set/?format=clash دیدن کنید تا محتوای اشتراک را با uuid مسیر تعیین شده و قالب کلش خود دریافت کنید. محتوا با کد base64 باز خواهد گشت.

توجه: uuid مجموعه شما همان uuid است که در محیط UUID یا فایل wrangler.toml، _worker.js تنظیم می کنید. وقتی uuid چندگانه تنظیم می‌کنید، می‌توانید از https://edtunnel.pages.dev/sub/uuid1/?format=clash برای دریافت محتوای اشتراک با مسیر uuid1 و فرمت کلش استفاده کنید. (فقط از اولین uuid در مجموعه uuid چندگانه پشتیبانی کنید)

مشترک شدن پیوند Cloudflare bestip (IP خالص).
برای دریافت اطلاعات اشتراک، به https://edtunnel.pages.dev/bestip/uuid مجموعه خود مراجعه کنید.

پیوند url اشتراک cpoy https://edtunnel.pages.dev/bestip/uuid مجموعه خود را برای هر کلاینت (clash/v2rayN/v2rayNG) که می خواهید استفاده کنید.

انجام شده. اگر سوالی دارید لطفا به @moeinnetworkchat در تلگرام بپیوندید

پشتیبانی از چند پورت (اختیاری)
برای لیست پورت های پشتیبانی شده از Cloudflare، لطفاً به اسناد رسمی مراجعه کنید.

به طور پیش فرض، پورت 80 و 443 است. اگر می خواهید پورت های بیشتری اضافه کنید، می توانید از پورت های زیر استفاده کنید:

80, 8080, 8880, 2052, 2086, 2095, 443, 8443, 2053, 2096, 2087, 2083
پورت http: 80، 8080، 8880، 2052، 2086، 2095
پورت https: 443, 8443, 2053, 2096, 2087, 2083
اگر در صفحات cloudflare مستقر می شوید، پورت https پشتیبانی نمی شود. به سادگی چندین پورت را اضافه کنید و از لینک اشتراک استفاده کنید، محتوای اشتراک همه پورت های پشتیبانی شده از Cloudflare را برمی گرداند.

پروکسی IP (اختیاری)
هنگام استقرار در صفحات cloudflare، می توانید پروکسی IP را در فایل wrangler.toml تنظیم کنید. نام متغیر PROXYIP است.
همچنین توضیح می دهم که چگونه IP پاک را در سورس کد کارگر من نوشته شده در golafzani_worker.js ایجاد کنم.

هنگام استقرار در worker.dev، می توانید پروکسی IP را در فایل _worker.js تنظیم کنید. نام متغیر proxyIP است.

توجه: پروکسی آی پی یا دامنه ای است که می خواهید تنظیم کنید. این بدان معنی است که پروکسی IP برای هدایت ترافیک از طریق یک پروکسی به جای مستقیم به وب سایتی که از Cloudflare (CDN) استفاده می کند، استفاده می شود. اگر این متغیر را تنظیم نکنید، اتصال به IP Cloudflare لغو (یا مسدود می شود)...

نتایج: سوکت های خروجی TCP به محدوده IP Cloudflare به طور موقت مسدود شده اند، لطفاً به مستندات سوکت های tcp مراجعه کنید.

استفاده
ابتدا دامنه pages.dev خود را https://edtunnel.pages.dev/ در مرورگر خود باز کنید، سپس می توانید صفحه زیر را مشاهده کنید: مسیر /uuid تنظیمات خود را برای دریافت پیوند clash config و vless://.

# English: How to install Golafzani panel on cloudflare worker


Clone this repository deploy in cloudflare pages.

# Deploy in worker.dev
Copy _worker.js code from here.

Alternatively, you can click the button below to deploy directly.

# Deploy to Cloudflare Workers

UUID Setting (Optional)
When deploy in cloudflare pages, you can set uuid in wrangler.toml file. variable name is UUID. wrangler.toml file is also supported. (recommended) in case deploy in webpages, you can not set uuid in wrangler.toml file.

When deploy in worker.dev, you can set uuid in _worker.js file. variable name is userID. wrangler.toml file is also supported. (recommended) in case deploy in webpages, you can not set uuid in wrangler.toml file. in this case, you can also set uuid in UUID enviroment variable.

Note: UUID is the uuid you want to set. pages.dev and worker.dev all of them method supported, but depend on your deploy method.

UUID Setting Example
single uuid environment variable

UUID = "uuid here your want to set"
multiple uuid environment variable

UUID = "uuid1,uuid2,uuid3"
note: uuid1, uuid2, uuid3 are separated by commas,. when you set multiple uuid, you can use https://edtunnel.pages.dev/uuid1 to get the clash config and vless:// link.

subscribe vless:// link (Optional)
visit https://edtunnel.pages.dev/uuid your set to get the subscribe link.

visit https://edtunnel.pages.dev/sub/uuid your set to get the subscribe content with uuid your set path.

note: uuid your set is the uuid you set in UUID enviroment or wrangler.toml, _worker.js file. when you set multiple uuid, you can use https://edtunnel.pages.dev/sub/uuid1 to get the subscribe content with uuid1 path.(only support first uuid in multiple uuid set)

visit https://edtunnel.pages.dev/sub/uuid your set/?format=clash to get the subscribe content with uuid your set path and clash format. content will return with base64 encode.

note: uuid your set is the uuid you set in UUID enviroment or wrangler.toml, _worker.js file. when you set multiple uuid, you can will use https://edtunnel.pages.dev/sub/uuid1/?format=clash to get the subscribe content with uuid1 path and clash format.(only support first uuid in multiple uuid set)

subscribe Cloudflare bestip(pure ip) link
visit https://edtunnel.pages.dev/bestip/uuid your set to get subscribe info.

cpoy subscribe url link https://edtunnel.pages.dev/bestip/uuid your set to any clients(clash/v2rayN/v2rayNG) you want to use.

done. if have any questions please join @moeinnetworkchat in telegram

multiple port support (Optional)
For a list of Cloudflare supported ports, please refer to the official documentation.

By default, the port is 80 and 443. If you want to add more ports, you can use the following ports:

80, 8080, 8880, 2052, 2086, 2095, 443, 8443, 2053, 2096, 2087, 2083
http port: 80, 8080, 8880, 2052, 2086, 2095
https port: 443, 8443, 2053, 2096, 2087, 2083
if you deploy in cloudflare pages, https port is not supported. Simply add multiple ports node drictly use subscribe link, subscribe content will return all Cloudflare supported ports.

proxyIP (Optional)
When deploy in cloudflare pages, you can set proxyIP in wrangler.toml file. variable name is PROXYIP.
also i explain how to generate Clean IP in my worker source code writed in golafzani_worker.js

When deploy in worker.dev, you can set proxyIP in _worker.js file. variable name is proxyIP.

note: proxyIP is the ip or domain you want to set. this means that the proxyIP is used to route traffic through a proxy rather than directly to a website that is using Cloudflare's (CDN). if you don't set this variable, connection to the Cloudflare IP will be cancelled (or blocked)...

resons: Outbound TCP sockets to Cloudflare IP ranges are temporarily blocked, please refer to the tcp-sockets documentation

Usage
frist, open your pages.dev domain https://edtunnel.pages.dev/ in your browser, then you can see the following page: The path /uuid your seetting to get the clash config and vless:// link.
