# hexo-next-list-related-posts

A hexo plugin that generates a list of related posts on The Theme Next.

## Install

```sh
$ npm install hexo-next-list-related-posts --save
```

## Usage

In file `themes/next/layout/_macro/post.swig`, Add
```
      {% set related_post =  list_related_posts(post, {maxCount: 10, orderBy: 'date'}) %}
      {% if related_post.length > 0 %}
        <h3 class="article-title" style="font-size: 20px;">相关文章</h3>
        <ul class="related-posts">
        {% for rl_post in related_post %}
            <li class="related-posts-item"><a href="{{ url_for(rl_post.path) }}">{{ rl_post.title }}</a></li>
        {% endfor %}
        </ul>
      {% endif %}
```

