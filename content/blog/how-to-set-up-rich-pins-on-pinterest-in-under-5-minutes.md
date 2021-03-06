+++
categories = ["Pinterest Tips"]
date = "2019-06-04T00:00:00-04:00"
description = "Rich Pins help take Pinterest content marketing to the next level by pulling extra details from your website and exposing it on the pin. No matter the kind of content you are creating (eBooks, physical products, blog posts, recipes, DIY instructions, podcasts, etc), Pinterest is an essential platform to market your ideas for your business and rich pins are essential for marketing success. Learn how to set up rich pins and why they are so important. "
keywords = ["pinterest basics"]
title = "How to set up Rich Pins on Pinterest (in under 5 minutes)"
[images]
name = "How to set up rich pins on Pinterest (in under 5 minutes)"
src = "/uploads/richpins.png"
[[pins]]
pin_description = "How to set up rich pins for your business or blog to gain more traffic to your website.  Learn what rich pins are, what they look like, and why you need them. #richpins #pinterestmarketing #pinterestforbeginners #contentmarketing #digitalmarketing #bloggingforbeginners #seo #pinterest #blogging"
pin_image = "/uploads/how-to-setup-rich-pins-what-are-they.png"
[[pins]]
pin_description = "If you want to have the next viral pin, or just get repinned by other pinners, then you need to have rich pins enabled.  Learn how rich pins work, and why you need rich pins to be successful with your Pinterest Marketing. #richpins #pinterestmarketing #pinterestforbeginners #contentmarketing #digitalmarketing #bloggingforbeginners #seo #pinterest #blogging"
pin_image = "/uploads/why-you-need-rich-pins-to-go-viral.png"
[[pins]]
pin_description = "Your complete guide to Rich Pins on Pinterest. Learn what rich pins are, why you need them, and how to set them up for your business. If you aren't using rich pins, you are missing out on capturing your audiences attention! Activate them today!. #richpins #pinterestmarketing #pinterestforbeginners #contentmarketing #digitalmarketing #bloggingforbeginners #seo #pinterest #blogging"
pin_image = "/uploads/complete-guide-to-rich-pins.png"
[[pins]]
pin_description = "How to set up Rich Pins on Pinterest in 2 really simple steps. Rich Pins will improve the reach of your pins by exposing more details and keywords to your audience. This will help drive more traffic to your website. Learn how to set up Rich Pins - its really easy. #richpins #pinterestmarketing #bloggingforbeginners #seo #pinterest #blogging"
pin_image = "/uploads/how-to-setup-rich-pins-in-2-simple-steps.png"
[[pins]]
pin_description = "How to set up Rich Pins on Pinterest in under 5 minutes. Rich Pins supercharge your pins by bringing in contextual information from your website, making your Product Pins, Article Pins, Blog Pins, and Recipe Pins much more useful. This in turn will help drive more traffic to your website from your engaged audience. #richpins #blogtraffic #seo #pinterest #blogging"
pin_image = "/uploads/how-to-set-up-rich-pins.png"

+++
## What are Rich Pins?

Rich Pins are essentially a more enhanced version of a regular pin.  They will scour your website for extra information, and upgrade the look of your pin with all that wonderful information.

For example, if you have a recipe post, then details about your recipe such as the ingredients can be pulled right into the pin itself.

This has the effect of giving your potential audience more information to look at when they view your pin.  There are more details that can be indexed and searched on by users who search on Pinterest.  The net effect is it offers you more chances to get in front of your audience and drive traffic to your website or blog.

{{<imgproc "/uploads/richpin-article.png" Resize "600x" >}}Article Rich Pin{{</imgproc>}} {{<imgproc "/uploads/richpin-recipe.png" Resize "600x" >}}Recipe Rich Pin{{</imgproc>}}

As you can see in the two rich pins posted above, the article has meta data from the blog post pulled into it such as the page title/description, author, and published date.  Meanwhile, the recipe has the ingredients list pulled in.

This results in a more well rounded pin with the information your audience needs to see to make a decision on clicking through to the website.  The pin looks more professional and more engaging.  It will help your pin appear to more readers on Pinterest as the extra information helps feed the search terms that users search on (SEO).  And, the more people that get to see your pin, the better the chances of your pins going viral, leading to more traffic to your website.

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

#### 1. Set up your meta data

First you will need to set up your meta data on your posts so that Pinterest can scrape that information to display on your pins.

This follows the opengraph format, and essentially consists of you adding some `meta` tags to the `<head>` section of your html.

If you are using wordpress, then the [Yoast SEO](https://wordpress.org/plugins/wordpress-seo/ "Yoast SEO for Opengraph Tags") plugin is a popular choice to handle adding these tags for you.

If you want to add these yourself, then [http://ogp.me](http://ogp.me "http://ogp.me") has a good list of the types of meta tags to add to describe your content.

For example, if you look at the page source for this blog post, you should see something similar to below.  The meta data tags are targeted towards the Article type.

    <html>
    	<head>
        	...
            <meta property="og:title" content="How to set up Rich Pins on Pinterest (in under 5 minutes)">	    
            <meta property="og:type" content="article">
            <meta property="article:published_time" content="2019-06-04">
            <meta property="og:description" content="No matter the kind of content you are creating (eBooks, physical products, blog posts, recipes, DIY instructions, podcasts, etc), Pinterest is an essential platform to market your ideas for your business.  Rich Pins takes that marketing to the next level by pulling extra details from your website and exposing it on the pin. ">
            <meta property="og:url" content="https://www.thediyblogger.com/blog/how-to-set-up-rich-pins-on-pinterest-in-under-5-minutes/">
            <meta property="og:site_name" content="The DIY Blogger">
            <meta property="og:image" content="https://www.thediyblogger.com/uploads/richpins.png">
            <meta property="og:tags" content="pinterest-seo">
        	...
        </head>
        ...
    </html>

#### 2. Validate your page

Once you have your meta data set up and published live, the next step is to validate your page with Pinterest.  Visit the [Pinterest Rich Pins Validator](https://developers.pinterest.com/tools/url-debugger/ "Pinterest Rich Pin Validator") page and enter the full URL of your page that has the meta data added.

Pinterest will scan your page, and if it finds the meta data it will validate it and Rich Pins will be now enabled for your pins.  If there are problems with the meta data not being detected, then Pinterest will tell you there was an issue and you will need to check to see why the meta data is not there.