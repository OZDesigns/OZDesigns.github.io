# The `_posts` folder

This folder contains the blog posts that are ultimately published to your Web site's blog. Whenever you save a new file into this folder, Jekyll checks to see if it "looks like" a blog post. If it does, Jekyll creates a new page on your website for the blog post, and automatically adds the post to the many blog-aware listing pages.

For Jekyll to recognize a file in this folder as a blog post, each file must meet the following criteria:

* Its file name must be formatted like this:
  ```
  YYYY-MM-DD-slug.md
  ```
  For example, a file called `2018-05-28-my-first-post.md` will create a blog post published on May 5<sup>th</sup>, 2018 whose title is "My First Post." The `.md` at the end tells Jekyll that you intend to write the post using [Markdown](https://daringfireball.net/projects/markdown/), but you can also use a `.html` extension if you wanted to write in raw HTML, yourself.
* The file must begin with [Jekyll Front Matter](https://jekyllrb.com/docs/frontmatter/). Specifically, it must start with three dashes, then a newline, then another three dashes, like this:
  ```
  ---
  ---

  Your blog post body here.
  ```
  Inside the lines with three dashes on them, you can add any number of [custom fields](#custom-fields) (i.e., blog post metadata) to the blog post. However, even if you don't add any custom fields, you must include the front matter (the two lines of dashes) in order for Jekyll to recognize your file as a blog post.

See also [Jekyll's documentation for writing posts](https://jekyllrb.com/docs/posts/).

## Custom fields

Your blog posts can have custom metadata attached to them. This lets you do things like add a featured image to represent the main point of the post visually, set a title different than the one in the file name, change the publication date, include an author's byline, and more.

Custom fields must be written inside the Jekyll Front Matter block (between the lines with only three dashes on them) at the very start of the file. To add a custom field, you write the field's name, followed by a colon (`:`), followed by a single space, followed by the value you want. If the value you want includes a colon (`:`), you must enclose the value in double quotes. For example, to set a custom metadata field called `my_custom_metadata` with a value of `Special event: Dance of the Ages!`, you would add a line like this within the Front Matter portion of your blog post:

```yaml
my_custom_metadata: "Special event: Dance of the Ages!"
```

The rest of this section describes the custom fields that come built-in with your website's template.

### `featured`

Use the `featured` custom field to showcase a specific blog post in a prominent place on your Website, such as your home page. The only valid value is `true`.

### `image`

If you have already uploaded an image to [your site's `static/images` folder](../static/images/), you can use it as the featured image for this post by writing its filename as the `image` custom field. For example, assuming an image whose file name is `karaoke-event-poster.jpg` exists in [your site's `static/images` folder](../static/images/README.md), use this custom field value to make that image the featured image for this post:

```yaml
image: "karaoke-event-poster.jpg"
```

### `title`

Set this custom field to override the title of your post that was automatically generated from the post's filename.
