# Tail Action

Github Action to retrieve the last n lines of a file or string.

## Inputs

### `path`

The filepath to retrieve lines from. Must provide a path or a string..

### `string`

The string to retrieve lines from. Must provide a path or a string.

### `line-count`

The number of lines to retrieve.

## Outputs

### `content`

The retrieved lines.

## Example usage

```yaml
- uses: scribd/tail-action@v1
  id: tail
  with:
    path: xcode-build.log

- run: echo "${{ steps.tail.outputs.content }}"
```

More examples [here](https://github.com/scribd/tail-action/blob/master/.github/workflows/test.yml).