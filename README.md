# NuserAgent
## Introduction
NuserAgent is a modern alternative to the traditional User-Agent header, designed to provide more structured, meaningful, and easily parsable client information. While the traditional User-Agent string has become overly complex and difficult to parse reliably, NuserAgent offers a clean solution without breaking backward compatibility.

## Format
`Key=Value/Key=Value/Key=Value`

Each key-value pair is separated by a forward slash. The value may contain a plus sign (+) to represent spaces. Version information follows the key after an equals sign.

## Header Structure
- [User-Agent2](UA2.md): Core information about the client application, device, and platform
- [User-Data](UD.md): Additional technical details that help with compatibility assessment
- [User-Capabilities](UC.md): Specific features and technologies supported by the client

## Backward Compatibility
NuserAgent maintains backward compatibility by introducing new headers rather than replacing the existing User-Agent header. Systems can continue using the traditional User-Agent header while gradually adopting NuserAgent headers when available.

## Implementation Guide
Browsers and clients can implement NuserAgent by:
1. Continuing to send the traditional User-Agent header
2. Adding the three new headers with structured information
3. Ensuring consistent mapping between traditional and new formats

## Benefits
- Eliminates the need for complex User-Agent parsing libraries
- Reduces server-side processing for client detection
- Provides more accurate capability information
- Makes feature detection more reliable
- Enables more precise analytics without string manipulation

## Examples
### Example 1: Browser
#### Before
`User-Agent`: `"Mozilla/5.0 (Windows NT 10.0;) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.146 Safari/537.36 Lovense/30.6.2"`
#### After
`User-Agent2`: `"UA2=1.0.0 Lovense=30.6.2/Hytto+Ltd. Browser/Chrome=88.0.4324/Blink KHTML/Similar-Gecko Windows=10.0/32-bit/Microsoft+Corporation Desktop/Mouse"`  
`User-Data`: `"UA2=1.0.0 Mozilla=5.0 AppleWebKit=537.36 Chrome=88.0.4324 KHTML/Similar-Gecko"`  
`User-Capabilities`: `"Cookies Frames Iframes JavaScript Tables CSS1 CSS2 CSS3"`
#### Sources
https://user-agents.net/string/mozilla-5-0-windows-nt-10-0-applewebkit-537-36-khtml-like-gecko-chrome-88-0-4324-146-safari-537-36-lovense-30-6-2
### Example 2: Crawler
#### Before
`User-Agent`: `"DocBase Crawler/1.0"`
#### After
`User-Agent2`: `"UA2=1.0.0 DocBase+Crawler=1.0/DocBase Bot/Crawler"`  
`User-Data`: `"UA2=1.0.0 Crawler"`  
`User-Capabilities`: `nil`
#### Sources
https://user-agents.net/string/docbase-crawler-1-0