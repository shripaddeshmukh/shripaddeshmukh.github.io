# Academic Pages

![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)

Academic Pages is a Github Pages template for academic websites.

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running Locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    **On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about):**
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    
    **On MacOS:**
    ```bash
    # Install Ruby and Node via Homebrew
    brew install ruby
    brew install node
    
    # Add Homebrew Ruby to your PATH (required to use Homebrew Ruby instead of system Ruby)
    echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
    echo 'export PATH="/opt/homebrew/lib/ruby/gems/3.4.0/bin:$PATH"' >> ~/.zshrc
    
    # Reload your shell configuration
    source ~/.zshrc
    
    # Install Bundler
    gem install bundler
    ```
    
    **Note for macOS users:** If you get a permission error when running `gem install bundler`, it means you're using the system Ruby instead of Homebrew Ruby. Make sure you've added Ruby to your PATH and reloaded your shell configuration as shown above.

1. Navigate to your project directory and install dependencies:
    ```bash
    cd path/to/your/project
    bundle install
    ```
    If you get errors, delete `Gemfile.lock` and try again.

1. Start the Jekyll development server:
    ```bash
    bundle exec jekyll serve -l -H localhost
    ```
    The site will be available at `http://localhost:4000/`. The local server will automatically rebuild and refresh the pages on change.
    
    Press `Ctrl+C` to stop the server.

### Running the Website (After Initial Setup)

Once you've completed the initial setup, you only need to run these commands each time you want to work on your site:

```bash
cd path/to/your/project
bundle exec jekyll serve -l -H localhost
```

Then open your browser to `http://localhost:4000/`

### Troubleshooting

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`

# Maintenance

Bug reports and feature requests to the template should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.
