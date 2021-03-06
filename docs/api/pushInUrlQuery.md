### `pushInUrlQuery(queryParam, encodedValue, [location])`

Updates the URL to have the specified query parameter's (`queryParam`) value set to `encodedValue`, while keeping all the other query parameters the same. Uses push to change the URL, which means the new state will be pushed on to the history stack, so the back button will be able to return you to the previous state.

#### Arguments

1. `queryParam` (*String*): The name of the query parameter to update.
1. `encodedValue` (*String*): The value to set the query parameter to have in the URL.
1. [`location`] (*Object*): The location from which the current URL state should be read. If not provided, `location` is read from the configured `history` or the `window`.

#### Returns

(*Any*): The result of `history.push()`, will depend on the history being used.

#### Examples

```js
// Given URL /page?foo=bar&baz=123&jim=bo
pushInUrlQuery('foo', 'test');
// URL is now /page?foo=test&baz=123&jim=bo
```
