# django-compile-blog-comment-system
Github link: https://github.com/gurnitha/django-compile-blog-comment-system

## 01. Real World Project - Blog Application

#### 01.1 178. Section Overview
	pass

#### 01.2 179. Getting your template files
	pass


#### 01.3 180. Project setup

        modified:   README.md
        new file:   app/__init__.py
        new file:   app/admin.py
        new file:   app/apps.py
        new file:   app/migrations/__init__.py
        new file:   app/models.py
        new file:   app/tests.py
        new file:   app/views.py
        new file:   blogapp/__init__.py
        new file:   blogapp/asgi.py
        new file:   blogapp/settings.py
        new file:   blogapp/urls.py
        new file:   blogapp/wsgi.py
        new file:   manage.py


#### 01.4 181. Posts: Building model

        new file:   app/migrations/0001_initial.py
        modified:   app/models.py
        modified:   blogapp/settings.py


#### 01.5 182. Structuring templates
	pass


#### 01.6 183. Posts: views and templates

        new file:   app/templates/app/post.html
        modified:   app/views.py
        modified:   blogapp/settings.py
        new file:   templates/base.html


#### 01.7 184. Posts: URLs and viewing posts

        modified:   app/admin.py
        new file:   app/urls.py
        modified:   blogapp/settings.py
        modified:   blogapp/urls.py
        new file:   upload/images/post.png


#### 01.8 185. Configuring static files and render post

        new file:   app/static/app/style.css
        modified:   app/templates/app/post.html
        modified:   blogapp/urls.py
        modified:   templates/base.html

        
#### 01.9 186. Building the home page

        new file:   app/templates/app/index.html
        modified:   app/urls.py
        modified:   app/views.py


#### 01.10 187. Building Tags

        modified:   app/admin.py
        new file:   app/migrations/0002_tag_post_tags.py
        modified:   app/models.py
        modified:   app/templates/app/post.html

        Activities:

        1. Build Tag model
        2. Add relationship with Post model + related_name
        3. Run and applay migrations
        4. Register Tag to admin
        5. Add some tag in admin
        6. Open post + select tag/s
        7. Render tags to post.html

        NOTE: just a basics (not complete the post page yet)

        # IN THE TERMINAL

        F:\_workspace\blog\blog-comment-a-comment (main)
        (venv3941) λ REM: open shell

        ...
        >>> from app.blog.models import Post, Tag
        >>> posts = Post.objects.all()
        # show first post --> [0]
        >>> posts[0]
        <Post: Post object (1)>
        # show all tags belongs to post1
        >>> posts[0].tags.all()
        <QuerySet [<Tag: tag1>, <Tag: tag2>]>
        IN THE POST PAGE

        <div class="blog-tags">
            {% for tag in post.tags.all %}
              <div class="tag">{{tag.name}}</div>
            {% endfor %}
        </div>


#### 01.11 188. Recording views

        modified:   app/migrations/0002_tag_post_tags.py
        new file:   app/migrations/0003_post_view_count.py
        new file:   app/migrations/0004_alter_post_tags.py
        modified:   app/models.py
        modified:   app/templates/app/index.html
        modified:   app/templates/app/post.html
        modified:   app/views.py


#### 01.12 189. Allowing users to comment

        modified:   app/admin.py
        new file:   app/forms.py
        new file:   app/migrations/0004_comments.py
        new file:   app/migrations/0005_alter_post_tags.py
        renamed:    app/migrations/0004_alter_post_tags.py -> app/migrations/_0004_alter_post_tags.py
        modified:   app/models.py
        modified:   app/templates/app/post.html
        modified:   app/views.py


#### 01.13 190. Rendering comments

        modified:   app/templates/app/post.html
        modified:   app/views.py


#### 01.14 191. Fixing the submit issue on refresh

        modified:   app/views.py

        
#### 01.15 192. Building replies

        modified:   app/models.py
        new file:   app/static/app/url.js
        modified:   templates/base.html

        Note:

        1. After submiting the form:

        Forbidden (403)
        CSRF verification failed. Request aborted.

        NEXT: to replace the codes using my own codes

        
#### 01.16 193. Allowing users to leave a reply

        modified:   app/migrations/0001_initial.py
        new file:   app/migrations/0002_tag_post_tags.py
        new file:   app/migrations/0003_post_view_count.py
        new file:   app/migrations/0004_comments.py
        new file:   app/migrations/0005_comments_parent.py
        new file:   app/migrations/0006_alter_post_tags.py
        modified:   app/templates/app/post.html
        modified:   app/views.py

        
#### 01.17 194. Rendering replies
#### 01.18 195. Section Summary
