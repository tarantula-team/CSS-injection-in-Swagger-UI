# CSS-injection-in-Swagger-UI

We have found a CSS Injection vulnerability on Swagger UI that allows us to use the Non-Root-Relative Path Overwrite (RPO) technique to steal users' tokens based on the attribute selectors feature.

**Researcher: Kevin (DatLP) of The Tarantula Team, VinCSS (a member of Vingroup)**

## What is Swagger UI

Swagger UI allows anyone — be it your development team or your end consumers — to visualize and interact with the API’s resources without having any of the implementation logic in place. It’s automatically generated from your OpenAPI (formerly known as Swagger) Specification, with the visual documentation making it easy for back end implementation and client side consumption.

## Background

We've discovered the vulnerability when reading the following in the document of Swagger:

```
We’ve observed that the ?url= parameter in SwaggerUI allows an aacker to override an otherwise hard‐coded schema file
The decision was made to put this in the public issue tracker because (a) we aren’t going to immediately fix this, and (b) the aack surface for this is significantly diminished by our effecve sanizaon efforts to deter XSS aacks in documents used as input.
```
So Swagger had known the problem for a long time, but Swagger thought that this vulnerability could not lead to an Cross-Site Scripting (XSS) exploit there so they ignored it.


## Tested versions
Lastest version of XXX. Release: September XX, XX.

## Disclosure timeline



## Reference

1. [ Swagger UI | API Development Tools | Swagger](https://swagger.io/tools/swagger-ui/)
2. [Detecting and exploiting path‐relative stylesheet import (PRSSI) vulnerabilities | PortSwigger Research](https://portswigger.net/research/detecting-and-exploiting-path-relative-stylesheet-import-prssi-vulnerabilities)
3. [RPO](http://www.thespanner.co.uk/2014/03/21/rpo/)
4. [Exfiltration via CSS Injection](https://medium.com/bugbountywriteup/exfiltration-via-css-injection-4e999f63097d)
5. [Attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)
6. [GitHub ‐ d0nutptr/sic: A tool to perform Sequential Import Chaining](https://github.com/d0nutptr/sic)
7. [Better Exfiltration via HTML Injection ‐ d0nut ‐ Medium](https://medium.com/@d0nut/better-exfiltration-via-html-injection-31c72a2dae8b)
8. [2019‐s3_css_injection_attacks.pdf](https://vwzq.net/slides/2019-s3_css_injection_attacks.pdf)
9. [RPO Gadgets](https://blog.innerht.ml/rpo-gadgets/)
10. [add an `enableQueryConfig` option issue #4872](https://github.com/swagger-api/swagger-ui/issues/4872)


