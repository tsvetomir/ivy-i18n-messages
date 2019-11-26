# Angular Ivy - i18n for library components

Messages for third-party components are extracted successfully when running `ng xi18n`, but the compiler fails to locate the translated strings during compilation.

To reproduce:
1. Run `npm ci`
1. Run `ng serve --configuration=es` or `ng serve --configuration=es,production`

Result:
* None of the messages declared in `CalendarModule` are translated.
* The message declared in the application ("Hello, World!") is translated.
* If `enableIvy` is set to false in `tsconfig.json` messages are translated normally.

> This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.0.0-rc.3.

