# Awesome Playable Ads

A curated collection of useful resources, articles, tools, and inspiration for creating and understanding playable ads.

## What are Playable Ads?
Playable ads are interactive advertisements that allow users to engage with a mini-version of an app or game before downloading or purchasing. They are widely used in mobile marketing to increase user engagement and conversion rates.

## Frameworks and engines can be used for Playable Ads development
- [Three.js](https://threejs.org/) – JavaScript 3D library for creating interactive 3D content in the browser.
- [PixiJS](https://pixijs.com/) – Fast 2D rendering engine for creating rich, interactive graphics and games.
- [Construct 3](https://www.construct.net/) – Powerful no-code/low-code game development platform ideal for building playable ads.

## Technical Requirements of Ad Networks


Playable ads must comply with the technical specifications set by various ad networks to ensure compatibility and optimal performance. Below are requirements and validation tools for major networks:

| Ad Network      | File Size & Format         | Validation Tools / Links | Notes |
|-----------------|---------------------------|--------------------------|-------|
| **Facebook Ads** | 2MB (HTML), 5MB (ZIP)     | [Playable Preview](https://developers.facebook.com/tools/playable-preview/) *(public tool does not test ZIPs; use Ads Manager for full validation)* | |
| **Google Adwords** | 5MB (ZIP)                | [H5 Validator](https://h5validator.appspot.com/dcm/asset) | |
| **Unity**         | 5MB (HTML)                | [iOS Validator](https://apps.apple.com/us/app/ad-testing/id1463016906), [Android Validator](https://play.google.com/store/apps/details?id=com.unity3d.auicreativetestapp&hl=en_US) | Rejects on invalid URLs in playable. Check embedded links and avoid Cyrillic. Google Play links should be short (e.g., `https://play.google.com/store/apps/details?id=my.arena`). Use CTA button for store redirects. Alerts for misclicks. |
| **AppLovin**      | 5MB (HTML)                | [Web Validator](https://p.applov.in/playablePreview?create=1&qr=1), [iOS App](https://apps.apple.com/us/app/playable-preview/id6468529760), [Android App](https://install.appcenter.ms/orgs/iosdeveloper-dbmy/apps/android-playable-preview/distribution_groups/all-users-of-android-playable-preview) | |
| **IronSource**    | 5MB (HTML)                | Only in Ads Manager      | From 2025, accepts Unity builds in MRAID (not DAPI). |
| **Moloco**        | 5MB (HTML)                | —                        | Uses Facebook's format and API. Code must NOT contain `XMLHttpRequest` (remove from PixiJS/Howler if present). |
| **TikTok**        | 5MB (ZIP)                 | [Playable Ads Help](https://ads.tiktok.com/help/article/playable-ads), [Feishu Doc 1](https://bytedance.feishu.cn/docs/doccnSSJ2uAY8EYPCAtTuoX3u9), [Feishu Doc 2](https://bytedance.us.feishu.cn/docs/doccnmdeT1KStyS0QdVExnVAy8v) | Error if `config.json` is missing—add this file to the archive. |
| **Mintegral**     | 5MB (ZIP)                 | [Mindworks Review](https://www.mindworks-creative.com/review/) | Archive name must match the main folder/file inside. |

### General Requirements
- **File Size Limits:** Most networks enforce a maximum file size (e.g., 2MB or 5MB) for fast loading.
- **Supported Formats:** HTML5 is the standard, but some networks may have additional format preferences.
- **Loading Time:** Ads should load quickly, typically within 1–3 seconds.
- **Responsive Design:** Playable ads should adapt to different screen sizes and orientations.
- **API Integrations:** Some networks require integration with their SDKs or specific event tracking APIs.
- **Asset Optimization:** Use compressed images, minified scripts, and efficient code to reduce load times.



## Contributing
Feel free to submit a pull request with more resources or suggestions!

---

*This project aims to help developers, marketers, and designers find the best resources for building and learning about playable ads.*
