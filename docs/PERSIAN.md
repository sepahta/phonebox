# Persian interface

Persian translation and integration maintained by Mani Nezafat (مانی نظافت). PhoneBox remains an MIT-licensed project by Ersin KOÇ and contributors.

Select **فارسی** in the settings language selector. `fa` is accepted by the desktop configuration normalizer and persisted with the existing settings. A Persian browser/phone locale is also detected in Follow system mode.

This branch adds all 830 English keyed strings, all 683 catalog labels/descriptions/options covered by the full reference catalog, and all 275 panel literals currently wrapped by the panel translation helper. The native Android pairing dialogs have matching Persian resources. Technical identifiers, file paths, API names, code samples and saved values remain unchanged. Unwrapped upstream interface literals and user-defined page/shortcut names are not automatically translated.

The document switches to RTL for Persian and back to LTR for other languages. Grid coordinates and the pager remain LTR to preserve the saved arrangement and swipe behavior. Widget text follows RTL; code and technical inputs remain LTR. The main clock displays Persian digits; dates use the Persian browser locale. API data and timestamps retain their original format.

No translation service is called by the application at runtime. All translated strings ship locally in `i18n.js`.

Validation:

```sh
node tools/test-persian.cjs
python3 tools/check-release.py
```

Run the demo with `python3 tools/demo-server.py 8791`, open `/settings/`, and select فارسی. The demo contains simulated data and does not change the running desktop agent. Device and visual testing are required in addition to dictionary coverage tests; coverage does not guarantee translation quality.
