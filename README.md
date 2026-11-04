# Emergency Offline Kit catalog

Package manifests and profiles for [`kit`](../kit). Add it with:

    kit catalog add main https://github.com/TetrisIQ/katalog/releases/latest/download/catalog.tar.gz

## Layout
- `<category>/<id>.yaml`: one manifest per package, file name = id, unknown keys rejected.
- `profiles/<id>.yaml`: package selections with a size budget.
- `catalog.yaml`: catalog metadata (`name`, `description`, `format`).

## Rules
- Every package declares a license; no copyrighted media.
- Kiwix content has no hardcoded size, URL or checksum (read live from the Kiwix catalog).
- Any other download is `https://` with `sha256` and `size_bytes`.

Validate with `kit catalog check .`. A release tag publishes `catalog.tar.gz` and `catalog.tar.gz.sha256`.
