
## PHP Slim

create project slim library

```bash
  mkdir php-slim
  cd php-slim
```

Install library
```bash
  composer require slim/slim
  composer require slim/psr7
  composer require slim/middleware
```
index.php
```bash
<?php

use Psr\Http\Message\ResponseInterface as Response;
use Psr\Http\Message\ServerRequestInterface as Request;
use Slim\Factory\AppFactory;

require __DIR__ . '/vendor/autoload.php';

$app = AppFactory::create();

$app->get('/', function (Request $request, Response $response, $args) {
    $response->getBody()->write("Hello, World!");
    return $response;
});

$app->run();

```

run project
```bash
  php -S localhost:8080 index.php
```

## PHP Skeleton

create project
```bash
  composer create-project slim/slim-skeleton [ชื่อโปรเจ็คของคุณ]
```
run project
```bash
  php -S localhost:8080 -t public/
```
