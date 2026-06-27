---
'@backstage/plugin-techdocs-backend': patch
---

Fixed an issue where TechDocs documentation builds that hung indefinitely (e.g. due to an unreachable docs source or a broken native dependency) would never surface an error to the user. Builds that exceed 10 minutes now time out with a clear error message instead of spinning forever.
