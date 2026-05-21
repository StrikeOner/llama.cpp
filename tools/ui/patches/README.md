# Patches

## mermaid-support.patch

Adds [Mermaid](https://mermaid.js.org/) diagram rendering support to the llama.cpp built-in server frontend (`tools/ui`). When a code block is annotated with the `mermaid` language tag, it is rendered as an interactive diagram instead of raw text.

### Compatibility

Generated against: 40d5358

### Usage

**Option A — use the fork branch directly:**

```bash
git clone -b feature/mermaid https://github.com/StrikeOner/llama.cpp
```

**Option B — apply the patch to your existing checkout:**

```bash
# from the root of your llama.cpp checkout
curl -O https://raw.githubusercontent.com/StrikeOner/llama.cpp/feature/mermaid/tools/ui/patches/mermaid-support.patch
git apply tools/ui/patches/mermaid-support.patch

# reinstall dependencies to pick up mermaid
cd tools/ui && npm install
```

### Notes

- `package-lock.json` is intentionally excluded from the patch — `npm install` regenerates it
- The patch is kept in sync with upstream on a best-effort basis
