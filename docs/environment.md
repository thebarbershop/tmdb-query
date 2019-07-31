# 환경 구축

## 설치

1. (필요한 경우) 다음 스크립트를 실행하여 RVM, Ruby 2.5.3, Bundler 2.0.1를 설치한다.

    ```sh
    sudo chmod +755 install-ruby.sh
    ./install-ruby.sh
    ```

1. (필요한 경우) 다음 스크립트를 실행하여 MySQL 5.6.45를 설치한다.

    ```sh
    sudo chmod +755 install-mysql.sh
    ./install-mysql.sh
    ```

1. 본 git 저장소를 다운로드한다.

    ```sh
    git clone https://github.com/thebarbershop/tmdb-query.git
    ```

1. bundler를 이용하여 본 어플리케이션에 필요한 gem을 설치한다.

    ```sh
    bundle install
    ```

## 실행

1. MySQL 서버를 실행한다.

    ```sh
    sudo /usr/local/mysql/bin/mysqld_safe &
    ```

1. ActiveRecord Migration을 실행한다.

    ```sh
    rails db:migrate
    ```

1. 루비 온 레일즈 서버를 실행한다.

    ```sh
    rails server
    ```