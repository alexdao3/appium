# Get All Contexts

Get all the contexts available to automate
## Example Usage

```java
// Java
Set<String> contextNames = driver.getContextHandles();

```

```python
# Python
contexts = driver.contexts

```

```javascript
// Javascript
// webdriver.io example
let contexts = driver.contexts();



// wd example
let contexts = await driver.contexts();

```

```ruby
# Ruby
contexts = @driver.available_contexts

```

```php
# PHP
$contexts = $driver->contexts();

```

```csharp
// C#
// TODO C# sample

```


## Description

Retrieve all the contexts available to be automated. This will include, at least, the native context. There can also be zero or more web view contexts. For information on the format of the context names, see the [get context documentation](/docs/en/commands/context/get-context.md).

For information on contexts, see Appium's [hybrid automation docs](/docs/en/writing-running-appium/web/hybrid.md).


## Support

### Appium Server

|Platform|Driver|Platform Versions|Appium Version|Driver Version|
|--------|----------------|------|--------------|--------------|
| iOS | [XCUITest](/docs/en/drivers/ios-xcuitest.md) | 9.3+ | 1.6.0+ | All |
|  | [UIAutomation](/docs/en/drivers/ios-uiautomation.md) | 8.0 to 9.3 | All | All |
| Android | [UiAutomator2](/docs/en/drivers/android-uiautomator2.md) | ?+ | 1.6.0+ | All |
|  | [UiAutomator](/docs/en/drivers/android-uiautomator.md) | 4.2+ | All | All |
| Mac | [Mac](/docs/en/drivers/mac.md) | None | None | None |
| Windows | [Windows](/docs/en/drivers/windows.md) | None | None | None |

### Appium Clients

|Language|Support|Documentation|
|--------|-------|-------------|
|[Java](https://github.com/appium/java-client/releases/latest)| All |  [appium.github.io](http://appium.github.io/java-client/io/appium/java_client/AppiumDriver.html#getContextHandles--)  |
|[Python](https://github.com/appium/python-client/releases/latest)| All |  [github.com](https://github.com/appium/python-client/blob/master/README.md#switching-between-native-and-webview)  |
|[Javascript (WebdriverIO)](http://webdriver.io/index.html)| All |  [webdriver.io](http://webdriver.io/api/mobile/contexts.html)  |
|[Javascript (WD)](https://github.com/admc/wd/releases/latest)| All |  [github.com](https://github.com/admc/wd/blob/master/doc/api.md)  |
|[Ruby](https://github.com/appium/ruby_lib/releases/latest)| All |  [github.com](https://github.com/appium/ruby_lib)  |
|[PHP](https://github.com/appium/php-client/releases/latest)| All |  [github.com](https://github.com/appium/php-client/)  |
|[C#](https://github.com/appium/appium-dotnet-driver/releases/latest)| All |  [github.com](https://github.com/appium/appium-dotnet-driver/)  |

## HTTP API Specifications

### Endpoint

`GET /wd/hub/session/:session_id/contexts`

### URL Parameters

|name|description|
|----|-----------|
|session_id|ID of the session to route the command to|

### JSON Parameters

None

### Response

Array of the names of all available contexts (`Array<String>`)

## See Also

* [JSONWP Specification](https://github.com/SeleniumHQ/mobile-spec/blob/master/spec-draft.md#webviews-and-other-contexts)