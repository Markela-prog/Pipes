# PipesDeepDive

Pipes transform the way data is displayed

## Built-in Pipes

- AsyncPipe	        Read the value from a Promise or an RxJS Observable.
- CurrencyPipe	    Transforms a number to a currency string, formatted according to locale rules.
- DatePipe	        Formats a Date value according to locale rules.
- DecimalPipe	    Transforms a number into a string with a decimal point, formatted according to locale rules.
- I18nPluralPipe	Maps a value to a string that pluralizes the value according to locale rules.
- I18nSelectPipe	Maps a key to a custom selector that returns a desired value.
- JsonPipe	        Transforms an object to a string representation via JSON.stringify, intended for debugging.
- KeyValuePipe	    Transforms Object or Map into an array of key value pairs.
- LowerCasePipe	    Transforms text to all lower case.
- PercentPipe	    Transforms a number to a percentage string, formatted according to locale rules.
- SlicePipe         Creates a new Array or String containing a subset (slice) of the elements.
- TitleCasePipe	    Transforms text to title case.
- UpperCasePipe	    Transforms text to all upper case.

## Custom Pipes

All pipes must have transform method!

```
import { Pipe, PipeTransform } from "@angular/core";

@Pipe({
    name: 'temp', // must be set
    standalone: true,
})
export class TemperaturePipe implements PipeTransform {
    
    transform(value: any, ...args: any[]) {
        return value + ' - transformed';
    }
}
```

Transform accepts a value on which the pipe is used and the config values for the pipe