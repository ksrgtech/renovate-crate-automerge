# renovate-crate-automerge

## What?

Rust crate introduces many semver-compatible changes with release. Renovate suggests bumping those crates, but merging them manually is painful. The combination of many repository and many release quickly become unhandleable. 

This repository provides solution to that situation. This enables [automerge](https://docs.renovatebot.com/key-concepts/automerge/) on renovate side when the new version is compatible with old version.

**You should introduce if and only if you have set up continious integration.** This config does not guarantee all of your dependency follows [SemVer compatibility guide](https://doc.rust-lang.org/cargo/reference/semver.html) nor new version has all necessary feature. They're out of scope and will not supported.

## How to use

Change your `renovate.json` to add following line:

```diff
   "extends": [
-    "config:base"
+    "config:base",
+    "github>ksrgtech/renovate-crate-automerge"
   ],
```
