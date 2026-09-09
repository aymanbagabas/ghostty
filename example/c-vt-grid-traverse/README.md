# Example: `ghostty-vt` Grid Traversal

This contains a simple example of how to use the `ghostty-vt` terminal and
grid reference APIs to create a terminal, write content into it, and then
traverse the entire grid cell-by-cell using grid refs to inspect codepoints,
row state, styles, and hyperlinks.

The last two rows show the difference between a cell's hyperlink URI and
its hyperlink ID. Both rows link to the same URI, but only the first row
was written with an `id=` parameter. A link without `id=` gets an implicit
ID that the library does not expose, so
`ghostty_grid_ref_hyperlink_id()` reports `GHOSTTY_NO_VALUE` for it.

This uses a `build.zig` and `Zig` to build the C program so that we
can reuse a lot of our build logic and depend directly on our source
tree, but Ghostty emits a standard C library that can be used with any
C tooling.

## Usage

Run the program:

```shell-session
zig build run
```
