# RLC Website

## Editing

Don't use Microsoft Word to edit the Markdown files. If on Windows, use WordPad or Notepad. If on Mac, use TextEdit.

Markdown reference: https://guides.github.com/features/mastering-markdown/

### Worship Times

Edit the file `data/worship.toml` and change the `time` property. e.g. `time = "8:30 and 10:45 AM"`

### Shortcodes

There are a few shortcodes that will insert content into your pages.

#### figure

The `figure` shortcode helps you insert images with (optional) captions and alt-tags onto your page.

##### Usage

`figure` can use the following named parameters:

* src
* link
* title
* caption
* class
* attr (attribution)
* attrlink
* alt

##### Example

Your images should be stored in `static/img`, so a simple image would be:

    {{< figure src="/img/my_image.jpg" alt="verbal description" >}}

An image with a caption would look like this:

    {{< figure src="/img/my_image.jpg" alt="verbal description" caption="Caption that displays below the image" >}}
	
#### worship_times

The `worship_times` shortcode will insert the current worship times into your content (e.g. "8:30 and 10:45 AM"). These times are defined in the `data/worship.toml` file.

##### Example

    {{< worship_times >}}

#### newsletter

The `newsletter` shortcode will insert a styled newsletter signup form onto your page.

##### Example

    {{< newsletter >}}


## Testing

	hugo serve -w

Open `http://localhost:1313` in your browser.

## Build

	hugo

## Deploy

	goapp deploy
