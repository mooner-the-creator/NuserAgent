# UD.md
# User-Data

## Purpose
User-Data provides additional technical details about the client that are helpful for compatibility assessment but aren't core identity information (which belongs in User-Agent2) or capability information (which belongs in User-Capabilities).

## Format
`UA2=SpecVersion Key=Value Key=Value Key=Value`

Multiple key-value pairs are separated by spaces. Unlike User-Agent2, forward slashes are generally not used except in relationship notations.

## When to Use User-Data vs User-Agent2
- **User-Agent2**: Core identity information about the client (what it is)
- **User-Data**: Technical implementation details (how it works)
- **User-Capabilities**: Features the client supports (what it can do)

## Standard Properties
- `Mozilla`: Traditional Mozilla compatibility version
- `AppleWebKit`: WebKit version information
- `Chrome`: Chrome version for compatibility
- `Safari`: Safari compatibility version
- `KHTML/Similar-Gecko`: Engine relationship indicators
- `Crawler`: Indicates a web crawler
- `Bot`: Indicates an automated client
- `Compatibility-Mode`: Emulation or compatibility settings

## Legacy Information
User-Data is the appropriate place to maintain information from traditional User-Agent strings that isn't directly about identity or capabilities but may be used by legacy systems for compatibility decisions.

## Custom Property Guidelines
- Custom properties should use CamelCase naming
- Version numbers should follow Major.Minor.Patch format
- Avoid duplicating information already in User-Agent2 or User-Capabilities
- Include only information relevant for compatibility assessment

## Example Mappings
### Chrome Browser
**Traditional**: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36`

**User-Data**: `UA2=1.0.0 Mozilla=5.0 AppleWebKit=537.36 Chrome=91.0.4472 Safari=537.36 KHTML/Similar-Gecko`

### Safari Browser
**Traditional**: `Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/15.0 Safari/605.1.15`

**User-Data**: `UA2=1.0.0 Mozilla=5.0 AppleWebKit=605.1.15 KHTML/Similar-Gecko Safari=605.1.15 Version=15.0`