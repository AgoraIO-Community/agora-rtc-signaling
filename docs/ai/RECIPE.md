# RTC Signaling Sample

## Overview

Coordinate RTC call setup and participant state with signaling around Agora real-time media.

Repository: [AgoraIO-Community/agora-rtc-signaling](https://github.com/AgoraIO-Community/agora-rtc-signaling)

## Prerequisites and Setup

1. Install Node.js compatible with this repository's package manifest and use a WebRTC-capable browser.
2. At the repository root, run `npm install` followed by `npm run dev`. Open the Vite URL (the README uses `http://localhost:5173`).
3. Enter the App ID and a distinct User ID for each client, then click Login.
4. Use Subscribe for the signaling channel and Join Channel for RTC video. Open a second client with the same App ID and channel; use a different user ID.
5. Use `npm run build` to check the production bundle.

## What To Check

- Send both group and peer messages and verify their intended recipients.
- Test mute, device selection and presence updates with two clients.
- Leave the RTC channel, unsubscribe from signaling and log out; confirm both lifecycles terminate.

## Integration Notes

RTC and RTM are separate services and lifecycles. Preserve both configuration paths and obtain the appropriate service tokens from a trusted backend when authentication is required.

Keep App Certificates, customer secrets and privileged token generation on a trusted backend for production. Use only your own test credentials while configuring historical demos; do not commit them. Preserve the sample's existing dependency versions and lifecycle until a separate migration is tested.

## Source References

- [README.md](../../README.md)
- [package.json](../../package.json)
- [app.js](../../app.js)

## Validation Status

This recipe was checked against the repository's source and setup documents. The platform build and live service/device flow have not been run as part of this documentation change. Complete the checks above in an environment with the required SDKs, hardware and service access before treating it as a validated deployment.

## Implementation Prompt

```text
You are working in AgoraIO-Community/agora-rtc-signaling. Use docs/ai/RECIPE.md and its linked source files to adapt the RTC Signaling Sample reference to this project.

Start by inspecting the actual sample directory and configuration described above. Resolve its listed missing prerequisites before claiming it is runnable. Preserve the existing architecture and compatible dependency versions. Implement the recipe's feature-specific flow, permissions and resource cleanup. Use a trusted backend for privileged credentials and tokens in production.

Run the repository-specific build or launch flow, then perform each What To Check item. Report the commands run, the observed results and anything blocked by service access, hardware or incomplete sample code. Do not claim live validation from a documentation or catalog build alone.
```
