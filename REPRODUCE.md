# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py be <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 21,910 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
37e75d33b7b175a359f8f704338862fccfa4f11ba81798d8908be8181bf45db7 *be_anwaltsaufsicht.parquet
66a9e2b84f889a291f8c1d19b1ac0bfe7b1e85ce2e7386ffb5148cf362ab185d *be_bvd.parquet
3ccce24791a12f3bbe4fd393494efc8cad47c1e0d6ee809fe8a66eff6a20cbb1 *be_direktionen.parquet
084c3959c75dcf865a714bbb2ede9c92cd850d75a482035863e1f294cb7b48c4 *be_steuerrekurs.parquet
6dbbf1f4dd897b9747509cd5680029047381339bb5acb2e392a226b57e7fa360 *be_verwaltungsgericht.parquet
19808dc74895190f1613ccc08b6115f75110419aaf75aa33c6fe67ec80ff3927 *be_weitere.parquet
aa450123ee071b915e9e5ba3c62e5b6ca4516a5399d596629cacc7a9ed851dca *be_zivilstraf.parquet
```
