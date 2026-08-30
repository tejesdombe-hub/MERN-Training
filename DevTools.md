# Chrome DevTools Analysis Report

Website: https://www.meesho.in
Browser: Google Chrome

## 1. Largest Image on the Page

I opened Amazon.in and went to **DevTools → Network → Img. After reloading the page, I checked the image requests and sorted them by size.

The largest image I found was , with a size of approximately 21.7kb .

Web img Link : [https://images.meesho.com/images/products/541357581/00a6u_512.avif?width=360]

## 2. Request Taking More Than 500ms

After reloading the Amazon.in page, I checked the requests in the Network tab and sorted them based on their duration.

During my test, I did not find any request that took more than 500ms. The slowest request I observed took approximately 273ms.

Therefore, no request exceeded the 500ms threshold during my testing session.

The response times may vary depending on network conditions, server load, caching, and the resources requested by the website.

Link : https://www.meesho.com/ez-iphone-16-pro-boomtp-17/p/7iovki

## 3. Cookie Set by the Website

I opened DevTools → Application → Cookies → meesho.in
and checked the cookies created by the website.

I found a cookie named SID. With Value :  g.a000CAnsKrqMy4ssF9ALMBDok7JMMQGHwxnmk2SLDq_sb2uGhFIWYZ-ido1nft9UrkBgEhpyCAACgYKARwSARQSFQHGX2MiWUkoFbGnJUTYDiZzptlUFhoVAUF8yKp5UUZiYKHYK2Vg305sti1F0076

Its expiry is -> 2027-10-01T10:12:42.709Z

screenshot: : https://drive.google.com/drive/folders/1YYmanRPgkqZH4SKrLCRH1_HI1hsBBDif?usp=sharing

## 4. JavaScript File and Loading Behavior

I opened DevTools → Network → JS and selected one JavaScript file loaded by the website.

The JavaScript file was _buildMenifest.js. -> defer it using the defer while calling the script .. means it execute while html parsing and onece parsing finished it load the script ..

I then checked the corresponding `<script>` element in the Elements panel to determine how it was loaded.


A normal script without `async` or `defer` can block HTML parsing while it is downloaded and executed. An `async` script downloads independently and executes as soon as it is available. A `defer` script downloads while HTML parsing continues and executes after the HTML has been parsed.

Screenshot: https://drive.google.com/drive/folders/1YYmanRPgkqZH4SKrLCRH1_HI1hsBBDif?usp=sharing

