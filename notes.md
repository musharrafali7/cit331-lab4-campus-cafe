# HTTP observations (Lab 4, Task 1)

| Question | My answer |
|----------|-----------|
| Request method for index.html | GET |
| Status code with Disable cache ticked | 200 OK |
| Status code on a normal reload | 304 Not Modified |
| Status code for /nothing-here.html | 404 Not Found |
| Value of the Content-Type response header | text/html; charset=UTF-8 |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |

## Why is this address http and not https?

This local website is not deployed over internet so that is why its http and not https. https does encryption and we dont need that for development time.

This local website is not deployed over internet so that is why its http and not https. https does encryption and we dont need that

## XSS Security Question (Task 3)
The browser would execute teh injected code creating a css vulverability

## Bug log (Lab 4, Task 6)

| # | What was wrong (file and line) | Which tool showed it | My fix |
|---|---|---|---|
| 1 | `bugs.html` line 2: missing `lang` attribute on `<html>` | Lighthouse | Added `lang="en"` |
| 2 | `bugs.html` line 7: link points to non-existent `style.css` | DevTools Network Tab | Updated href to `bugs.css` |
| 3 | `bugs.html` lines 10-13: navigation links missing `<nav>` landmark | Accessibility Tree | Wrapped links in `<nav>` tag |
| 4 | `bugs.html` line 17: heading jumps from `<h1>` to `<h4>` | Accessibility Tree / Lighthouse | Changed `<h4>` to `<h2>` |
| 5 | `bugs.html` line 18: missing `alt` attribute on `<img>` | Lighthouse | Added `alt="Campus Café logo"` |
| 6 | `bugs.html` line 21: label `for="mail"` does not match input `id="email"` | Manual Test / DevTools | Changed label `for` to `email` |
| 7 | `bugs.css` line 14: invalid property `colour` | DevTools Styles Pane | Fixed property name to `color` |
| 8 | `bugs.css` line 21: missing semicolon after `background: #0b1f3a` | DevTools Styles Pane | Added missing semicolon |
| 9 | `bugs.css` line 25: selector `.notes` does not match HTML class `.note` | DevTools Styles Pane | Renamed selector to `.note` |
| 10 | `bugs.css` line 27: color `#999999` fails contrast ratio | Lighthouse | Changed color to `#595959` |