# Standalone deployment check

Date: 2026-10-09.
Source commit: `0e3097d58820f776c32923acdae49f8cff9f1b9f`.
Build: `0.6.2-main-0e3097d`.

## Completed checks

- `npm ci --prefix tools`: 4 packages installed; 0 reported vulnerabilities.
- `node tools/validate.mjs`: passed. Checked 163 files, 160 JavaScript modules
  and 59 story items. The package is self-contained.
- `node tools/build-standalone.mjs 0.6.2-main-0e3097d`: passed.
- `node tools/hebrew-interface-test.mjs file:///opt/src/harrygame1/local/build/HarryStudentWhoWasntThere-0.6.2-main-0e3097d/Play.html`:
  passed. Checked Hebrew layout, settings and control persistence, touch
  controls, exhibition play, and story save isolation. No browser errors.
- `index.html` and `Play.html` match the tested build byte for byte.

SHA256: `559f29d4bfbbd18afc0cb398968c787f85cf8a84f0cd3e94f229767ef451cc86`.

## Limits

The browser check uses installed Chrome on Linux with SwiftShader. It does
not establish hardware performance or acceptance on a physical phone or
tablet. The full story route was not run again for this deployment.
