# Update qanda

## 1 Setup, edit, push and build

Prerequisite (Python should be installed already):
``` shell
pip install mkdocs mkdocs-material mdx_truly_sane_lists pygments
```

Start the live-reloading docs server locally:
``` shell
mkdocs serve
```

Edit `docs/*.md` as you want. And commit and push it.

Build:
``` shell
mkdocs build
```

## 2 Deploy gh pages

Deploy to gh pages:
```
mkdocs gh-deploy
```

Finally, we can access this site (`https://XXX.github.io/qand/`).
