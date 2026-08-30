1. What is the difference between 301 and 302?

301 means the resource or page has been moved permanently to another URL. So whenever the user requests the old URL, the server redirects them to the new URL. 302 is used when the redirection is temporary, means currently the resource is available at another URL but later it can come back to the original URL.

2. Why is PUT idempotent but POST is not?

First thing to understand is idempotent means repeating the same action should result in the same final result. That's why PUT is idempotent because if we send the same PUT request multiple times, it will update the same resource with the same data. But POST is not idempotent because every time we send the same POST request, it can create a new resource, which can result in duplicate resources.

3. What is the difference between localStorage and sessionStorage?

localStorage is used to store data in the browser which should remain even after we close the tab or browser, until we manually remove it or the browser clears it. sessionStorage is used to store data only for the current browser tab/session, and when we close that tab, the stored data is removed. Both are mainly used for storing client-side data, but their main difference is their lifetime.

4. What triggers a reflow vs a repaint?

After the browser creates the DOM and CSSOM, it calculates the layout and then paints the page. Reflow happens when we make some change which affects the layout or position of elements, like changing width, height, font size, adding or removing elements etc. Repaint happens when only the visual appearance changes, like changing color or background color, without changing the layout. So simply we can remember reflow means layout change and repaint means visual change.

5. What is CORS and why does it exist?

Before understanding CORS, we need to understand SOP which is Same-Origin Policy. It means the browser allows JavaScript to access resources from the same origin, but it restricts accessing data from a different origin. CORS means Cross-Origin Resource Sharing, which allows the server to tell the browser which different origins are allowed to access its resources. It exists because of browser security, so any website cannot freely access sensitive data from another website. For example, frontend running on one origin can call a backend running on another origin if the backend allows that origin through CORS.