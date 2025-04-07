# UA2.md
# User-Agent2

## Format Specification
`UA2=SpecVersion Key=Value/Company Application/Engine Platform/Architecture/Manufacturer DeviceType/InputMethod`

## Standard Keys
- `UA2`: The specification version of User-Agent2 (required)
- Application name and version (e.g., `Chrome=88.0.4324`, `Firefox=89.0`)
- Company name if applicable (e.g., `Hytto+Ltd.`)
- Application type (e.g., `Browser`, `Bot`, `Mobile+App`)
- Engine information (e.g., `Blink`, `Gecko`, `WebKit`)
- Platform details including version (e.g., `Windows=10.0`, `iOS=14.5`)
- Architecture (e.g., `32-bit`, `64-bit`, `ARM`, `ARM64`)
- Manufacturer (e.g., `Microsoft+Corporation`, `Apple+Inc`)
- Device type (e.g., `Desktop`, `Mobile`, `Tablet`, `Game+Console`)
- Input method (e.g., `Mouse`, `Touch`, `Voice`, `Controller`)

## Version Format
- Major version: `Major` (e.g., `11`)
- With minor: `Major.Minor` (e.g., `11.0`)
- Complete: `Major.Minor.Patch.Build` (e.g., `11.0.45.1`)
- Version is attached to key with equals sign: `Chrome=88.0.4324`

## Special Formats
- Spaces in names are represented with a plus sign: `Microsoft+Corporation`
- Forward slash separates different components: `Browser/Chrome=88.0.4324/Blink`
- "Similar" relationships use slash notation: `KHTML/Similar-Gecko`

## Examples
### Web Browser
`UA2=1.0.0 Chrome=96.0.4664/Google+Inc. Browser/Chromium/Blink Windows=10.0/64-bit/Microsoft+Corporation Desktop/Mouse+Keyboard`

### Mobile App
`UA2=1.0.0 Instagram=215.0.0/Meta+Platforms+Inc. Mobile+App/React+Native Android=12/ARM64/Samsung Mobile/Touch`

### Game Console Browser
`UA2=1.0.0 EdgeBrowser=103.0.1264/Microsoft+Corporation Browser/EdgeHTML PlayStation=5/AMD+Ryzen/Sony Game+Console/Controller`

### IoT Device
`UA2=1.0.0 SmartHome=3.2.1/Acme+Corp IoT+Client/Custom+Runtime Linux=5.10/ARM/Acme+Corp Embedded/Voice`