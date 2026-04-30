# GEMINI.md - Project Context

## Project Overview
**Ahmed's Blog** is a personal blog built with [Jekyll](https://jekyllrb.com/), a static site generator. The primary purpose of this blog is to implement and explain various algorithms from scratch, sharing insights and source code for educational purposes.

### Key Technologies
- **Jekyll**: Version ~> 4.0.1
- **Ruby**: Managed via Bundler (`Gemfile`)
- **Theme**: [Minima](https://github.com/jekyll/minima) (~> 2.5)
- **Markdown**: Used for writing posts and pages
- **Liquid**: Templating engine for Jekyll

## Building and Running
To work with this project locally, you need Ruby and Bundler installed.

### Prerequisites
- Ruby
- Bundler (`gem install bundler`)

### Setup and Development
1. **Install Dependencies**:
   ```bash
   bundle install
   ```
2. **Start the Development Server**:
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at `http://localhost:4000`. It will automatically rebuild when files are changed.

## Development Conventions

### Directory Structure
- `_posts/`: Contains blog posts in Markdown format.
- `_layouts/`: Custom HTML layouts (e.g., `post.html`).
- `_includes/`: Reusable HTML components (e.g., `image.html`).
- `assets/`: Static assets like images and CSS.
- `_config.yml`: Global configuration for the site.

### Creating a New Post
Posts must follow the Jekyll naming convention: `YEAR-MONTH-DAY-title.md` (e.g., `2020-05-13-random-forest.md`).

Each post should include a YAML front matter at the top:
```yaml
---
layout: post
title:  "Your Post Title"
date:   YYYY-MM-DD HH:MM:SS +/-TTTT
categories: jekyll update
author: Tanbir Ahmed
---
```

### Code Highlighting
The blog uses Liquid tags for code highlighting. Use the following syntax:
```liquid
{% highlight python %}
def my_algorithm():
    pass
{% endhighlight %}
```

### Images
Images should be placed in `assets/images/` and can be included using the custom `image.html` include or standard Markdown syntax.
