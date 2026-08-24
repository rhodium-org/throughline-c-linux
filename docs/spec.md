# Linux kernel coding style — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses the **Linux kernel coding style** as a grounded IDD graph: each numbered chapter is a `user_requirement`, and every individual rule is a `system_requirement` that `implements` its chapter. The guide reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `clinux:SR-0001`, never by chapter name.

It carries
<!-- tl:count type == 'user_requirement' -->
21
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
57
<!-- tl:end --> style rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Kernel C is written in one consistent, readable, reviewable style** — `intent`, status `approved`

> The Linux kernel coding style exists so that C across the whole kernel tree reads as though written by one author: a single hard-tab-based layout, K&R brace placement, an 80-column bias, Spartan naming and a shared set of idioms for functions, memory, locking and messages, so that any kernel developer can read, review and change code they did not write.

**source_ref**: Linux Kernel Coding Style
<!-- tl:end -->

## Indentation

<!-- tl:item UR-0001 -->
**UR-0001 — Indentation** — `user_requirement`, status `approved`

> Rules governing the hard-tab-based indentation, its width and depth, and switch-case alignment.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Indentation
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Indentation') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Make one indentation level one 8-character tab |
| SR-0002 | system_requirement | approved | Keep nesting within about three levels |
| SR-0003 | system_requirement | approved | Align switch and its case labels in the same column |
| SR-0004 | system_requirement | approved | Put each statement on its own line |
| SR-0005 | system_requirement | approved | Indent with tabs only and leave no trailing whitespace |
<!-- tl:end -->

## Breaking Long Lines and Strings

<!-- tl:item UR-0002 -->
**UR-0002 — Breaking Long Lines and Strings** — `user_requirement`, status `approved`

> Rules governing the 80-column bias, how to break long statements and why strings are never broken.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Breaking Long Lines and Strings
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Breaking Long Lines and Strings') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0006 | system_requirement | approved | Prefer a line length of 80 columns |
| SR-0007 | system_requirement | approved | Indent a continuation well to the right of its parent |
| SR-0008 | system_requirement | approved | Never break a user-visible string across lines |
<!-- tl:end -->

## Placing Braces and Spaces

<!-- tl:item UR-0003 -->
**UR-0003 — Placing Braces and Spaces** — `user_requirement`, status `approved`

> Rules governing K&R brace placement, when braces are and are not used, and the use of spaces around keywords and operators.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Placing Braces and Spaces
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Placing Braces and Spaces') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Put the opening brace last for control blocks |
| SR-0010 | system_requirement | approved | Put a function's opening brace on its own next line |
| SR-0011 | system_requirement | approved | Keep a continuation keyword on the closing brace line |
| SR-0012 | system_requirement | approved | Omit braces around a single statement |
| SR-0013 | system_requirement | approved | Put a space after a keyword but not after a function name |
| SR-0014 | system_requirement | approved | Do not pad the inside of parentheses |
| SR-0015 | system_requirement | approved | Attach the pointer asterisk to the name |
| SR-0016 | system_requirement | approved | Space binary and ternary operators, not unary ones |
<!-- tl:end -->

## Naming

<!-- tl:item UR-0004 -->
**UR-0004 — Naming** — `user_requirement`, status `approved`

> Rules governing the Spartan naming of local and global identifiers and inclusive terminology.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Naming
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Naming') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0017 | system_requirement | approved | Keep local variable names short |
| SR-0018 | system_requirement | approved | Give globals and functions descriptive names |
| SR-0019 | system_requirement | approved | Do not encode the type into a name |
| SR-0020 | system_requirement | approved | Avoid master/slave and blacklist/whitelist terminology |
<!-- tl:end -->

## Typedefs

<!-- tl:item UR-0005 -->
**UR-0005 — Typedefs** — `user_requirement`, status `approved`

> Rules governing when a typedef may and may not be introduced.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Typedefs
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Typedefs') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0021 | system_requirement | approved | Do not typedef structures or pointers |
| SR-0022 | system_requirement | approved | Use a typedef only for a justified reason |
<!-- tl:end -->

## Functions

<!-- tl:item UR-0006 -->
**UR-0006 — Functions** — `user_requirement`, status `approved`

> Rules governing function length, single responsibility, blank-line separation, export placement and prototype ordering.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Functions —
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Functions —') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0023 | system_requirement | approved | Keep a function short and single-purpose |
| SR-0024 | system_requirement | approved | Separate functions with one blank line |
| SR-0025 | system_requirement | approved | Place the EXPORT macro after the closing brace |
| SR-0026 | system_requirement | approved | Name every parameter in a prototype without extern |
| SR-0027 | system_requirement | approved | Order the elements of a declaration consistently |
<!-- tl:end -->

## Centralized Exiting of Functions

<!-- tl:item UR-0007 -->
**UR-0007 — Centralized Exiting of Functions** — `user_requirement`, status `approved`

> Rules governing the use of goto for shared cleanup and descriptive error labels.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Centralized Exiting of Functions
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Centralized Exiting of Functions') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0028 | system_requirement | approved | Use goto for shared cleanup on multiple exits |
| SR-0029 | system_requirement | approved | Name error labels for the cleanup they perform |
<!-- tl:end -->

## Commenting

<!-- tl:item UR-0008 -->
**UR-0008 — Commenting** — `user_requirement`, status `approved`

> Rules governing what comments explain, where they go and their formatting.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Commenting
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Commenting') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0030 | system_requirement | approved | Say what code does, never how it works |
| SR-0031 | system_requirement | approved | Comment a kernel API at its head in kernel-doc |
| SR-0032 | system_requirement | approved | Format a multi-line comment with a left column of asterisks |
<!-- tl:end -->

## Kconfig Configuration Files

<!-- tl:item UR-0009 -->
**UR-0009 — Kconfig Configuration Files** — `user_requirement`, status `approved`

> Rules governing indentation of Kconfig entries and help text and advertising dangerous options.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Kconfig Configuration Files
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Kconfig Configuration Files') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0033 | system_requirement | approved | Indent a Kconfig entry and its help text as prescribed |
| SR-0034 | system_requirement | approved | Advertise a dangerous Kconfig option in its prompt |
<!-- tl:end -->

## Data Structures

<!-- tl:item UR-0010 -->
**UR-0010 — Data Structures** — `user_requirement`, status `approved`

> Rules governing reference counting of shared data structures.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Data Structures
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Data Structures') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0035 | system_requirement | approved | Reference-count a shared data structure |
<!-- tl:end -->

## Macros, Enums and RTL

<!-- tl:item UR-0011 -->
**UR-0011 — Macros, Enums and RTL** — `user_requirement`, status `approved`

> Rules governing macro and enum naming, do-while wrapping, parenthesisation and the pitfalls to avoid.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Macros, Enums and RTL
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Macros, Enums and RTL') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0036 | system_requirement | approved | Capitalise macro constants and enum labels |
| SR-0037 | system_requirement | approved | Wrap a multi-statement macro in do { } while (0) |
| SR-0038 | system_requirement | approved | Parenthesise macro arguments and expressions |
| SR-0039 | system_requirement | approved | Avoid macros with control flow or magic names |
<!-- tl:end -->

## Printing Kernel Messages

<!-- tl:item UR-0012 -->
**UR-0012 — Printing Kernel Messages** — `user_requirement`, status `approved`

> Rules governing spelling, conciseness and the dev_/pr_ message helpers.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Printing Kernel Messages
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Printing Kernel Messages') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0040 | system_requirement | approved | Keep kernel messages correctly spelt and concise |
| SR-0041 | system_requirement | approved | Use the dev_ and pr_ message helpers |
<!-- tl:end -->

## Allocating Memory

<!-- tl:item UR-0013 -->
**UR-0013 — Allocating Memory** — `user_requirement`, status `approved`

> Rules governing the preferred allocation idioms and not casting or double-reporting.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Allocating Memory
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Allocating Memory') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0042 | system_requirement | approved | Allocate against the pointer, not the spelt-out type |
| SR-0043 | system_requirement | approved | Do not cast the return of a void-pointer allocator |
<!-- tl:end -->

## The Inline Disease

<!-- tl:item UR-0014 -->
**UR-0014 — The Inline Disease** — `user_requirement`, status `approved`

> Rules governing restrained use of the inline keyword.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: The Inline Disease
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: The Inline Disease') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0044 | system_requirement | approved | Do not inline as a magic speed-up |
<!-- tl:end -->

## Function Return Values and Names

<!-- tl:item UR-0015 -->
**UR-0015 — Function Return Values and Names** — `user_requirement`, status `approved`

> Rules governing the error-code versus boolean return-value conventions.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Function Return Values and Names
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Function Return Values and Names') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0045 | system_requirement | approved | Return an error code from an action function |
| SR-0046 | system_requirement | approved | Return a boolean from a predicate function |
<!-- tl:end -->

## Using bool

<!-- tl:item UR-0016 -->
**UR-0016 — Using bool** — `user_requirement`, status `approved`

> Rules governing where bool improves readability and where it should be avoided.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Using bool
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Using bool') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0047 | system_requirement | approved | Prefer bool with true and false for boolean values |
| SR-0048 | system_requirement | approved | Avoid bool where layout or size matters |
<!-- tl:end -->

## Do Not Re-invent Kernel Macros

<!-- tl:item UR-0017 -->
**UR-0017 — Do Not Re-invent Kernel Macros** — `user_requirement`, status `approved`

> Rules governing reuse of existing kernel helper macros.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Do Not Re-invent Kernel Macros
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Do Not Re-invent Kernel Macros') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0049 | system_requirement | approved | Reuse existing kernel helper macros |
<!-- tl:end -->

## Editor Modelines and Other Cruft

<!-- tl:item UR-0018 -->
**UR-0018 — Editor Modelines and Other Cruft** — `user_requirement`, status `approved`

> Rules governing keeping editor configuration out of source files.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Editor Modelines and Other Cruft
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Editor Modelines and Other Cruft') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0050 | system_requirement | approved | Keep editor modelines out of source files |
<!-- tl:end -->

## Inline Assembly

<!-- tl:item UR-0019 -->
**UR-0019 — Inline Assembly** — `user_requirement`, status `approved`

> Rules governing when and how to write inline assembly.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Inline Assembly
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Inline Assembly') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0051 | system_requirement | approved | Use inline assembly only where C cannot do the job |
| SR-0052 | system_requirement | approved | Format and mark inline assembly correctly |
<!-- tl:end -->

## Conditional Compilation

<!-- tl:item UR-0020 -->
**UR-0020 — Conditional Compilation** — `user_requirement`, status `approved`

> Rules governing avoiding preprocessor conditionals in .c files.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Conditional Compilation
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Conditional Compilation') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0053 | system_requirement | approved | Avoid preprocessor conditionals in .c files |
| SR-0054 | system_requirement | approved | Use IS_ENABLED and __maybe_unused over |
<!-- tl:end -->

## Do Not Crash the Kernel

<!-- tl:item UR-0021 -->
**UR-0021 — Do Not Crash the Kernel** — `user_requirement`, status `approved`

> Rules governing panic, BUG, WARN and compile-time assertions.

*Derives from:* INT-0001

**source_ref**: Linux Kernel Coding Style: Do Not Crash the Kernel
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Linux Kernel Coding Style: Do Not Crash the Kernel') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0055 | system_requirement | approved | Reserve panic for unrecoverable boot failure |
| SR-0056 | system_requirement | approved | Prefer WARN_ON_ONCE to BUG |
| SR-0057 | system_requirement | approved | Warn only for should-never-happen situations |
<!-- tl:end -->

