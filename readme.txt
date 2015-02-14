=== wBounce ===
Contributors: kevinweber
Donate link: http://kevinw.de/donate/wBounce/
License: MIT
Tags: admin, newsletter, exit popup, exit popups, ab-testing, roi, conversion, conversion rate optimisation, free, plugin, wordpress, marketing, landing page
Requires at least: 3.5
Tested up to: 4.1
Stable tag: 1.4.0.1

wBounce improves bounce rate to boost conversions and sales. The free alternative to Bounce Exchange for WordPress.

== Description ==
wBounce is the free exit popup software for WordPress, evolved by marketing technologist [Kevin Weber](http://kevinw.de). This plugin bases on [Ouibounce]( http://carlsednaoui.github.io/ouibounce/) by Carl Sednaoui.

Exit popups are not only "in vogue", they are provably increasing conversions and therefore boost marketing, signups and sales. wBounce displays an inline popup before the user leaves your site. ("Inline popup" means that this is NOT one of those out-dated, annoying popups windows.) Inline popups catch the visitor's attention even if they are in the process of leaving your site.

wBounce is the free alternative to charged services like Bounce Exchange or OptinMonster that are often used for landing page optimisation. wBounce is lightweight and renounces unnecessary scripts. You decide which features will be developed and implemented next.

One concern in everyone's interest: Make sure to provide VALUE when you use wBounce and don't spam your visitors.

This plugin makes it extremely easy to implement exit popups. You don't have to manually "hack" your WordPress theme. Just activate and modify it via your admin backend. It works with WordPress Multisite so that you can define a wBounce template for each site in your network.

Demo and more information on the developer's website: [kevinw.de/wbounce/](http://kevinw.de/wbounce/)

You want to enhance this plugin? Please [contribute on Github](https://github.com/kevinweber/wbounce). I'm looking for a WordPress enthusiast who further develops this plugin; I'll give you guidance and promote you and the plugin.

= Features: =
* Display inline popup before the user leaves the site
* Alternatively display popup on enter or after a certain time period (self-acting fire)
* Set custom content via backend
* Shortcodes are supported
* Determine sensitivity, cookie expiration, hesitation, and more
* Add custom CSS
* Set default status: Define if wBounce should be fired on posts and/or pages by default. You can override the default setting on every post and page individually.
* Event tracking with Google Analytics

= Future features: =
* Define custom content for pages and posts individually
* Templates with intelligent template variables/shortcodes
* Styling options (display "x" icon to close the popup, set background transparency, ...)
* Intelligent timer (e.g., display popup when the user is inactive for a certain time period)
* A/B testing with Google Analytics
* ... YOU want one of those features RIGHT NOW or want to implement a feature yourself? [Contribute on Github](https://github.com/kevinweber/wbounce) and I'll publish your enhancements to the official WordPress directory.


== Installation ==

1. Upload wBounce into you plugin directory (/wp-content/plugins/) and activate the plugin through the 'Plugins' menu in WordPress.
2. Configure the plugin via the admin backend and define your template. You can even insert shortcodes that are provided by your other plugins.
3. Optionally: Sign up to the wBounce newsletter to get notified about major updates.


== Frequently Asked Questions ==

= Does wBounce work with MailChimp, aWeber, GetResponse? =
Yes! You can use any form from every newsletter service since you can insert HTML code into the "wBounce content" text field. Simply copy the form code that's provided by MailChimp (or any other newsletter service) into the "wBounce content" text field.

Additionally, you can add CSS using the "Custom CSS" text field.

= How to use MailPoet, SendPress Newsletters and other plugins with wBounce? =
You can actually insert any shortcode that is provided by other plugins. For example, to use MailPoet with wBounce, simply insert the provided shortcode that contains the form's ID, as follows:  
`[wysija_form id="1"]`

By the way, [MailPoet](https://wordpress.org/plugins/wysija-newsletters/) allows to set up autoresponders, so give it a try.

Another well-known newsletter plugin, [SendPress](https://wordpress.org/plugins/sendpress/), offers shortcodes that look like this:
`[sp-form formid=18547]`

Notice: If a plugin or service doesn't offer such a shortcode, you can still insert any HTML code. I’m pretty sure that every useful newsletter service offers at least a piece of HTML code that works with wBounce :-)

= wBounce does not fire, scripts are not loaded or jQuery is loaded too late. What's wrong? =
Probably your theme does not implement the wp_footer() function in the appropriate position, if at all. Always have it just before the closing </body> tag of your theme. [#support](https://wordpress.org/support/topic/plugin-does-not-fire-the-popup?replies=3#post-6530865)

= How to use Jetpack's Subscriptions module with wBounce? =
Use Jetpack's shortcode within the wBounce content field:
`[jetpack_subscription_form]`
You can even extend the shortcode using modifiers as [explained by Jetpack](http://jetpack.me/support/subscriptions/).


== Changelog ==

= 1.4.0.1 =
* Improved CSS to hide scrollbars in some browsers. Note: To hide scrollbars in all browsers completely, use the following custom CSS: .wbounce-modal .wbounce-modal-sub { overflow: hidden; }

= 1.4 =
* New feature: Event tracking with Google Analytics.
* Extended "Default status" drop-down list with "Fire on posts and pages".
* Added 15% discount code for OptinMonster.

= 1.3.4.5 =
* Fixed not working cookieDomain.

= 1.3.4.4 =
* Fixed not working cookieExpire and cookieDomain.

= 1.3.4.3 =
* CSS fix.

= 1.3.4.2 =
* Fix: Make aggressive mode working as expected.

= 1.3.4 =
* Fix: Make cookie option work with self-acting fire.

= 1.3.3 =
* Fix: Improved self-acting fire. When self-acting fire fired, don't use exit popup again.
* Major CSS update: Removed fix height so that the content determines the modal's height. Default width is still 600px. When the modal's content requires more space than the screen is high, the modal is scrollable. Raised z-index from 1 to 21. Use CSS property "transform" to centre the modal vertically. Added margin to prevent the modal from being overlapped by the admin bar.
* New feature: Load script before footer. Normally, scripts are placed in <head> of the HTML document. If this parameter is true, the script is placed before the </body> end tag. This requires the theme to have the wp_footer() template tag in the appropriate place.
* Improvement: Use not minified JavaScript files when SCRIPT_DEBUG is true (defined in wp-config.php).
* Added version number to scripts.

= 1.3 =
* Renamed functions.php to wbounce.php. (This will cause your WordPress site to automatically deactivate wBounce. So you simply have to activate it again, that’s it.)
* New feature: Self-acting fire (timer). Automatically trigger the popup after a certain time period.
* New feature: Cookie domain.
* New: The cookie is stored for the whole site (and not only for specific pages/posts).
* New feature: Cookie per page. With this option enabled, every page/post gets its own cookie.
* Fix: Added CSS "box-sizing: border-box".
* Fix: Added CSS to make wBounce work with themes that use Bootstrap 3.

= 1.2.1 =
* Fixed broken post view.

= 1.2 =
* Improvement: Added support for shortcodes that are inserted into the "wBounce content" text area.
* New feature: Hesitation. wBounce waits x milliseconds before showing the model when the user's cursor leaves the window.
* Improvement: Only load scripts and CSS when they are actually needed.
* Improvement: Merged CSS from two files into one.
* Fixed "unexpected T_PAAMAYIM_NEKUDOTAYIM".

= 1.1.1 =
* New feature: Deactivate wBounce for pages and posts individually ("wBounce status").
* New feature: Define if wBounce should be fired on posts and/or pages by default.
* New feature: The wBounce status can be seen in an additional column on the overview for posts and pages.
* New feature: Sensitivity.
* New feature: Cookie expiration. wBounce sets a cookie by default to prevent the modal from appearing more than once per user. You can add a cookie expiration (in days) to adjust the time period before the modal will appear again for a user.
* wBounce is ready for WordPress 4.0.

= 1.0 =
* Plugin goes public.
* First available features: Admin panel to customise settings. Insert content/code + example template. Test mode. Aggressive mode. Timer. Custom CSS.


== Upgrade Notice ==

= 1.2.2 =
* Renamed functions.php to wbounce.php. This will cause your WordPress site to automatically deactivate wBounce. So you simply have to activate it again, that’s it.

= 1.0 =
* Plugin goes public.


== Screenshots ==

1. Screenshot of a site that uses wBounce.
2. Admin panel tab "content".
3. Admin panel tab "options".
4. Meta box besides post editor (v1.1).
5. Post column displays status (v1.1).