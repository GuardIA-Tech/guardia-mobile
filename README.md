# guardia-mobile

GuardIA MVP - Mobile application (Flutter).

[![Work-in-progress](https://img.shields.io/badge/status-work--in--progress-yellow)](https://github.com/GuardIA-Tech/guardia-mobile)

## Architecture Overview

```text
                               +-------------------+
                               | Gemini (Vertex AI)|
                               +-------------------+
                                       ^ Enrichment
                                       |
+-------------+      +-------------------------+      +--------------------------+
| IP Cameras  |----->| guardia-backend         |<---->| Alerts (FCM, Email, SMS) |
| (RTSP/ONVIF)|      | (Python/OpenCV, FastAPI)|      +--------------------------+
+-------------+      | (Cloud Run / GKE)       |
                       +-------------------------+
                                 ^ API Calls | Notifications
                                 |           |
               +-----------------+-----------+-----------------+
               |                                               |
+-------------------------+                      +-------------------------+
| guardia-mobile          |                      | guardia-web             |
| (Flutter App)           |                      | (React App)             |
+-------------------------+                      +-------------------------+
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
