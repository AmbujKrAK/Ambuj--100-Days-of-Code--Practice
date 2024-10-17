The revert keyword reverts the cascade value of the position property from its current value to the value the property would have had if no changes had been made to the current element.

This resets the property to its inherited value if it inherits from its parent or to the default value established by the user agent's stylesheet.

Note: This keyword removes all the styles from the cascade that have been overridden. It doesn't affect rules applied to the children of an element you reset.

div {
  position: absolute;
  background-color: orange
}

.div {
  position: revert;
  margin-top: 8px;
  padding: 50px
}

Here the div element is set to have an absolute position. Note that by default, this value is set to static. Now, as div.div's property is set to revert, therefore it resets the position properly from absolute to static.