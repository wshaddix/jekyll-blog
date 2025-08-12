---
layout: post
title: How to create blogs and pages
---
Usage
After you have installed (see above), run bundle exec jekyll help and you should see:

Listed in help you will see new commands available to you:

  draft      # Creates a new draft post with the given NAME
  post       # Creates a new post with the given NAME
  publish    # Moves a draft into the _posts directory and sets the date
  unpublish  # Moves a post back into the _drafts directory
  page       # Creates a new page with the given NAME
  rename     # Moves a draft to a given NAME and sets the title
  compose    # Creates a new file with the given NAME
Create your new page using:

    $ bundle exec jekyll page "My New Page"
Create your new post using:

    $ bundle exec jekyll post "My New Post"
    # or specify a custom format for the date attribute in the yaml front matter
    $ bundle exec jekyll post "My New Post" --timestamp-format "%Y-%m-%d %H:%M:%S %z"
    # or by using the compose command
    $ bundle exec jekyll compose "My New Post"
    # or by using the compose command with post specified
    $ bundle exec jekyll compose "My New Post" --post
    # or by using the compose command with the posts collection specified
    $ bundle exec jekyll compose "My New Post" --collection "posts"
Create your new draft using:

    $ bundle exec jekyll draft "My new draft"
    # or by using the compose command with draft specified
    $ bundle exec jekyll compose "My new draft" --draft
    # or by using the compose command with the drafts collection specified
    $ bundle exec jekyll compose "My new draft" --collection "drafts"
Rename your draft using:

$ bundle exec jekyll rename _drafts/my-new-draft.md "My Renamed Draft"
# or rename it back
$ bundle exec jekyll rename _drafts/my-renamed-draft.md "My new draft"
Publish your draft using:

    $ bundle exec jekyll publish _drafts/my-new-draft.md
    # or specify a specific date on which to publish it
    $ bundle exec jekyll publish _drafts/my-new-draft.md --date 2014-01-24
    # or specify a custom format for the date attribute in the yaml front matter
    $ bundle exec jekyll publish _drafts/my-new-draft.md --timestamp-format "%Y-%m-%d %H:%M:%S %z"
Rename your post using:

$ bundle exec jekyll rename _posts/2014-01-24-my-new-draft.md "My New Post"
# or specify a specific date
$ bundle exec jekyll rename _posts/2014-01-24-my-new-post.md "My Old Post" --date "2012-03-04"
# or specify the current date
$ bundle exec jekyll rename _posts/2012-03-04-my-old-post.md "My New Post" --now
Unpublish your post using:

    $ bundle exec jekyll unpublish _posts/2014-01-24-my-new-draft.md
Create your new file in a collection using:

    $ bundle exec jekyll compose "My New Thing" --collection "things"
