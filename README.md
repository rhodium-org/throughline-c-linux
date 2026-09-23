# throughline-c-linux

The **Linux kernel coding style** expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
`tl` from [throughline](https://pypi.org/project/throughline/) 3.11.0 or later.

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference
its rules as `clinux:SR-0001`.

## The Linux-kernel convention — one of two orthogonal C styles

This source captures the **Linux-kernel** C convention: 8-wide hard tabs, K&R brace
placement, an 80-column bias, Spartan naming and the kernel's own idioms. It is one
of **two orthogonal, mutually exclusive C-style choices**. The sibling source
`throughline-c-gnu` captures the **GNU** convention, which takes the opposite
position on brace placement and indentation.

**Do not compose both `throughline-c-linux` and `throughline-c-gnu` in the same
project** — they directly contradict each other. Pick exactly one C style per
codebase.

It is otherwise one of a family of **orthogonal** language and concern sources:
compose it alongside a concern source so a project's kernel-style C is grounded in
both at once.

## Status

<!-- tl:count type == 'user_requirement' -->
21
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
57
<!-- tl:end --> style rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why the guide exists), `normative: false`.
- Each numbered guide chapter as a `user_requirement` that `derives_from` the intent.
- Every individual rule as a `system_requirement` that `implements` its chapter,
  carrying the guide reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so
they cannot drift.

## Editions — dated tags

The guide is a living document. A material revision is cut as a dated tag on this
repo (e.g. `v2026-08`); a consumer pins the ref it wants.

## Composing it

```toml
[[sources]]
namespace = "clinux"
url = "https://github.com/rhodium-org/throughline-c-linux"
ref = "v2026-08"
```

Then reference a rule from your own items:

```yaml
links:
- target: clinux:SR-0001        # Linux Kernel Coding Style: one 8-character tab per level
  type: satisfies
```

`tl check` in the consuming project composes this source and resolves the reference.
A `tl` older than 3.11.0 reports it as `namespace-unresolved`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

The Linux kernel coding style is part of the Linux kernel documentation, © the Linux
kernel developers, licensed GPL-2.0. See [NOTICE](NOTICE) and
https://www.kernel.org/doc/html/latest/process/coding-style.html. This repository is
Apache-2.0 for its structure and tooling; the reproduced rule text remains the work
of the Linux kernel developers.
