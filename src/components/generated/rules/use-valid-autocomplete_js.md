**Since**: `vnext`
:::caution
This rule is part of the [nursery](/linter/rules/#nursery) group.
:::

Sources: 
- Same as: <a href="https://github.com/jsx-eslint/eslint-plugin-jsx-a11y/blob/main/docs/rules/autocomplete-valid.md" target="_blank"><code>jsx-a11y/autocomplete-valid</code></a>

Use valid values for the `autocomplete` attribute on `input` elements.

The HTML autocomplete attribute only accepts specific predefined values.
This allows for more detailed purpose definitions compared to the `type` attribute.
Using these predefined values, user agents and assistive technologies can present input purposes to users in different ways.

## Examples

### Invalid

```jsx
<input type="text" autocomplete="incorrect" />
```

<pre class="language-text"><code class="language-text">code-block.jsx:1:20 <a href="https://biomejs.dev/linter/rules/use-valid-autocomplete">lint/nursery/useValidAutocomplete</a> ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

<strong><span style="color: Orange;">  </span></strong><strong><span style="color: Orange;">⚠</span></strong> <span style="color: Orange;">Use valid values for the </span><span style="color: Orange;"><strong>autocomplete</strong></span><span style="color: Orange;"> attribute.</span>
  
<strong><span style="color: Tomato;">  </span></strong><strong><span style="color: Tomato;">&gt;</span></strong> <strong>1 │ </strong>&lt;input type=&quot;text&quot; autocomplete=&quot;incorrect&quot; /&gt;
   <strong>   │ </strong>                   <strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong>
    <strong>2 │ </strong>
  
<strong><span style="color: lightgreen;">  </span></strong><strong><span style="color: lightgreen;">ℹ</span></strong> <span style="color: lightgreen;">The autocomplete attribute only accepts a certain number of specific fixed values.</span>
  
<strong><span style="color: lightgreen;">  </span></strong><strong><span style="color: lightgreen;">ℹ</span></strong> <span style="color: lightgreen;">Follow the links for more information,
</span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;"><a href="https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose">WCAG 1.3.5</a></span><span style="color: lightgreen;">
</span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;"><a href="https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill">HTML Living Standard autofill</a></span><span style="color: lightgreen;">
</span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;">  </span><span style="color: lightgreen;"><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete">HTML attribute: autocomplete - HTML: HyperText Markup Language | MDN</a></span>
  
</code></pre>

### Valid

```jsx
<>
  <input type="text" autocomplete="name" />
  <MyInput autocomplete="incorrect" />
</>
```

## Options

```json
{
    "//": "...",
    "options": {
        "inputComponents": ["MyInput"]
    }
}
```

## Accessibility guidelines

- [WCAG 1.3.5](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose)

### Resources

- [HTML Living Standard autofill](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill)
- [HTML attribute: autocomplete - HTML: HyperText Markup Language | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete)

## Related links

- [Disable a rule](/linter/#disable-a-lint-rule)
- [Configure the rule fix](/linter#configure-the-rule-fix)
- [Rule options](/linter/#rule-options)