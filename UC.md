# UC.md
# User-Capabilities

## Purpose
User-Capabilities explicitly indicates which web technologies and features the client supports, allowing servers to make informed decisions about content delivery without relying on User-Agent sniffing.

## Format
Space-separated list of supported capabilities:
`Capability1 Capability2 Capability3`

## Relationship with Feature Detection
User-Capabilities complements client-side feature detection:
- Server uses User-Capabilities for initial content decisions
- Client refines experience using feature detection
- Both mechanisms work together to optimize the user experience

User-Capabilities should reflect actual support, not theoretical capabilities based on version numbers.

## Capability Naming Conventions
- Use singular nouns for discrete capabilities (e.g., "Canvas" not "Canvases")
- Use PascalCase for multi-word capabilities (e.g., "LocalStorage")
- When appropriate, use plus sign for related features (e.g., "Background+Sounds")
- Capabilities should represent concrete features, not abstract concepts

## Standard Properties

### CSS Support
- `CSS1`: Supports CSS Level 1
- `CSS2`: Supports CSS Level 2
- `CSS3`: Supports CSS Level 3
- `CSS4`: Supports CSS Level 4

### Content Structure
- `Tables`: Supports HTML tables
- `Frames`: Supports frame elements
- `Iframes`: Supports inline frames

### Programming
- `JavaScript`: Supports JavaScript execution
- `Java`: Supports Java applets
- `ActiveX`: Supports ActiveX controls
- `VBScript`: Supports Visual Basic Script

### User Interaction
- `Cookies`: Supports HTTP cookies
- `LocalStorage`: Supports Web Storage API (localStorage)
- `SessionStorage`: Supports Web Storage API (sessionStorage)
- `ServiceWorker`: Supports Service Worker API
- `Touch`: Supports touch events
- `Pointer`: Supports pointer events
- `Gamepad`: Supports gamepad input

### Media Capabilities
- `Canvas`: Supports Canvas API
- `WebGL`: Supports WebGL
- `WebGL2`: Supports WebGL 2
- `Audio`: Supports HTML5 audio
- `Video`: Supports HTML5 video
- `MediaRecorder`: Supports MediaRecorder API
- `Background+Sounds`: Supports background audio

### Modern Web Features
- `WebAssembly`: Supports WebAssembly
- `WebRTC`: Supports WebRTC
- `WebSockets`: Supports WebSockets
- `WebWorkers`: Supports Web Workers
- `WebComponents`: Supports Web Components
- `Fetch`: Supports Fetch API
- `Geolocation`: Supports Geolocation API

## Usage Examples

### Modern Desktop Browser
`Cookies Frames Iframes JavaScript Tables CSS1 CSS2 CSS3 LocalStorage SessionStorage Canvas WebGL Audio Video Fetch WebSockets WebWorkers WebComponents ServiceWorker Pointer`

### Mobile Browser with Limited Support
`Cookies JavaScript Tables CSS1 CSS2 CSS3 LocalStorage SessionStorage Canvas Audio Video Touch Fetch`

### Simple Bot or Crawler
`nil` or `JavaScript CSS1 CSS2`

### Legacy Browser
`Cookies Frames JavaScript Tables CSS1 CSS2 Java`