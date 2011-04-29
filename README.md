Templates for Slide Show S9
===========================

Instructions at [github.com/geraldb/slideshow](https://github.com/geraldb/slideshow)

	gem install slideshow
	mkdir -p ~/.slideshow/templates
	git clone git@github.com:zeke/slideshow_templates.git ~/.slideshow/templates
	
Here's a rake task:

	task :preso => :environment do  
	  system "sass ~/.slideshow/templates/helvetica/ui/default/pretty.sass ~/.slideshow/templates/helvetica/ui/default/pretty.css"
	  system "slideshow -o ~/Projects/wordnik/sniphr/doc/slides -t helvetica.txt ~/Projects/wordnik/sniphr/doc/preso.md"
	  system "open ~/Projects/wordnik/sniphr/doc/slides/preso.html"
	end
