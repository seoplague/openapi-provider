# OpenApi Geocoder provider

This is the OpenAPI provider from the PHP Geocoder. This is a **READ ONLY** repository. See the
[main repo](https://github.com/geocoder-php/Geocoder) for information and documentation.

### Install

```bash
composer require seoplague/openapi-provider
```

## Usage

The API now requires an API key. [See here for more information](https://openapi.it/en/real-estate-services/geocoding).

```php
$httpClient = new \GuzzleHttp\Client();
$provider = new \Geocoder\Provider\OpenApi\OpenApi($httpClient, null, '<your-api-key>);

$result = $geocoder->geocodeQuery(GeocodeQuery::create('ул.Ленина, 19, Минск 220030, Республика Беларусь'));
$result = $geocoder->reverseQuery(ReverseQuery::fromCoordinates(...));
```

### Note

The default language-locale is `en-US`

### Contribute

Contributions are very welcome! Send a pull request to the [main repository](https://github.com/geocoder-php/Geocoder) or
report any issues you find on the [issue tracker](https://github.com/geocoder-php/Geocoder/issues).
