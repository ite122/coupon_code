Coupon Code
===========
PHP library to generate and validate coupon code strings.

Synopsis
--------
This library is a loose port of the 
[CPAN module Algorithm::CouponCode](https://github.com/grantm/Algorithm-CouponCode) 
by Grant McLean.

Copyright & License
-------------------
This library is Copyright (c) 2014 Marius Wilms if not otherwise stated.
The code is distributed under the terms of the BSD 3-clause License. For
the full license text see the LICENSE file.

Installation
------------
The preferred installation method is via composer. You can add
the library as a dependency via:

```
composer require atelierdisko/coupon_code
```

Quickstart
----------
```php
use CouponCode\CouponCode;

$code = new CouponCode();

$result = $code->generate();
// returns a string in `XXXX-XXXX-XXXX` format i.e.
// `1K7Q-CTFM-LMTC`.

$code->validate($result);
// returns a boolean indicating if the code is valid.

$code->normalize('i9oD_V467-8Dsz');
// returns `190D-V467-8D52`
```
