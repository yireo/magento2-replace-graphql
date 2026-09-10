# Magento 2 removal of optional GraphQL modules

This repository contains a composer meta-package that removes optional modules. To install this package, use the instructions on the repository [`yireo/magento2-replace-tools`.](https://github.com/yireo/magento2-replace-tools)

## Caveats

### Interface "Magento\ReCaptchaWebapiGraphQl\Model\Adapter\ReCaptchaConfigInterface" not found 
```
There is an error in /tmp/m2/vendor/magento/module-re-captcha-version-3-invisible/Model/Config.php at line: 16
26
Interface "Magento\ReCaptchaWebapiGraphQl\Model\Adapter\ReCaptchaConfigInterface" not found#0 /tmp/m2/vendor/composer/ClassLoader.php(576): include()
```

Unfortunately the package `magento/module-re-captcha-version-3-invisible` contains a hard-coded dependency with the package
`magento/module-re-captcha-webapi-graph-ql` Because of this, the package `magento/module-re-captcha-webapi-graph-ql` is not replaced, even though it should be.
