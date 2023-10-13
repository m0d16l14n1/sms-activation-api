# sms-activation-api
PHP Library for working with SMS activation services

## Supported sevices
* [sms-reg.com](https://sms-reg.com) ([API Documentation](https://sms-reg.com/docs/API.html))
* [smsbower.com](https://smsbower.com) ([API Documentation](https://smsbower.com/api))
* [getsms.online](https://getsms.online) ([API Documentation](https://getsms.online/en/api.html))
* [onlinesim.io](https://onlinesim.io) ([API Documentation](https://onlinesim.io/docs/api))
* [sms-activate.org](https://sms-activate.org) ([API Documentation](https://sms-activate.org/en/api2))
* [sms-area.org](https://sms-area.org) ([API Documentation](https://sms-area.org/api/documentation.html))

## Instalation
   ```
   composer require webjeyros/sms-activation-api
   ```
## Example usage:

```php
use SmsActivator\Service\smsReg;
use SmsActivator\SmsActivator;

require_once __DIR__.'/../vendor/autoload.php';
$client= new GuzzleHttp\Client();
$smsActivator=new SmsActivator(new smsReg('_api_key_here_'),$client);
print_r($smsActivator->getBalance()) ;
```
