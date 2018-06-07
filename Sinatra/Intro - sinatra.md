# Intro - sinatra

- `mkdir sinatra-test`

- `cd sinatra-test` 

- `touch app.rb`

- `gem install sinatra`

- ```ruby
  # app.rb
  require 'sinatra'
  
  
  get '/' do
    'Hello world!'
  end
  ```

- `ruby app.rb -o $IP`  

> 바인딩이 필요해서 입력 변경시 서버 재시작 필요, 서버 종류 ctrl + c 