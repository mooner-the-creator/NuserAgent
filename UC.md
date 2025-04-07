# User-Capabilities

## Purpose
The `User-Capabilities` header provides a list of supported web features and technologies that can be used by servers to adapt responses to client capabilities.

## Format
A whitespace-separated list of capabilities, e.g.:

`"User-Capabilities"`: `"Cookies Frames Iframes JavaScript Tables CSS1 CSS2 CSS3"`

## Common Capabilities

### Scripting
- `JavaScript`
- `ES6`

### Layout
- `Tables`
- `Flexbox`
- `Grid`

### Styles
- `CSS1`, `CSS2`, `CSS3`, `CSS4`
- `DarkMode`
- `CustomProperties`

### Media Capabilities
- `Audio`
- `Video`
- `Autoplay`
- `WebGL`
- `WebGL2`
- `MediaSource`

### Device Features
- `Touch`
- `Mouse`
- `Controller`
- `Keyboard`
- `Voice`
- `Orientation`
- `Geolocation`

### Input Types
- `Range`
- `Date`
- `Color`
- `File`

### Storage and Data APIs
- `Cookies`
- `LocalStorage`
- `SessionStorage`
- `IndexedDB`
- `FileSystemAccess`

### Modern Web Features
- `WebRTC`
- `ServiceWorker`
- `PushAPI`
- `Notifications`
- `Clipboard`
- `Fullscreen`
- `WebXR`
- `PWA`
- `SpeechRecognition`

## Extensibility
Vendors may append custom capabilities using a namespace prefix, e.g., `AcmeCorp-XYZFeature`.

## Examples

- `"User-Capabilities"`: `"Cookies Frames JavaScript CSS3 Grid WebGL WebRTC PushAPI Touch"`
- `"User-Capabilities"`: `"JavaScript ServiceWorker WebGL2 Orientation Voice SpeechRecognition"`
- `"User-Capabilities"`: `nil`