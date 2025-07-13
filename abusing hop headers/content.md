# Abusing Hop Headers

_Adding known Hop-by-Hop headers to the `Connection:` header value can trick misconfigured reverse proxies or load balancers into removing important headers, potentially causing access control bypass or unexpected behavior._

## Table of Contents

1. [Understand the Basics of HTTP Headers](#-understand-the-basics-of-http-headers)

## Understand the Basics of HTTP Headers

**HTTP/1.1 Headers** are pieces of metadata sent in HTTP requests and responses.

There are two types of headers:

- **End-to-End headers**: These are sent all the way to the final destination (e.g., `Host`, `User-Agent`).
- **Hop-by-Hop headers**: These are processed and removed by each intermediate proxy or load balancer. Examples include:
  - `Connection`
  - `Keep-Alive`
  - `Proxy-Authenticate`
  - `Proxy-Authorization`
  - `TE`
  - `Trailer`
  - `Transfer-Encoding`
  - `Upgrade`

👉 _For more about headers, make sure to read this [MDN article on HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers)._

