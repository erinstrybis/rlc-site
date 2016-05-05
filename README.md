# RLC Website

![wercker status](https://app.wercker.com/status/b995a60bd9ed204ce1972656c84199cd/m/master "wercker status")

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

#### panorama

The `panorama` shortcode lets you insert a large image into your content. Width must be 960px or greater.

More info on how slope is used here: http://voormedia.com/blog/2012/11/responsive-background-images-with-fixed-or-fluid-aspect-ratios

##### Usage

Provide the URL, height and slope of the image:

    {{< panorama src="/img/panorama.jpg" height="300" slope="10" >}}
	
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


## Getting your computer up to speed

1. [Sign up for a free GitHub account](https://github.com/join). Make sure to verify your account by clicking the link in the email GitHub sends you.
2. Navigate to the [rlclakeview/rlc-site](https://github.com/rlclakeview/rlc-site) repository and create a fork by clicking on the Fork button in the top-right corner of the page
3. Download and install [GitHub Desktop](https://desktop.github.com)
4. Sign in to GitHub Desktop with the login information you created in step 1.
5. Go through the walk through on the basics of [GitHub Flow](https://guides.github.com/introduction/flow/)
6. Click the `+` button in the to-left, then click "Clone" and you should see the `rlc-site` repository underneath your username.
7. Download [the latest release of hugo](https://github.com/spf13/hugo/releases)

## Updating the site

1. Create a feature branch
2. Make changes
3. Test your changes
4. Commit your changes
5. Create a pull request
