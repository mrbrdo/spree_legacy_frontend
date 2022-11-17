# Spree (Legacy) Frontend

This is the old Spree Storefront extracted from Spree < 4.3 which was upgraded to Turbo/Hotwire.

## Developed by

[![Vendo](https://assets-global.website-files.com/6230c485f2c32ea1b0daa438/623372f40a8c54ca9aea34e8_vendo%202.svg)](https://getvendo.com?utm_source=spree_frontend_github)

> All-in-one platform for all your Marketplace and B2B eCommerce needs. [Start your 30-day free trial](https://e98esoirr8c.typeform.com/contactvendo?typeform-source=spree_sdk_github)

## Installation

Add

```ruby
gem 'spree_frontend'
```

to your `Gemfile`, and make sure both `gem 'jsbundling-rails'` and `gem 'turbo-rails'` are added.

Run:

```bash
bundle install
bin/rails javascript:install:esbuild
bin/rails turbo:install
bin/rails g spree:frontend:install
```

## Running Tests

In order to generate the dummy app required for running tests, you’ll need to have the following installed on your machine:
* node v16.13.1 (npm v8.1.2)
* yarn ≥ v1.22.15
* ruby v3.0.3

To run tests locally, first run `bundle exec rake test_app`, then `bundle exec rspec`.

### Troubleshooting
If you are running on a Mac with an M1 processor, you may run into the following error when running tests:
```          
Webdrivers::NetworkError:
Net::HTTPServerException: 404 "Not Found"
```
If so, update your gemfile locally to get version 5.0 or higher for the web drivers gem:
```
gem 'webdrivers', '~> 5.0'
```

## Maintanence policy

This gem is in maintainence mode.

We only accept bug fixes, Spree/Rails compatibility improvements & security patches.

For new project we recommend using [Storefront API](https://api.spreecommerce.org/) to create your own unique storefront or use one of the pre-built starters: 

* [Next.js](https://dev-docs.spreecommerce.org/storefronts/next.js-commerce)
* [Vue Storefront](https://dev-docs.spreecommerce.org/storefronts/vue-storefront)

## Customization

[Developer documentation](https://dev-docs.spreecommerce.org/customization/storefront)
