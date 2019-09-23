# Django-Blog
Repo for our Django Blog project

In this project, we will be creating a blog. This blog will be a multi user blog. The entire blog is created using ATOM text editor.
Environment name is MyDjangoEnv and django version used is 1.10. Python 3.5.2 is used. Using this blog, we can create new posts. There is an author field, title field and a text field. We also have drafts which are basically unpublished posts. we can edit this post later on. The published posts also have a comment field wherein anyone can post their comment and as a user we can approve or reject the comment.Our homepage "My Tech Blog" shows a list of all our published posts. On clicking on any of those posts, we get detailed description of that post along with comments which were approved. Using navbar, we have links to GitHub as well  as LinkedIn. We will call the project "mysite" and the application name is "blog". 

We created a class Post. Each blog post is going to connect to a model in our database. Another class called comment is created using which we can add comments to a post. 

After someone creates a post or comment, where should the website take them. We use detail views for post and function views for comment. The function has to be called get_absolute_url as Django looks for it.What it does is after we create a post and hit publication, we go to post_detail page for the primary key of the post we just created.We will do same in Comment class. Since a comment needs to be approved by a superuser, it does not makes sense to go back to a list of comments.Instead what we do is once a person is done writing a comment, they go back to a list of posts which is the home page.

After creating models, we create forms in forms.py folder. They simply represent our models in a proper form format. 

We create different class based and function based views in views.py file. They simplyadd functionality. The indicate what will happen if a particular action is performed.

Views are mapped to URLs. We take the MTV(Model Templates Views) approach. Templates basically contain the different html files and static folder contains the CSS and JS files.

After setting up everything, we register the models in admin.py file and create a superuser for admin access. Superuser credentials are, name: priyanka, password: p@21021994. Then we migrate to create a database and make sure everything is set up properly. Using the command "python manage.py runserver 8080", we get the url "http://127.0.0.1:8080/". Pasting it in our browser gives the application we created.


(MyDjangoEnv) C:\Users\PRIYANKA KUMARI\Desktop\Blog_Clone_Project\blog_project>python manage.py runserver 8080
Performing system checks...

System check identified no issues (0 silenced).
September 19, 2019 - 20:57:16
Django version 1.10.5, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8080/
Quit the server with CTRL-BREAK.
