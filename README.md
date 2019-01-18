The DIY Blogger blog (based on Hugo Static Site Generator)

Running Locally
----------------

```$ hugo server -D```


Adding a new Blog Post
----------------------

```$ hugo new blog/title-of-my-post.md```

Then edit the post and add the content from within the `/content/blog` folder.

Any images for your blog post should be added to the `/static/images` folder.


Saving and Publishing your updates
-----------------------

from the /blog folder, run the following:

``` 
$ git status
```

add any new files added:

```
$ git add <filepath>
```

save your changes
```
$ git commit -a -m "<what you changed>"
$ git push
```

deploy all latest updates
```
$ ./deploy.sh 
```


Viewing your updates live
-------------------------

Once the deploy script has run, the website should update within a few seconds.

Go to https://www.thediyblogger.com/ to view the latest published website.


