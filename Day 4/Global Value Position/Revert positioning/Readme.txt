The revert-layer keyword rolls back the value of a position property in a cascade layer to the property's value in a CSS rule matching the element in a previous cascade layer.

The property's value will be recalculated as if no rules were specified on the target element in the current cascade layer.

Note: This is an experimental global value. You need to check the browser compatibility for it to use in production code.

If there is no cascade layer to revert, the property value rolls back to the computed value derived from the current layer. Also, if there is no matching CSS rule, the property value will roll back to the style defined in the previous style origin.

One crucial difference to note between revert-layer and revert is that the latter lets us remove styles applied in the origin. If the revert-layer is set on a property outside a layer, then the value will roll back to the default established by the user agent's stylesheet.

@layer default {
  a { color: maroon; }
}

@layer theme {
  a { color: var(--brand-primary, purple); }
  
  .no-theme { color: revert-layer; }
}

In the example above, we are using the color property to show how the revert-layer works on the @layer rule. The link tag with the no-theme class will roll back to use the value set in the default layer. When revert-layer is used in un-layered styles above it, it behaves the same as revert.