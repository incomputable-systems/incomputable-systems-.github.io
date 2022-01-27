# Incomputable LLC Website

Incomputable is a software engineering consulting company specialized in high-performance computing (HPC). We deliver customized software systems to execute workflows on the largest HPC platforms in the world. With more than twenty years of experience, we bring to your organization the cutting edge technology that power workflow applications at scale. We enable computational innovation in biology, chemistry, material engineering, particle physics and climate sciences. We engage in the grand challenges of our times, fighting cancer, climate change and pandemics. 

This site is based on a clone of [SinglePaged theme](https://github.com/t413/SinglePaged)

## Run the website locally

To run locally, follow Jekyll's [installation instructions](https://jekyllrb.com/), clone this repository and `cd` in its root directory.

### Ubuntu

```bash
sudo gem install jekyll
sudo gem install rouge
sudo gem install jekyll-redirect-from
sudo gem install bundler
sudo gem install html-proofer
jekyll serve
```

### macOS

First, install [homebrew](https://brew.sh/) if not already installed, then do the following. Note: use `.zshrc` instead of `.bash_profile` if you are using `zsh` shell instead of `bash`.

```
xcode-select --install
brew install ruby
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
gem install --user-install bundler jekyll rouge jekyll-redirect-from html-proofer
echo 'export PATH="/Users/$USER/.gem/ruby/2.7.0/bin:$PATH"' >> ~/.bash_profile
. ~/.bash_profile
```
Note: this assumes that ruby 2.7.0 was installed. Change the last echo command if you have a different version.

Check that the installation was successful:
- `which ruby` should return `/usr/local/opt/ruby/bin/ruby` if it returns `/usr/bin/ruby` you are using the one shipped with macos and jekyll will likely not work.
- `gem env` should show `/Users/$USER/.gem/ruby/2.7.0/bin:$PATH` under SHELL PATH.

Issue:
```
jekyll serve
```

You should be able to see the website in your browser at `http://127.0.0.1:4000`. Any local change made to the website should be immediately reflected reloading the page.
