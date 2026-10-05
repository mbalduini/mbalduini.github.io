source "https://rubygems.org"

# Same gem set used by GitHub Pages (https://pages.github.com/versions/)
gem "github-pages", "~> 232", group: :jekyll_plugins

gem "tzinfo-data"
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Needed by `jekyll serve` on Ruby >= 3.0
gem "webrick", "~> 1.8"

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-redirect-from"
end

group :test do
  gem "html-proofer", "~> 5.0"
end
