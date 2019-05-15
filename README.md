# Guzzle Gzip Request Middleware

#### Installation with Composer

```bash
composer require tech-noir-breakfast-club/guzzle-gzip-request-middleware
```

##### Create Guzzle Client with Gzip Middleware

```php
use GuzzleHttp\Client;
use GuzzleHttp\HandlerStack;
use TechNoirBreakfastClub\GuzzleGzipRequestMiddleware\GzipMiddleware;

$stack = HandlerStack::create();
$stack->push(new GzipMiddleware());

$client = new Client([$stack]);

// Make requests galore...
