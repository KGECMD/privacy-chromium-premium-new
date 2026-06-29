# Default Settings

Vanilla Chromium settings are not often changed by Privacy-Chromium Premium Edition, however there are some exceptions.  
Below is a list of the documented changes to the default Chromium settings.

## Core Privacy & Security Settings

Setting | New State | Location
-- | -- | --
Allow sites to check if you have payment methods saved | Disabled | chrome://settings/payments
Ask where to save each file before downloading | Enabled | chrome://settings/downloads
Auto sign-in | Disabled | chrome://settings/passwords
Block third-party cookies | Enabled | chrome://settings/cookies
Continue running background apps when Chromium is closed | Disabled | chrome://settings/system
Hyperlink auditing (a ping) | Disabled | NA
Link Doctor | Disabled | NA
Offer to save passwords | Disabled | chrome://settings/passwords
Payment autofill | Disabled | chrome://settings/payments
Preload pages | Disabled | chrome://settings/performance
Search suggestions | Disabled | chrome://settings/syncSetup
Show bookmark bar | Enabled | chrome://settings/appearance
Third-party sign-in | Disabled | --enable-features=FedCm
WebRTC IP handling policy | Disable Non-Proxied UDP | --webrtc-ip-handling-policy

## Privacy-Chromium Premium Edition Additional Defaults

### Network & Connection Privacy

Setting | New State | Rationale
-- | -- | --
HTTPS-Only Mode | Enabled | Force secure connections when available
DoH (DNS-over-HTTPS) | Enabled | Encrypted DNS queries
Strict Referrer Policy | Enabled | Controls referrer information leakage
Network Time Service | Disabled | No external time queries

### Tracking & Fingerprinting Protection

Setting | New State | Rationale
-- | -- | --
Privacy Sandbox | Disabled | No tracking or profiling
Client Hints API | Disabled | Prevents fingerprinting
Metrics/Usage Statistics | Disabled | No telemetry collection
Tracking Protection | Standard+ | Blocks known trackers
Canvas Fingerprinting | Noise | Prevents canvas fingerprinting
Client Rect Noise | Enabled | Prevents element dimension fingerprinting
WebGL | Limited | Reduces fingerprinting surface

### Search & Discovery

Setting | New State | Rationale
-- | -- | --
Default Search Engine | SearXNG | Privacy-respecting search
Spell Check Suggestions | Local Only | No cloud-based spell checking
Translate Prompts | Disabled | No Google Translate integration

### Data Collection Prevention

Setting | New State | Rationale
-- | -- | --
Safe Browsing | Disabled | Uses local blocklists instead
Crash Reports | Disabled | No crash data sent
Domain Reliability | Disabled | No domain health reporting
MEI Preload | Disabled | No media engagement data
Google Host Detection | Disabled | No connectivity checks to Google

### Build-Time Privacy Flags

Setting | Rationale
-- | --
Google API Keys | Empty - no Google API access
Safe Browsing Mode | Disabled
Reporting | Disabled
Field Trial Testing | Disabled
CRLSET Updates | Uses bundled CRLset only

## Command Line Switches

Privacy-Chromium Premium Edition includes additional command-line switches for advanced configuration:

- --disable-client-hints - Disable Client Hints API
- --disable-features=PrivacySandbox - Disable Privacy Sandbox entirely
- --force-dark-mode - Enable dark mode (when available)
- --enable-features=WebRtcHideLocalIps - Hide local IPs in WebRTC
- --enable-features=CanvasOopRasterization - Enable out-of-process canvas
- --no-default-browser-check - Skip default browser check
- --reduce-security-for-testing - Disable some security for specific testing scenarios (use with caution)

## Privacy-Focused Behaviors

1. **No Telemetry**: All metrics and usage reporting are disabled
2. **No Google Services**: All connections to Google services are blocked
3. **Enhanced Isolation**: Third-party storage partitioning is enabled
4. **Strong Defaults**: Security-conscious defaults for all privacy-sensitive settings
5. **Minimal Network Requests**: Background services that make network requests are disabled
