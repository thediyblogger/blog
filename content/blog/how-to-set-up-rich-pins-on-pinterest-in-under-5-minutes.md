+++
categories = ["Pinterest"]
date = "2019-06-04T00:00:00-04:00"
description = "No matter the kind of content you are creating (eBooks, physical products, blog posts, recipes, DIY instructions, podcasts, etc), Pinterest is an essential platform to market your ideas for your business.  Rich Pins takes that marketing to the next level by pulling extra details from your website and exposing it on the pin. "
draft = true
pins = []
title = "How to set up Rich Pins on Pinterest (in under 5 minutes)"
[images]
name = "How to set up rich pins on Pinterest (in under 5 minutes)"
src = "/uploads/richpins.png"

+++
## What are Rich Pins?

Rich Pins are essentially a more enhanced version of a regular pin.  They will scour your website for extra information, and upgrade the look of your pin with all that wonderful information.

For example, if you have a recipe post, then details about your recipe such as the ingredients can be pulled right into the pin itself.

This has the effect of giving your potential audience more information to look at when they view your pin.  There are more details that can be indexed and searched on by users who search on Pinterest.  The net effect is it offers you more chances to get in front of your audience and drive traffic to your website or blog.

{{<imgproc "/uploads/richpin-article.png" Resize "600x" >}}Article Rich Pin{{</imgproc>}} {{<imgproc "/uploads/richpin-recipe.png" Resize "600x" >}}Recipe Rich Pin{{</imgproc>}} 

As you can see in the two rich pins posted above, the article has meta data from the blog post pulled into it such as the page title/description, author, and published date.  Meanwhile, the recipe has the ingredients list pulled in.

This results in a more well rounded pin with the information your audience needs to see to make a decision on clicking through to the website.  The pin looks more professional and more engaging.

There are currently 4 categories of Rich Pins:

* Apps
* Products
* Recipes
* Articles

#### Product Rich Pins

Product Rich Pins are essential for any business selling products.  Pins will be updated with contextual information around pricing information, availability, and where to buy the product.  This makes shopping much easier.

#### Recipe Rich Pins

Recipe Pins will give home chefs the information they need to decide whether or not to cook the exciting dish in front of them.  Recipe Pins will show ingredients, cooking time, and serving sizes.

#### Article Rich Pins

Article Pins pull in story headlines, descriptions, and author data. This helps pinners decide if the story resonates with them, encouraging them to save it for later or click through to read it.

#### App Rich Pins

App Pins are currrently (2019) only available on iOS devices.  They display information about the App, and include an `Install` button right there on the pin, allowing the user to install the app without having to leave Pinterest.

More information about Rich Pins can be found on the [Pinterest Blog](https://business.pinterest.com/en/rich-pins "Pinterest Rich Pins").

## How to Set Up Rich Pins

Setting up rich pins is very easy.  Start by visiting the [Pinterest Developer Portal](https://developers.pinterest.com/docs/rich-pins/overview/? "Pinterest Rich Pins - Developer Portal").

1. First you will need to set up your meta data on your posts so that Pinterest can scrape that information to display on your pins.  
     
   This follows the opengraph format, and essentially consists of you adding some `meta` tags to the `<head>` section of your html.  
     
   If you are using wordpress, then the [Yoast SEO](https://wordpress.org/plugins/wordpress-seo/ "Yoast SEO for Opengraph Tags") plugin is a popular choice to handle adding these tags for you.  
     
   If you want to add these yourself, then [http://ogp.me](http://ogp.me "http://ogp.me") has a good list of the types of meta tags to add to describe your content.
2. Once you have your meta data set up and published live, the next step is to validate your page with Pinterest.  Visit the [Pinterest Rich Pins Validator](https://developers.pinterest.com/tools/url-debugger/ "Pinterest Rich Pin Validator") page and enter the full URL of your page that has the meta data added.  
     
   Pinterest will scan your page, and if it finds the meta data it will validate it and Rich Pins will be now enabled for your pins.  If there are problems with the meta data not being detected, then Pinterest will tell you there was an issue and you will need to check to see why the meta data is not there.