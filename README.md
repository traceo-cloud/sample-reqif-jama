# sample-reqif-jama

Public ReqIF sample in the shape of Jama Connect exports, with the
**fidelity receipt** [Traceo](https://traceo.cloud) writes when it reads it.

> **Read this first.** At least one file here is *shaped*: hand-written to resemble an export from Jama Connect, not produced by it. A clean read of a shaped file shows that Traceo reads that shape. It does not show that Traceo reads what the tool really emits.

## Files

| File | Kind | Source | Licence | sha256 (prefix) |
|---|---|---|---|---|
| `jama_shaped.reqif` | **shaped**: hand-written to look like the tool's export, *not* produced by it | [`jackhale98/sysml-web`](https://github.com/jackhale98/sysml-web/blob/cddbd21/src/lib/dataio/fixtures/reqif/jama.reqif) @ `cddbd21` | Apache-2.0 OR MIT | `6e422be322597a22` |

- `jama_shaped.reqif`: Hand-written in the shape of a Jama Connect export. Jama did not produce it.

Each file is copied byte-for-byte from the repository named and is unedited. Check it against the sha256.

## What Traceo kept

Traceo writes a receipt before it imports anything. The receipt counts every class of item **in**
the file and **kept**. It names every item it did not keep, with a reason code. A file with nothing
in it gets the verdict `vacuous`, never `clean`.

### `jama_shaped.reqif`

Verdict: **lossy**, some items were not kept, and every one of them is named below.

| Class | In the file | Kept |
|---|---:|---:|
| objects | 3 | 3 |
| attributes | 13 | 13 |
| enumeration values | 3 | 3 |
| link types | 1 | 1 |
| links | 1 | 1 |
| hierarchy nodes | 3 | 3 |
| attachments | 1 | 0 |

Not kept, grouped by reason:

| Class | Reason | Count | Example detail |
|---|---|---:|---|
| attachments | `ole_preview_only` | 1 | embedded object in Description |

Full receipt: [`receipts/jama_shaped.reqif.receipt.json`](receipts/jama_shaped.reqif.receipt.json)

These receipts were written by Traceo's ReqIF importer at commit `90cfc15` on 2026-11-03.

## Try it

Traceo's import screen is not released yet. When it is, importing one of these files will show
this receipt before anything is written.

## Names

Jama Connect is a trademark of its owner. It is named here only to describe the file. Traceo is not
affiliated with or endorsed by its owner.

## Licence

The `.reqif` files are third-party and keep their upstream licence. The texts are in
[`LICENSES/`](LICENSES/). The README and the `receipts/` are © Traceo, released under the MIT
licence in [`LICENSE`](LICENSE).
