source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the right Jekyll version is running.
# Happy Jekylling!
gem "jekyll", "~> 4.3.0"
# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minimal-mistakes-jekyll"
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-paginate", "~> 1.1"
  gem "jekyll-sitemap", "~> 1.4"
  gem "jekyll-gist", "~> 1.5"
  gem "jekyll-include-cache", "~> 0.2"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
# Include the-file-watcher-gem if you are on Windows.
# Uncomment the following line if you are using Windows and want improved file watcher performance
# gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` to `v0.6.x` on JRuby. If you upgrade to a newer version of Ruby, you may need to `bundle update`.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
