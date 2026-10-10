# Standalone deployment check

Date: 2026-10-10.
Source commit: `fd3c7fac5314116e7df5252c5ed20ef48fc3c9ed`.
Build: `0.6.2-main-fd3c7fa`.

## Completed checks

- `node tools/validate.mjs`: passed. Checked 163 files, 160 JavaScript modules
  and 59 story items. The package is self-contained.
- `node tools/render-scale-test.mjs`: passed. Checked the adaptive resolution
  limits, recovery and disabled states.
- `node tools/build-standalone.mjs 0.6.2-main-fd3c7fa`: passed.
- `node tools/hebrew-interface-test.mjs file:///opt/src/harrygame1/local/build/HarryStudentWhoWasntThere-0.6.2-main-fd3c7fa/Play.html`:
  passed, 19 checks. Checked Hebrew layout, settings and control persistence,
  touch controls, exhibition play, and story save isolation. No browser errors.
- `node tools/autotest.mjs --base file:///opt/src/harrygame1/local/build/HarryStudentWhoWasntThere-0.6.2-main-fd3c7fa/Play.html --jobs 1 A01 A11`:
  passed, 2 of 2 story items.
- `index.html` and `Play.html` match the tested build byte for byte.
- GitHub Pages deployment completed for commit `ac022a3`. Public URL:
  `https://nnnsss999.github.io/harry-play/`.
- Downloads of the public root page and `Play.html` match the tested build
  byte for byte.
- `node tools/hebrew-interface-test.mjs https://nnnsss999.github.io/harry-play/`:
  passed, 19 checks. No JavaScript errors.
- `node tools/autotest.mjs --base https://nnnsss999.github.io/harry-play/ --jobs 1 A01`:
  passed, 1 of 1 story item.

SHA256: `5da445c5b9f3ab09c94ea9be45117f1a721b9284e9a715119b2b6fa8b7c64380`.

## Limits

The browser checks use installed Chrome on Linux with SwiftShader. They do
not establish hardware performance or acceptance on a physical phone or
tablet. `npm ci` was not run again; the tool lock file did not change after
the last deployment. The full story route was not run again for this
deployment. The source record for this commit has that result.
