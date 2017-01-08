---
title: Richard Kiene's Blog
---

<p><a href="https://github.com/richardkiene">GitHub</a></p>
<p><a href="https://twitter.com/shmeeny">Twitter</a></p>
<p><a href="https://keybase.io/shmeeny">Keybase</a></p>
<p><a href="https://www.linkedin.com/in/richard-kiene-bb235b5">LinkedIn</a></p>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
