<script lang="ts">
  type StackAlign =
    | "normal"
    | "stretch"
    | "center"
    | "start"
    | "end"
    | "flex-start"
    | "flex-end"
    | "baseline"
    | "first baseline"
    | "last baseline"
    | "safe center"
    | "unsafe center"
    | "inherit"
    | "initial"
    | "revert"
    | "revert-layer"
    | "unset"

  type StackJustify =
    | "center"
    | "start"
    | "end"
    | "flex-start"
    | "flex-end"
    | "left"
    | "right"
    | "normal"
    | "space-between"
    | "space-around"
    | "space-evenly"
    | "stretch"
    | "safe center"
    | "unsafe center"
    | "inherit"
    | "initial"
    | "revert"
    | "revert-layer"
    | "unset"

  export let direction: "row" | "column" = "row"
  export let align: StackAlign = "normal"
  export let justify: StackJustify = "normal"

  let compiledStyle = `
  flex-direction: ${direction};
  align-items: ${align};
  justify-content: ${justify};
  `
</script>

<div style={compiledStyle}>
  <slot />
</div>

<style>
  div {
    display: flex;
  }
</style>
