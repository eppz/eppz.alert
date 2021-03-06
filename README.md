## ![eppz!tools](http://eppz.eu/beacons/eppz!alert.png) eppz!alert
Simplest UIAlertView wrapper ever.
```Objective-C
[EPPZAlert alertWithTitle:@"Alert!"
                  message:@"Please choose a task below."
             buttonTitles:@[@"Clean", @"Upload", @"Cancel"]
             completition:^(NSString *selectedButtonTitle)
    {
        if ([selectedButtonTitle isEqualToString:@"Clean"])
            [self clean];
     
        if ([selectedButtonTitle isEqualToString:@"Upload"])
            [self upload];
    }];
```
- - -
Added some factory presets trough a category [EPPZAlert+Factory](https://github.com/eppz/eppz-alert/blob/master/eppz!alert/EPPZAlert%2BFactory.h#L20), so you can make it more explicit like these calls below.
```Objective-C
[EPPZAlert alertWithTitle:@"Select an answer!"
                  message:nil
                      yes:^() { [EPPZAlert alertWithTitle:@"That was a Yes!" message:@"You can belive me."]; }
                       no:^() { [EPPZAlert alertWithTitle:@"That was a No!" message:@"When I say to you."]; }
                   cancel:^() { [EPPZAlert alertWithTitle:@"That was a Cancel!" message:@"I can easily recognize."]; }]; }];
```

#### License
> Licensed under the [Open Source MIT license](http://en.wikipedia.org/wiki/MIT_License).

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/a1347c1d10981327b579a5c806597301 "githalytics.com")](http://githalytics.com/eppz/eppz-alert)
[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/eppz/eppz-alert/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

