---
layout: post
title:      "Rails App From Scratch"
date:       2020-01-26 17:46:48 +0000
permalink:  rails_app_from_scratch
---


What they say is true - Ruby on Rails is powerful (and magical!). But to really appreciate that power and magic, you'd have to build an app from the ground up. Let's work through that initial setup of creating folders and files to get a Rails app up and running.

Let's build a coupon application, which stores coupon codes and the stores they belong to.

1. Create a coupon model in a folder `models` in a file `coupon.rb`:

```
class Coupon < ActiveRecord::Base

end
```

2. Create the table and migrate it. Go into your `db` folder and create a new folder, `migrate`, and within that folder, a new file, `001_create_coupons.rb`:

```
class CreateCoupons < ActiveRecord::Migration
  def change
    create_table :coupons do |t|
      t.string :coupon_code
      t.string :store

      t.timestamps null: false
    end
  end
end
```

3. Migrate by running `bin/rails db:migrate RAILS_ENV=test` and look at your schema file afterwards to ensure all looks well.

4. Create the `CouponsController` located in the `controllers` folder:

```
class CouponsController < ApplicationController

end
```

5. Create the routes within the folder `config` and the file `routes.rb`:

```
Rails.application.routes.draw do

  resources :coupons, only: [:index, :show, :create, :new]

end
```

The `resources` route maps HTTP verbs to controller actions automatically - just the beginning of the magic

6. Start building out the `CouponsController`:

```
class CouponsController < ApplicationController

    def index
		  @coupons = Coupon.all
    end

    def show
		  @coupon = Coupon.find(params[:id])
    end
    
    def new

    end
		
    def create
        @coupon = Coupon.new
        @coupon[:coupon_code] = params[:coupon][:coupon_code]
        @coupon[:store] = params[:coupon][:store]
        @coupon.save
        redirect_to coupon_path(@coupon)
    end
		
end
```

7. At any point, type `rails routes` in the terminal to see the created routes. 

8. Start mapping out the views within the folder `views` and folder `coupon` and your file names will look like this:

```
index.html.erb
new.html.erb
show.html.erb
```

The rest is ensuring your views display what you intend them to display, using your console for testing, and seeing what your browser displays - errors, empty content or your actual content. 

Cheers to building your own Rails app from scratch, and may you enjoy the power and magic!


