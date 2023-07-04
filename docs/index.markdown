---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="posts-grid">
{% for post in site.posts %}
<a class="post-card" href="{{ post.url }}">
    <img src="{{ post.image }}">
    <h2>{{ post.title }}</h2>
</a>
{% endfor %}

<style>
    .posts-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        grid-gap: 20px;
        padding: 50px 50px;
    }

    .post-card {
        padding: 12px;
        margin-bottom: 10px;
        border-radius: 12px;
        background-color: #f5f5f5;
        text-decoration: none;
        transition: all 0.1s ease-in-out;
    }

    .post-card img {
        width: 100%;
        border-radius: 8px;
    }

    .post-card h2 {
        margin: 0;
        margin-top: 10px;
        padding: 0;
        font-size: 1.2rem;
        font-weight: 600;
        color: #333;
    }

    .post-card:hover {
        background-color: #e5e5e5;
    }
</style>
