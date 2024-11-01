=== Singular ===
Tags: admin, slug, postname, permalink, singular, suffix, unique 
Contributors: majelbstoat

By default in Wordpress 1.5 and onwards, a post's sanitised name that appears in a permalink structure is checked for duplication and a numeral is appended if one is found. This is to prevent two posts having the same permalink, even when they have the same title. This could not be guaranteed otherwise, for instance because not all structures use a date to reference their archives.

In some permalink structures, this default behaviour is not desirable. Typically, these will be those that do incorporate a date or some other unique identifier. In these cases, a site author might wish to have the sanitised name the same for each post, for example in the case of a weekly report or column. Singular is a simple plugin which removes the extra suffix that Wordpress automatically adds when a post with a similar name is published.

== Installation ==

* One Click Installation is available, if you are using the Wordpress <a href="http://www.wp-plugins.net/">Plugins Manager</a>

Otherwise:

1. Upload singular.php to your plugins folder, usually `wp-content/plugins/`
2. Activate the plugin on the plugin screen.


== Frequently Asked Questions ==

= Huh? =

An example:

A post titled "A Witty Quote" for example, has a post slug (which is used in a post's permalink) of 'a-witty-quote'.  A second post titled "A wiTTy QUoTe" (or something similar) would have a post slug of 'a-witty-quote-2'.  If you want the second post slug to be 'a-witty-quote' instead of 'a-witty-quote-2', use this plugin.


= Is this useful for me? =

If you're asking, it probably isn't!  To be useful, the following should all be true:

1. You have a blog that uses a permalink structure incorporating the date, or some other unique path.
2. You write posts that have the same title (or that would sanitise to the same title) regularly.
3. You don't like the second and third posts having '-2' and '-3' appended.


= Will Singular re-write my post slug arbitrarily? =

No.  Singular merely repeats Wordpress' own method of creating a post slug.  That is, it takes the title of the post and sanitises it.  All Singular does is skip the code that checks for a duplicate that could possibly add a numeral suffix.


= Will this screw anything up? =

If you have a unique permalink structure similar to that described above, no.  However, the numeral is put there for a reason.  If you store archives by category, for example, and two posts in the same category have a similar title, both posts will resolve to the same permalink.  Which one will take priority is up to your .htaccess file.  Ensure you understand the implications of fiddling with your permalink structure before you run with this.  That said, it won't actually delete any posts, it just might make them hard to find...