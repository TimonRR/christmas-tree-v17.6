# Hand tracking assets

These files are served from this website so recognition does not depend on a separate Google Storage or MediaPipe CDN connection.

- MediaPipe Tasks Vision: version 0.10.3.
- `mediapipe/vision_bundle.mjs` and `mediapipe/wasm/*`: official npm package `@mediapipe/tasks-vision@0.10.3`, retrieved from `https://cdn.jsdelivr.net/npm/@mediapipe/tasks-vision@0.10.3/`.
- `models/hand_landmarker.task`: official float16 hand landmarker model version 1, retrieved from `https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task`.
- Model size: 7,819,105 bytes. MD5 (base64): `FTGEMOo4UWcP6ZFBFqnPrQ==`, verified against the source response.
- MediaPipe license: Apache 2.0; see `mediapipe/LICENSE`.

Video frames are processed in the browser. The application does not upload camera frames.
