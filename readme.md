## Lavender

Lavender is an Open Source E-Commerce Framework built on top of Laravel.


### License

Lavender is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)


### Support

Come chat with us on [freenode in #lavender](http://webchat.freenode.net/?channels=#lavender), or [submit an new issue.](https://github.com/lavender/lavender/issues/new)


### Installation instructions

Run Composer:

    composer create-project lavender-commerce/lavender

Set lavender/public as your new web root (example):

    ln -s lavender/public public_html

Navigate to the lavender directory:

    cd lavender
    
Set up your connection in the database config file:

    vim app/config/database.php

Run the lavender installer:

    php artisan lavender:install
    
Publish all package assets:

    php artisan asset:publish
    
Seed catalog sample data! (optional)

    php artisan db:seed --class=SampleData

That's it!


### Troubleshooting

Login not working? Try modifying your sessions config:

    app/config/session.php

Emails not working? Try modifying your email config:

    app/config/mail.php

Something else? Follow the install instructions carefully or [submit an new issue!](https://github.com/lavender/lavender/issues/new)


### Lavender Ecommerce Features

#### Entities

A common task while developing features for an e-commerce site is extending existing entities (customers, orders, products,
etc) and creating new ones (blog posts, banners, etc) and handling relationships. Lavender's Entity model (see 'entity.php' config files) makes it easy to create and extend entities without having to deal with managing rewrite conflicts, writing database migrations or manually creating relationships.

##### Updating entities

To create a new migration based on updated entity config, run:

    php artisan migrate:entity make_foo

...which creates a migration file for you, now run:

    php artisan migrate

You're done!


#### Themes

You can configure routes, route filter, views, and view composers based on themes. Themes can be configured to fallback to the 'default' theme with an unlimited depth of inheritence.

#### Routing

Routes can be configured from the 'routes.php' config file. available to each module. 

#### Layout Injection

Injecting content to templates is done via the 'layout.php' config file. 

#### View composers and Filters

You can assign composers to views with the 'composers.php' config file and predefine route filters in 'filters.php' file.


### Contributing

This repository contains the controllers, models, and views that makes Lavender an Ecommerce platform. Lavender is in active development and [pull requests](https://github.com/lavender/lavender/pulls) are much appreciated! (especially with frontend stuff)

To contribute to the Lavender Framework, please see the [lavender/framework](https://github.com/lavender/framework) repository.
