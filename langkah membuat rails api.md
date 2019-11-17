## Langkah membuat rails API

### membuat aplikasi baru

  * rails new market_place_api --api --database=postgresql
    * --api artinya hanya generate api
    * --database=postgresql = pakai postgresql
  * menghilangkan gem 'tzinfo-data'
    * buka Gemfile dan beri mark pada baris gem 'tzinfo-data'
    * ini hanya untuk windows
  * 