# Standalone deployment check

Date: 2026-10-11.
Source commit: `6bf947ec3bab581aa49300304f7c49936d00508a`.
Build: `0.6.2-main-6bf947e`.

This build adds the rounded look: irregular rounded stones, rounded box
edges, smooth trees and rocks, draped Quidditch stands and oak castle doors.

## Completed checks

- `node tools/validate.mjs`: passed. Checked 250 files, 247 JavaScript modules
  and 59 story items. The package is self-contained.
- `node tools/render-scale-test.mjs`: passed. Checked the adaptive resolution
  limits, recovery and disabled states.
- `node tools/build-standalone.mjs 0.6.2-main-6bf947e`: passed.
- `node tools/hebrew-interface-test.mjs file:///opt/src/harrygame1/local/tmp/deploy-6bf947e/local/build/HarryStudentWhoWasntThere-0.6.2-main-6bf947e/Play.html`:
  passed, 30 checks. No browser errors.
- `node tools/autotest.mjs --base file:///opt/src/harrygame1/local/tmp/deploy-6bf947e/local/build/HarryStudentWhoWasntThere-0.6.2-main-6bf947e/Play.html --jobs 1 A01 A11`:
  passed, 2 of 2 story items.
- `node tools/lighting-test.mjs file:///opt/src/harrygame1/local/tmp/deploy-6bf947e/local/build/HarryStudentWhoWasntThere-0.6.2-main-6bf947e/Play.html`:
  passed. Checked 12 views on all nine maps at Low and Medium.
- `index.html` and `Play.html` match the tested build byte for byte.
- GitHub Pages deployment completed for commit `62c8d23`. Public URL:
  `https://nnnsss999.github.io/harry-play/`.
- Downloads of the public root page and `Play.html` match the tested build
  byte for byte.
- `node tools/hebrew-interface-test.mjs https://nnnsss999.github.io/harry-play/`:
  passed, 30 checks. No JavaScript errors.
- `node tools/autotest.mjs --base https://nnnsss999.github.io/harry-play/ --jobs 1 A01`:
  passed, 1 of 1 story item.
- `node tools/lighting-test.mjs https://nnnsss999.github.io/harry-play/`:
  passed, 12 views at Low and Medium. The captures show the new stones.

SHA256: `87465d3c2c6f58bcdc62789e64b20083c39a1856741f6245d186d1b963ac3b9b`.

## Limits

The browser checks use installed Chrome on Linux with SwiftShader. They do
not establish hardware performance or acceptance on a physical phone or
tablet. The tool lock file did not change after the last deployment. The full
story route was not run again for this deployment. The source record
(`docs/verification/rounded-look-verification.md`) has that result.
