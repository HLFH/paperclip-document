# Paperclip::Document

[![Gem Version](https://badge.fury.io/rb/paperclip-document.png)](http://badge.fury.io/rb/paperclip-document) 
[![Dependency Status](https://gemnasium.com/ekylibre/paperclip-document.png)](https://gemnasium.com/ekylibre/paperclip-document)
[![Quality metrics](https://codeclimate.com/github/ekylibre/paperclip-document.png)](https://codeclimate.com/github/ekylibre/paperclip-document)
[![Continuous Integration](https://api.travis-ci.org/ekylibre/paperclip-document.png?branch=master)](https://travis-ci.org/ekylibre/paperclip-document)
[![Code coverage](https://coveralls.io/repos/ekylibre/paperclip-document/badge.png?branch=master)](https://coveralls.io/r/ekylibre/paperclip-document)

Document processors for paperclip.

## Installation

Add this line to your application's Gemfile:

    gem 'paperclip-document'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install paperclip-document

## Usage

Use processors like the example:

    has_attached_file :file, {
      styles: {
        default:   {format: :pdf, processors: [:reader, :counter, :freezer], clean: true},
        thumbnail: {format: :jpg, processors: [:sketcher]}
      }
    }

Dev note: I have to check if text cleaning is effective on ruby >= 2.6 with docsplit-ng dependency (0.8.0)

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
