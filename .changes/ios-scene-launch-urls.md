---
"tao": patch
---

On iOS, emit `Event::Opened` for the URLs in the first scene's `UISceneConnectionOptions` (app launched from a custom URL scheme or universal link while not running). Previously only `scene:openURLContexts:` (app already running) produced the event, so the launch URL was silently dropped under the UIScene lifecycle.
