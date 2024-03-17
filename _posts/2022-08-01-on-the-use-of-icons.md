---
layout: post
title: On the use of icons
lead: A very quick guide.
---

The icons used throughout this theme are partly custom-made, and partly come from the [Iconoir](https://iconoir.com/) library. More can be created or downloaded from the Iconoir website as svg files, and saved in `assets/svg` for use in your website.

Here's an overview of icons that already ship with the theme.

<table class="table">
  <thead>
    <tr>
      <th>Software Developer II</th>
      <th class="time">07/2021 - Present</th>
    </tr>
    <tr>
      <th colspan="2">Software Developer II</th>
    </tr>
  </thead>
</table>
- Ut enim ad minim veniam
- Quis nostrud exercitation
- Ullamco laboris nisi
- Ut aliquip ex ea commodo consequat

<table class="table">
  <thead>
    <tr>
      <th>Software Developer II</th>
      <th class="time">07/2021 - Present</th>
    </tr>
    <tr>
      <th colspan="2" class="location">LawDepot</th>
    </tr>
  </thead>
</table>
- Ut enim ad minim veniam
- Quis nostrud exercitation
- Ullamco laboris nisi
- Ut aliquip ex ea commodo consequat

They can be used in two ways through Liquid tags. First, as simple glyphs for decorative purposes, as in the table above or in the [contact](/cv) section of the CV:

{% highlight text %}
{% raw %}{% include svg/github.svg %}{% endraw %}
{% endhighlight %}

Second, as links:

{% highlight text %}
{% raw %}{% include iconlink.html icon="svg/github.svg" href="https://github.com/" %}{% endraw %}
{% endhighlight %}

In this case, the icon shows up with link formatting and its stroke width slightly increases on hovering. Here is an example: {% include iconlink.html icon="svg/github.svg" href="https://github.com/" %}

Simple CSS allows you to modify many aspects of the icon's appearance, including stroke width, color (with the `stroke` property), and size (with `transform`). Here is a usage example:

{% highlight css %}
svg {
/_ 250% of its original size _/
transform: scale(2.5);
}
svg path {
/_ red color _/
stroke: red;
/_ thinner line _/
stroke-width: 1.25;
}
{% endhighlight %}

## Note

Each icon available from Iconoir is essentially a text file:

{% highlight text %}

<?xml version="1.0" encoding="UTF-8"?><svg width="24px" height="24px" stroke-width="1.5" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#000000"><path d="M16 22.027v-2.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7a5.44 5.44 0 00-1.5-3.75 5.07 5.07 0 00-.09-3.77s-1.18-.35-3.91 1.48a13.38 13.38 0 00-7 0c-2.73-1.83-3.91-1.48-3.91-1.48A5.07 5.07 0 005 5.797a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7a3.37 3.37 0 00-.94 2.58v2.87M9 20.027c-3 .973-5.5 0-7-3" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></svg>

{% endhighlight %}

The `<?...?>` tag at the beginning is useful for apps but not for a Jekyll website, and will sometimes show up as a string of text, so it needs to be deleted. This has already been done for the default icons, but remember to do it also for every additional icon you download.
