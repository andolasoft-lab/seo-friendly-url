<h1>Generating SEO Friendly URL in Rails 3.x</h1>

SEO friendly URLs are more important to make a page popular & search engines to crawl. FriendlyId is the slugging and

permalink plug-in for Ruby on Rails. It allows you to create pretty URLs and work with human-friendly strings. The URLs created by slug are very useful for SEO. It is designed for generation of URL slug and history maintenance.

Steps to create Pretty URLs:

<h6>Step#1</h6>

Include gem in your Gem file:

<i>gem 'friendly_id'</i>

Then run bundle install.

<h6>Step#2</h6>

Modify your model on which you want the pretty URL:

<i>extend FriendlyId</i>
 
<i>friendly_id :title, use: :slugged</i>

<h6>Step#3</h6>

Add the slug column in your migration file to add it on the table

<i>add_column :articles, :slug, :string</i>

Then run

<i>rake db:migrate</i>

Now if you create an article with Title like “This is a demo title for testing”, it will create a SEO friendly URL like “this-is-a-demo-title-for-testing” and will save into the articles table under slug column.
