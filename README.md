#Alchemy CMS Gem

![alchemy_logo](https://cloud.githubusercontent.com/assets/14220315/12629971/25d36424-c518-11e5-9f42-69579a716d5d.png)

The Alchemy CMS Gem is a Content Management System (CMS) Framework for Rails. 

While Alchemy CMS has many powerful features, the overall accomplishment of the Gem is that it adds a user centric backend interface to rails web applications.  

Simply stated, it enables a web developer to create a custom website that can be maintained by a non-developer. The web developer is in full control of the website's features, markup and styling, and the end user actually manages the content of the site.

<h2>Front-End</h2>

<img width="1437" alt="screen shot 2016-01-27 at 5 11 10 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630184/47fc071c-c519-11e5-9cca-6f27812112ac.png">

<h2>Back-End</h2>
This easy to use and intuitive interface is a powerful tool. 

<img width="1377" alt="screen shot 2016-01-27 at 5 10 11 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630121/ded76a9c-c518-11e5-8ac6-faadf1ac8342.png">

<h3>Some Key User Interface Features Include:</h3>
<hr>

<h4>Library for Images & Files</h4>

<img width="1439" alt="screen shot 2016-01-27 at 5 19 24 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630442/6946661e-c51a-11e5-8a91-f9c7aef5a827.png">

<h4>Easy & Clear Navigation</h4>

<img width="1438" alt="screen shot 2016-01-27 at 5 20 11 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630453/7de470a2-c51a-11e5-975d-eb1011ff3116.png">

<h4>Simple Content Generation Features</h4>

<img width="1436" alt="screen shot 2016-01-27 at 5 20 29 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630469/9834427a-c51a-11e5-92eb-e65bca743b00.png">

<h3>Some Valuable Development Features Include:</h3>
<hr>

<ul>
<li><strong>Flexible Storing Architecture</strong>- Alchemy stores content. Unlike many other CMS’s that store a whole page body with complete html markup, Alchemy only stores unformatted text, ids of objects (like attachments and pictures) and only some richtext content in the database. No html markup, no css, no styling, no layout. Just pure content.</li><br>
<li><strong>Partial Rendering</strong> - Alchemy strongly uses the Rails partial rendering mechanism. It has no own templating language and no special files.</li>
</ul>

<h2>The General Process for Developers</h2>
<hr>
<ol>

<li><h4>Concept & Structure - Breakdown the Layout into Cells, Elements, and Essences</h4></li>

![alchemycms_core_concepts](https://cloud.githubusercontent.com/assets/14220315/12630752/ee70a272-c51b-11e5-8677-3c641aa3cfc6.png)

When working with Alchemy CMS the very first thing the webdeveloper conceptually does is splitting the website´s layout into different types (called page layouts). Every page which is structurally different to other, should get its own page-layout. A page-layout is a html template with specified properties.

<h4>Define Cells, Elements & </h4>

After that the developer will look deeper to the content and will perhaps split the pages into cells. Cells can be rendered on page-layouts and are acting as containers for elements. More about <a href="http://guides.alchemy-cms.com/edge/cells.html">Cells</a>

In any case the developer splits the content into elements. That means grouping the smallest parts of the website (the contents). Elements are containers for essences (called contents) and can be rendered on page-layouts or in cells. More about <a href="http://guides.alchemy-cms.com/edge/elements.html">Elements</a>

A content is the smallest part in Alchemy and refers to one of the essence-types Alchemy CMS provides (EssenceText, EssencePicure, EssenceRichtext, …). More about <a href="http://guides.alchemy-cms.com/edge/essences.html">Essences</a>

<h4>Define Page Layout</h4>

Every page which is structurally different to other, should get its own page-layout. A page-layout is a html template with specified properties. More about <a href="http://guides.alchemy-cms.com/edge/page_layouts.html">PageLayouts</a>

A content is the smallest part in Alchemy and refers to one of the essence-types Alchemy CMS provides (EssenceText, EssencePicure, EssenceRichtext, …). More about <a href="">Essences</a>

<h4> Generate Partial Views for each Cell & Element </h4>
<h4> Customize Partial Views for each Cell & Element </h4>
<h4> Embed Cells & Elements into Layout Pages </h4>

<h1>How to Install the Alchemy CRM Gem:</h1>

<h3>Installation</h3>

The installing of Alchemy CMS is very easy. You just need to run the gem command.

<strong>$ gem install alchemy_cms</strong>

You now have the newest Alchemy CMS gem installed on your system!

<h4>Create a New Application</h4>
<hr>

The gem provides an executable file that can automagically create new rails applications with a pre-configured Alchemy CMS engine. While the installation process you will get asked about your local development environment. Just follow the instructions.

<strong>$ alchemy new YOUR_APP_NAME</strong>

The installer creates a database, migrates the tables and also seeds them. After finishing, your application is ready to start!

<h4>Install into an Existing Rails Application</h4>
<hr>
If you already have an existing Rails application, you can require the Alchemy CMS gem in your app.

Add these Gems to Gemfile:

	gem 'alchemy_cms'
	gem 'alchemy-devise'

Since Alchemy CMS is a mountable engine, you need to define the mountpoint in your config/routes.rb file.

	MyApp::Application.routes.draw do
 	   mount Alchemy::Engine => '/'
	end

You can mount Alchemy on every route you want. Most of the time you go with the root route.

<strong>$ bundle install</strong> - Run bundler for installing the dependencies.

<strong>$ rails generate alchemy:scaffold</strong> - Create the folders Alchemy CMS needs.

<strong>$rake alchemy:install:migrations</strong> - Copy the database migration files to your application.

<strong>$rake db:migrate</strong> - Migrate the database to get the table structure.

<strong>$rake alchemy:db:seed</strong> - Seed the database with initial data.

You´re done! Alchemy is now available in your Rails project!

<h4>Running Alchemy CMS!</h4>
<hr>

With Alchemy CMS successfully installed, you can create your first user with administrative privilegs.

<strong>$ cd YOUR_APP_NAME && rails s</strong> - Move into folder and start locatal ruby server.

Open a browser window and navigate to <a href="http://localhost:3000">http://localhost:3000</a> 

You will be greeted with a screen that is prompting you to create the first user.

<img width="1329" alt="screen shot 2016-01-27 at 11 13 45 am" src="https://cloud.githubusercontent.com/assets/14220315/12630059/919fb9aa-c518-11e5-85f4-85e88d0fb609.png">

<h3>Congratulations, you can now access the backend!</h3>

<img width="797" alt="screen shot 2016-01-27 at 5 07 08 pm" src="https://cloud.githubusercontent.com/assets/14220315/12630082/ae27ed72-c518-11e5-9427-850c21199edc.png">

<h2>Resources</h2>
<a href"http://guides.alchemy-cms.com/edge/index.html">Alchemy CMS Guide</a>
<a href="https://github.com/AlchemyCMS/alchemy_cms">Alchemy CMS GitHub</a>