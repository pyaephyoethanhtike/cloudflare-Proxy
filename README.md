# golafzani-panel 📡
Persian EDtunnel - GolafzaniPanel: a serverless cloudflare worker used for unbreak the filternet!
GitHub Repository for https://github.com/zizifn/edgetunnel
Github Repository for sample: https://github.com/3Kmfi6HP/EDtunnel

ask question and cloudflare ips: https://t.me/moeinchat
our official channel: https://t.me/moeinnetwork

See YouTube Video:

https://www.youtube.com/watch?v=8I-yTNHB0aw
 
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

done. if have any questions please join @moeinchat in telegram

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
