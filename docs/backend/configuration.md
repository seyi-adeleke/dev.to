---
title: Configuration
---

# Configuration

We currently use two gems for configuring the application:

* [rails-settings-cached](https://github.com/huacnlee/rails-settings-cached)
* [ENVied](https://github.com/eval/envied)

## ENVied

This gem is primarily used for configuring environment variables related to credentials and third party services. Examples:

* `REDIS_URL`
* `FASTLY_API_KEY`
* `STRIPE_SECRET_KEY`

Settings managed via ENVied can be found in [`Envfile`](https://github.com/thepracticaldev/dev.to/blob/master/Envfile) (see [Configuring Environment Variables](../getting-started/config-env.md)).

## rails-settings-cached

We use this gem for managing settings used within the app's business logic. Examples:

* `main_social_image`
* `rate_limit_follow_count_daily`
* `suggested_tags`

These settings can be accessed via the [`SiteConfig`](https://github.com/thepracticaldev/dev.to/blob/master/app/models/site_config.rb) object and viewed / modified via `/internal/config` (see [Accessing the admin panel](./admin.md)).