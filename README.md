# Rails pagy 

Rails 頁碼套件

[https://ddnexus.github.io/pagy/index](#https://ddnexus.github.io/pagy/index)

* gem 'pagy'
* application_controller.rb 加入 ** include Pagy::Backend **
* product_controller.rb 加上 ** @pagy, @records = pagy(Product.all) **
* application_helper.rb 加上 ** include Pagy::Frontend **
* 要出現頁碼的 view 加上 ** pagy_nav(@pagy) or pagy_bootstrap_nav(@pagy) if @pagy.pages > 1 **

## config
config/initializers/pagy.rb

	Pagy::VARS[:items]    = 出現數量

