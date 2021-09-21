# emojiPicker
A simple JQuery picker component for Unicode emoticons

emojiPicker is a very simple JQuery component for selecting unicode emoticons and inserting them into a text field.

The component is ideally associated with a button (or more generally with any clickable tag) and bound with a text field in which the emoji will be inserted.

When you click the associated button a div panel with the list of available emojis is displayed (below or over the button, aligned with its left or right side). From this panel you can click the emojis and they are inserted in/appended to the text field you have bound.

Here is a minimal example of use:

```javascript
$('#picker-button-id').emojiPicker('any-text-field-id');
```

The component is customizable by adding options:

```javascript
$('#picker-button-id').emojiPicker('any-text-field-id', {
  emojis: [ '&#x1F642;', '&#x1F641;', ... ],
  classes: 'border rounded',
  css: {
    background: '#E0E0FF',
    padding: '10px',
  },
  emojiCSS: {
    width: 'font-size: 24px',
    padding: '2px',
  },
  columns: 8,
  position: 'below-right'
});
```
The `emojis` option contains the list of emoji codes you want to display in the panel. The `classes` and `css` are classes and styles you want to add to the emoji panel, while `emojiCSS` is the list of styles which will be associated to any single emoji entry.
The panel will have `columns` columns and will be displayed below or over the button, aligned with its right or left side according with the `position` parameter. Possible values for `position` are:
- below-right (or bottom-right)

   The top-right corner of the panel is below the button, aligned with its right side.

- below-left (or bottom-left)

   The top-left corner of the panel is below the button, aligned with its left side.
   
- over-right (or top-right)

   The bottom-right corner of the panel is over the button, aligned with its right side.
   
- over-left (or top-left)

   The bottom-left corner of the panel is over the button, aligned with its left side.


