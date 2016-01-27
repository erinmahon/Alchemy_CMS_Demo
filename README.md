#Alchemy CMS Gem

What Alchemy CMS Accomplishes:

The Alchemy CMS Gem is a Content Management System (CMS) Framework for Rails. 

While Alchemy CMS has many powerful features, the overall accomplishment of the Gem is that it creates a user centric backend interface to the rails application.  It comes with an extreme flexible content storing architecture

Simple stated, it enables a web developer to create a custom website that can be maintained by a non-developer. The web developer is in full control of the website's features, markup and styling, and the end user actually manages the content of the site.

This easy to use and intuitive interface is a powerful tool. Some key features including an image gallery

1) Concept & Structure - Breakdown the Layout into Cells, Elements, and Essences

When working with Alchemy CMS the very first thing the webdeveloper conceptually does is splitting the website´s layout into different types (called page layouts).

Every page which is structurally different to other, should get its own page-layout. A page-layout is a html template with specified properties. More about PageLayouts »

After that the developer will look deeper to the content and will perhaps split the pages into cells. Cells can be rendered on page-layouts and are acting as containers for elements. More about Cells »

In any case the developer splits the content into elements. That means grouping the smallest parts of the website (the contents). Elements are containers for essences (called contents) and can be rendered on page-layouts or in cells. More about Elements »

A content is the smallest part in Alchemy and refers to one of the essence-types Alchemy CMS provides (EssenceText, EssencePicure, EssenceRichtext, …). More about Essences »

2) Define Cells & Elements
3) Definen Page Layout
4) Generate Partial Views for each Cell & Element
5) Customize Partial Views for each Cell & Element
6) Embed Cells & Elements into Layout Pages

How to Install the Alchemy CRM Gem:

Installation

The installing of Alchemy CMS is very easy. You just need to run the gem command.

gem install alchemy_cms

You now have the newest Alchemy CMS gem installed on your system!

3.1 Create a new application
The gem provides an executable file that can automagically create new rails applications with a pre-configured Alchemy CMS engine. While the installation process you will get asked about your local development environment. Just follow the instructions.

alchemy new YOUR_APP_NAME
The following parameters are available for the installer:

—database=sqlite3
—scm=git/svn

The installer creates a database, migrates the tables and also seeds them. After finishing, your application is ready to start!

3.2 Install into an existing Rails application
If you already have an existing Rails application, you can require the Alchemy CMS gem in your app.

Just add this line to your Gemfile.

gem 'alchemy_cms', '~>2.1'
Since Alchemy CMS is a mountable engine, you need to define the mountpoint in your config/routes.rb file.

MyApp::Application.routes.draw do
  mount Alchemy::Engine => '/'
end
You can mount Alchemy on every route you want. pages, cms, typo3, what ever you want. Most of the time you go with the root route.

Now you need to run bundler for installing the dependencies.

bundle install
It´s recommended to create the folders Alchemy CMS needs.

rails generate alchemy:scaffold
Copy the database migration files to your application.

rake alchemy:install:migrations
Migrate the database to get the table structure.

rake db:migrate
Seed the database with initial data.

rake alchemy:db:seed
You´re done! Alchemy is now available in your Rails project!

4 Running Alchemy CMS!

Now that you have Alchemy CMS successfully installed, let’s move on by creating your first user with administrative privilegs.

You just need to start a local ruby server on your development machine.

cd YOUR_APP_NAME && rails s
Open a browser window and navigate to http://localhost:3000. You will be greeted with a screen that is prompting you to create the first user.

Congratulations, you can now access the backend!
