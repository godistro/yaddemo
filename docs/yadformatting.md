# YAD Dialog Formatting

There is nothing in this guide that cannot be easily discovered with some experimentation,
but showing some examples will save some time.

## Dialog Width

The width of a dialog is, initially, determined by the width of certain elements of the
dialog. YAD will stretch the dialog to contain the dialog buttons and the dialog text
(set with the `--text` option).  There is also an option, `--width` that can be used to
set a minimum width in case the buttons or the text are missing or too short to result
in a pleasing format.

One option that **does not** affect the dialog width is the `--title` option, which sets
the caption bar text.  Instead, the title will be truncated to fit if the dialog is not
wide enough to contain the title.

At least two things (I may be missing others) determine the width of a dialog, the
`--width` option and the `--text` option.  The `--width` option is works as expected, but the
`--text` was a surprise, coming from HTML development.

The dialog will expand horizontally to contain the contents of the `--text` option.
If the text is set to a very long string without any newlines, the dialog will be rendered
wide enough to contain the text.

**Use newlines in --text options to create a pleasing format.**

Find the examples of a long text option, with and without incorporated newlines, at
- *main* -> *YAD Dialog Formatting* -> *YAD Too Long*, and
- *main* -> *YAD Dialog Formatting* -> *YAD Just Right*.

## YAD Borders

I had expected the `--borders` option to create a thick border around the dialog, but, instead,
the `--borders` option creates space between the dialog's border and its contents.  It behaves
like the CSS *padding* property.

Find an example of the formatted text dialog with borders to make a nicer dialog:

- *main* -> *YAD Dialog Formatting* -> *YAD Just Right, Loosened*