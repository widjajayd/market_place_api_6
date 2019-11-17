## Langkah membuat rails API

### membuat aplikasi baru

  * rails new market_place_api --api --database=postgresql
    * --api artinya hanya generate api
    * --database=postgresql = pakai postgresql
  * menghilangkan gem 'tzinfo-data'
    * buka Gemfile dan beri mark pada baris gem 'tzinfo-data'
    * ini hanya untuk windows
  * Git
    * git add .
    * git commit -m 'initial commit'
    * penjelasan
      * secara otomatis rails membuat git init
      * maka tambahkan semua file pada project
      * dan beri commit pada step awal
    * git remote
    * git remote add origin https://github.com/widjajayd/market_place_api_6.git
    * git push -u origin master
      * username: widjajaydror@gmail.com
      * pass sur AB

### 02 membuat api user

  * mkdir app/controllers/api
    * membuat folder api di dalam controller
    * ini digunakan untuk keperluan namespace
  * buka config/routes.rb

    ```ruby
    Rails.application.routes.draw do
      namespace :api, defaults: { format: json } do
        
      end
    end
    ```
  
  * adanya namespace api ?? (masih bingung)
    * bila mau user akan menjadi localhost/users/api/1 
  * common API pattern
    * api.example.com = depannya api
    * example.com/api/
    * example.com/api/v1 
  * defaults artinya semua lalulintas 
    * data melewati routes tersebut formatnya json
  * membuat versi API
    * mkdir app/controllers/api/v1
    * buka routes.rb dan tambahkan namespacenya sbb:

      ```ruby
        Rails.application.routes.draw do
          namespace :api, defaults: { format: json } do
            namespace :v1 do
                  
            end
          end
        end
      ```

  * 