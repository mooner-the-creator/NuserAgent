# NuserAgent
## Format
`Info=Version/MoreInfo=Version/ExtraInfo=Version`
## Extra Info
- [User-Agent2](UA2.md): Info about the agent the request is coming from
- [User-Data](UD.md): Extra data that might help with compatibility, Properties from [user-agents.net](https://user-agents.net) are used here as well.
- [User-Capabilities](UC.md): What the user can do, used for compatibility, Capabilites & CSS from [user-agents.net](https://user-agents.net) are used here as well.
## Examples
### Example 1: Browser
#### Before
`User-Agent`: `"Mozilla/5.0 (Windows NT 10.0;) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.146 Safari/537.36 Lovense/30.6.2"`
#### After
`User-Agent2`: `"UA2=1.0.0 Lovense=30.6.2/Hytto+Ltd. Browser/Chrome=88.0.4324/Blink KHTML/Similar-Gecko Windows=10.0/32-bit/Microsoft+Corporation Desktop/Mouse"`<br>
`User-Data`: `"UA2=1.0.0 Mozilla=5.0 AppleWebKit=537.36 Chrome=88.0.4324 KHTML/Similar-Gecko"`<br>
`User-Capabilities`: `"Cookies Frames Iframes JavaScript Tables CSS1 CSS2 CSS3"`
#### Sources
https://user-agents.net/string/mozilla-5-0-windows-nt-10-0-applewebkit-537-36-khtml-like-gecko-chrome-88-0-4324-146-safari-537-36-lovense-30-6-2
### Example 2: Crawler
#### Before
`User-Agent`: `"DocBase Crawler/1.0"`
#### After
`User-Agent2`: `"UA2=1.0.0 DocBase+Crawler=1.0/DocBase Bot/Crawler"`<br>
`User-Data`: `"UA2=1.0.0 Crawler"`<br>
`User-Capabilities`: `nil`
#### Sources
https://user-agents.net/string/docbase-crawler-1-0
