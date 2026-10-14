---
illustrations: patch
---

Stop publishing declaration maps. The shared `tsconfig.project.json` enables `declarationMap`, and the illustrations build only turned off `sourceMap`, so every published `.d.ts` came with an empty `.d.ts.map` (`"mappings": ""`) pointing at `src/`, which is not published. Turning them off removes ~6,400 files from the package; `.d.ts` output and import paths are unchanged.
