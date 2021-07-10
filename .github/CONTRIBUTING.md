# 開発環境
====

## IDE

IntelliJ IDEAを使用します。

### Plugin

下記の最新版をインストールします。

1. google-java-format Settings
1. Lombok Plugin

## 起動方法

1. 当プロジェクトをIntelliJ IDEAにGradleProjectとしてclone
1. openapi.jsonをgenerate(`:openapi-generate -> Tasks -> openapi tools -> openApiGenerate`)
1. docker-composeよりOpenApi/Redocを起動
   `$ docker-compose -f ./docker/mac/docker-compose.yml up -d --build`
1. Javaファイル生成(`:micro-api -> Tasks -> openapi tools -> openApiGenerate`)
1. axios-frontを生成(`:micro-site -> Tasks -> other -> generateClient`)

### Endpoints

[OpenApi(Api)][]
[Site(Riot)][]
[Swagger-ui][]
[ReDoc][]

## 停止方法

1. bootRunの停止
1. docker-composeより停止  
   `$ cd docker/mac`  
   `$ docker-compose -f docker-compose.yml stop`
1. docker-composeよりコンテナ破棄  
   `$ docker-compose -f docker-compose.yml down`

[OpenApi(Api)]: http://localhost:9001/CatCafeApi/swagger-ui.html            "OpenApi(Api)"

[Site(Riot)]: http://localhost:9011/CatCafeSite/                            "Site(Riot)"

[Swagger-UI]: http://localhost:8002/                                        "openapi-ui"

[ReDoc]: http://localhost:8081                                              "ReDoc"