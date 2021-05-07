Documentation regarding products from https://iwasz.com
Work in progress

# Links
* Theme used : [Just The Docs](https://pmarsceill.github.io/just-the-docs/)

# Jekyll / Ruby oddities
After some time, I was unable to build this website even though Travis accepted it happily.

I've added `gem "webrick"` to the Gemfile as suggested [here](https://github.com/jekyll/jekyll/issues/8523). It was to solve the `/home/iwasz/workspace/website-docs/vendor/bundle/ruby/3.0.0/gems/jekyll-4.0.1/lib/jekyll/commands/serve/servlet.rb:3:in require': cannot load such file -- webrick (LoadError)` problem.

```
sudo pacman -S ruby
gem install jekyll bundler # this step was described in https://jekyllrb.com/docs/step-by-step/01-setup/
bundle config set --local path 'vendor/bundle'
bundle update
bundle exec jekyll build
bundle exec jekyll serve --livereload
```

Then I pointed my browser to [http://127.0.0.1:4000/docs/gp8-stopwatch/](http://127.0.0.1:4000/docs/gp8-stopwatch/)

# TODO
* [x] Possible connections
* [ ] Rough state machine description (simplified) - blind 
* [x] Pictures 

