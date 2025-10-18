# Additional deployment notes

- Test WebRTC in-app thoroughly (audio device selection, echo cancellation). Some electron versions may require flags for advanced codecs.
- If Browser-Phone uses service workers / PWA features, Electron may treat them differently.
- If you need TLS for SIP (WSS/TLS), ensure the WebSocket endpoints are reachable and certs are OK. For self-signed certs you may need to configure certificate handling.
- Consider setting `app.setAppUserModelId('com.yourcompany.browserphone')` on Windows for proper notifications and taskbar behavior (do it early in main).
