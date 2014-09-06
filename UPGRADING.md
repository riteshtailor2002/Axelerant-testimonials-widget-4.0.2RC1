# Upgrade Notices - Testimonials by Aihrus

## 3.0.0

* This is a major overhaul *without* backwards compliance. If you use custom CSS, actions, or filters to modify Testimonials by Aihrus and Testimonials Premium actions or output, this 3.0 upgrade will not be compatible with those modifications until corrections are made. Please read [Testimonials by Aihrus and Testimonials Premium 3.0.0 Upgrade Notice](https://aihrus.zendesk.com/entries/52514055) for more help.

## 2.19.9

* Added `margin-bottom: 2em;` to `.testimonials-widget-testimonial.list`

## 2.19.8

* Cite fields for company and location are swapped

## 2.19.6

* Enable Video also means enable video embedding and display

## 2.19.0

* CSS class `.title` is now `.job-title`. Thank you Mark
* Please resave your WordPress Admin > Testimonials > Settings so that missing aoptions are included again.
* Shortcode and theme function `testimonialswidget_list` being deprecated by `testimonials`
* Shortcode and theme function `testimonialswidget_widget` being deprecated by `testimonials_slider`

## 2.18.3

* CSS class `.hide` renamed `.display-none`
* This is the last version supporting pre-bxSlider options

## 2.18.2

* CSS class `.display-none` renamed `.hide`

## 2.18.1

* CSS is back to being always loaded in the header
* Removed "Use bxSlider?" and "Include IE7 CSS" from widget options

## 2.18.0

* `remove_hentry` is now true by default

## 2.16.0

* [Requires PHP 5.3+](https://aihrus.zendesk.com/entries/30678006)

## 2.15.0

* If upgrading, bxSlider will not be enabled by default. You must enable it in your widget and global settings. CSS customizations must be reviewed to have the `.active` and `.display-none` classes removed. The main `.testimonials-widget-testimonial` class also need the `display: none;` and `clear: left;` removed.

## 2.14.0

* **60 modifications** See [Changelog](https://github.com/michael-cannon/testimonials-widget/blob/master/CHANGELOG.md)
* CSS wp_register_style and wp_enqueue_style slug changed from 'testimonials-widget' to 'Testimonials_Widget'
* Gravatar image size now based upon Thumbnail size in Media Settings
* Scripts `ksort` removed. Use `array_unshift` in your `testimonials_widget_testimonials_js` filters instead.
* Testimonials > Settings, General tab, option Enable Review Schema? is enabled by default.

## 2.13.6

* IE 7 CSS moved to separate file. Include via Testimonials > Settings if needed

## 2.12.0

* CSS and JavaScript renaming
	* `bottom_text` renamed to `bottom-text`
	* `close_quote` renamed to `close-quote`
	* `display_none` renamed to `display-none`
	* `join_location` renamed to `join-location`
	* `join_title` renamed to `join-title`
	* `open_quote` renamed to `open-quote`
	* `testimonialswidget_testimonial` renamed to `testimonials-widget-testimonial`
	* `testimonialswidget_testimonials` renamed to `testimonials-widget-testimonials`

## 2.11.3

* Correct filter name `testimonials_widget_next_posts_link` to `testimonials_widget_next_posts_link_text`

## 2.11.0

* CSS class names are simplified. For the most part, other than `testimonialswidget_testimonial` remove `testimonialswidget_` from the CSS class name in your CSS customizations.
	* Ex: `.testimonialswidget_join` becomes `.join`
	* Ex: `.testimonialswidget_author` becomes `.author`
* Testimonials are now formatted using `blockquote` than `q` for HTML5 compliance. If you need `q` tag formatting, enable it at WP Admin > Testimonials > Settings, Compatibility & Reset tab
	* `cite` is now `div.credit`

## 2.8.0

* Deprecated
	* `hide_author` now `hide_source`
* Removed filters `testimonials_widget_options_update`, `testimonials_widget_options_form`
	* Use `testimonials_widget_validate_settings` and `testimonials_widget_settings` instead
* Renamed variable and related class `widget_text` to `bottom_text`

## 2.7.3

* Quotes are no longer handled via `q`, `p:before`, or `p:after` CSS. It's handled via `.testimonialswidget_testimonial .testimonialswidget_open_quote:before` and `.testimonialswidget_testimonial .testimonialswidget_close_quote:after`
* This change was made to keep consistency in how quotes were managed and to reduce the number of exception cases. In the end, this is simpler.

## 2.7.0

* Quotes with `keep_whitespace=true` aren't applied via CSS `.testimonialswidget_testimonial q` tag anymore, but `.testimonialswidget_testimonial q p:first-child:before` and `.testimonialswidget_testimonial q p:last-child:after`
* Widget testimonial `p` tags are no longer CSS `display: inline`, `display: block` as expected

## 2.4.1

* Paging is on by default, except for widgets

## 2.0.0

* CSS
	* Class `testimonialswidget_company` replaces `testimonialswidget_source`
	* Class `testimonialswidget_source` replaces `testimonialswidget_author`
	* The tighten widget display up, p tags within q are displayed inline.
* JavaScript
	* The JavaScript for rotating testimonials is moved to the footer. As such, your theme requires `wp_footer()` in the footer.
* Shortcode options
	* `hide_source` replaced by `hide_url`
	* `hide_author` replaced by `hide_source`
* Testimonials
	* Migration from the old custom table to new custom post type is automatically done. Import might take a few moments to complete.
	* Company, URL and email details are attempted to be identified and placed properly based upon the original author and source fields. The company is "guessed" from the `author` field when there's a ", " or " of " context. If the `source` is an email, it's saved as such. Otherwise, it's assumed to be a URL.
	* Public testimonials are saved as Published. Non-public testimonials are marked as Private.
* Widget options
	* "Show author" and "Show source" options are replaced by "Hide source" and "Hide URL" respectively. There's no backwards compatibility for these changes. 
	* Default `min-height` is now 250px than 150px.

## Background

Version 2.0.0 of Testimonials is a complete rewrite based upon a composite of ideas from user feedback and grokking the plugins [Imperfect Quotes](http://www.swarmstrategies.com/imperfect-quotes/), [IvyCat Ajax Testimonials](http://wordpress.org/extend/plugins/ivycat-ajax-testimonials/), [Quotes Collection](http://srinig.com/wordpress/plugins/quotes-collection/), and [TB Testimonials](http://travisballard.com/wordpress/tb-testimonials/). Thank you to these plugin developers for their efforts that have helped inspire this rewrite.

Prior to version 2.0.0, this plugin was a fork of [Quotes Collection](http://srinig.com/wordpress/plugins/quotes-collection/) by [Srini G](http://wordpress.org/support/profile/SriniG) with additional contributions from [j0hnsmith](http://wordpress.org/support/profile/j0hnsmith), [ChrisCree](http://wordpress.org/support/profile/ChrisCree) and [comprock](http://wordpress.org/support/profile/comprock).