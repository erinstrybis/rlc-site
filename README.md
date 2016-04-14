# RLC Website

## Editing

Don't use Microsoft Word to edit the Markdown files. If on Windows, use WordPad or Notepad. If on Mac, use TextEdit.

Markdown reference: https://guides.github.com/features/mastering-markdown/

### Worship Times

Edit the file `data/worship.toml` and change the `time` property. e.g. `time = "8:30 and 10:45 AM"`

### Shortcodes

There are a couple of shortcodes that will insert content into your pages.

    {{< worship_times >}}

This will insert the current worship times (e.g. 8:30 and 10:45 AM) as set in the configuration above.

    {{< newsletter >}}

This will insert a styled newsletter signup form.

## Testing

	hugo serve -w

Open `http://localhost:1313` in your browser.

## Build

	hugo

## Deploy

	goapp deploy
