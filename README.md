# Rails pagy 

Rails 頁碼套件

[https://ddnexus.github.io/pagy/index](https://ddnexus.github.io/pagy/index)

* gem 'pagy'
* application_controller.rb 加入 ** include Pagy::Backend **
* product_controller.rb 加上 ** @pagy, @records = pagy(Product.all) **
* application_helper.rb 加上 ** include Pagy::Frontend **
* 要出現頁碼的 view 加上 ** pagy_nav(@pagy) or pagy_bootstrap_nav(@pagy) if @pagy.pages > 1 **

## config
config/initializers/pagy.rb

	Pagy::VARS[:items]    = 出現數量


## i18n
https://github.com/ddnexus/pagy/tree/master/lib/locales

config include ** require 'pagy/extras/i18n' **

	pagy:
	    nav:
	      prev: "上一頁"
	      next: "下一頁"
	      gap: "…"
	    combo_nav_js: "第 %{page_input} / %{pages} 頁"
	    
	    info:
	      no_items: "沒找到項"
	      single_page: "顯示 <b>%{count}</b> 項%{item_name}"
	      multiple_pages: "共 <b>%{count}</b> 項%{item_name}，顯示 <b>%{from}-%{to}</b>"

	    items_selector_js: "每頁顯示 %{items_input} 項%{item_name}"

