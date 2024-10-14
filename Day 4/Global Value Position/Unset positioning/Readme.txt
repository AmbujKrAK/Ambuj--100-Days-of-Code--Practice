The unset keyword resets a position property to its inherited value if the property naturally inherits from its parent and to its initial value if not.

It behaves differently on inherited and non-inherited properties. When the unset value is set on inherited property, it resets the property value to its inherited value. On the other hand, it resets a non-inherited property to its initial value.

Hence, the unset behaves like the inherit keyword for inherited property and like initial for the non-inherited property.

.div {
  margin-top: 8px;
  padding: 50px;
  position: unset;
}

Here we are setting the position value to be unset, which in itself is an inherited property. So, it will behave like a inherit keyword here, causing it to have a static positioning.