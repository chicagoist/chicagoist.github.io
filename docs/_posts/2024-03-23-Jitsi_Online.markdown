---
layout: post
title:  "Jitsi HTML to MD"
date:   2024-03-23
categories: post posts
---
![Signature](/favicon.ico)



```html
    <!DOCTYPE html>
    <html>
      <head>
        <script src='https://8x8.vc/vpaas-magic-cookie-bd5ae19ccaee4691baefc7b2997d3455/external_api.js' async></script>
        <style>html, body, #jaas-container { height: 100%; }</style>
        <script type="text/javascript">
          window.onload = () => {
            const api = new JitsiMeetExternalAPI("8x8.vc", {
              roomName: "vpaas-magic-cookie-bd5ae19ccaee4691baefc7b2997d3455/SampleAppNewSpotlightsInterruptAside",
              parentNode: document.querySelector('#jaas-container'),
							// Make sure to include a JWT if you intend to record,
							// make outbound calls or use any other premium features!
							// jwt: "null"
            });
          }
        </script>
      </head>
      <body><div id="jaas-container" /></body>
    </html>
```
