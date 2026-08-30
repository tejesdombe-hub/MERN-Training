# Write a 1-page markdown document in your own words explaining every step that happens when you type https://www.google.com in the browser and hit Enter. Include DNS, TCP, TLS, HTTP, HTML parsing, and rendering. Diagrams encouraged.


when we generally Enters the  https://www.google.com  in the browser  following process takes place sequentially 

What Happens When We Enter `https://www.google.com` in the Browser

When we enter `https://www.google.com` in the browser and press Enter, several processes happen between the browser and Google's server before the webpage is displayed.

The general flow is:

Enter URL
   
Browser understands URL
   
DNS Lookup
   
TCP Connection
   
TLS/HTTPS Handshake
   
HTTP Request
   
HTTP Response
   
HTML Parsing
   
DOM + CSSOM
   
Render Tree
   
Layout → Paint → Composite
   
Google page displayed


### 1. Browser receives the URL

First, the browser receives:

https://www.google.com
```

The browser understands the different parts of the URL:


https://     → Protocol/Scheme
www.google.com → Host/Domain


Since this is an HTTPS URL, the browser knows that the communication should be secure.

2. DNS Lookup

The browser needs the **IP address** of `www.google.com` because computers communicate using IP addresses.

It checks available caches first. If the IP address is not already available, a DNS lookup is performed.


www.google.com
       
      DNS
       
IP Address


DNS converts the human-readable domain name into an IP address.

 3. TCP Connection

After getting the server's IP address, the browser establishes a **TCP connection** with the server.

TCP performs a connection establishment process called the **three-way handshake**:

Client              Server

  SYN      ────────→
           ←──────── SYN-ACK
  ACK      ────────→


Now the browser and server have a TCP connection.

 4. TLS Handshake

Because the website uses HTTPS, the browser needs to establish a secure connection using TLS

During the TLS handshake, the browser and server negotiate security parameters and establish encryption keys. The browser also verifies the server's certificate.

After this step, communication can happen securely over HTTPS.


TCP Connection
      
TLS Handshake
      
Encrypted HTTPS Connection


 5. HTTP Request

Now the browser can send an HTTP request to Google.

Conceptually:

GET / HTTP/1.1
Host: www.google.com


The request travels through the network to Google's server.

. HTTP Response

Google's server processes the request and sends an HTTP response back.

The response contains a status code, headers, and usually HTML content.

For example:


HTTP/1.1 200 OK

HTML content...

The browser receives the response.

7. HTML Parsing

The browser starts parsing the received HTML.


The browser converts the HTML into a DOM

At the same time, when CSS is encountered, the browser processes it into a **CSSOM**.


HTML
 ↓
DOM

CSS
 ↓
CSSOM

 8. Render Tree

The browser combines the DOM and CSS information to create the **Render Tree**.

The Render Tree contains the elements that need to be displayed and the styles that should be applied to them.


DOM + CSSOM
     ↓
Render Tree


9. Layout

The browser calculates the exact position and size of elements on the screen.


This process is called **Layout**.

 10. Paint and Composite

After layout, the browser paints the elements such as:

Text
Images
Backgrounds
Borders
Colors


Finally, the browser composites the different layers and displays the result on the screen.


Layout
  ↓
Paint
  ↓
Composite
  ↓
Webpage displayed


Therefore, what looks like a simple action of entering `https://www.google.com` and pressing Enter actually involves several steps involving DNS, networking, security, HTTP communication, HTML/CSS processing, and browser rendering** before we finally see the webpage.
