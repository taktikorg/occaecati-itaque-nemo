# @taktikorg/occaecati-itaque-nemo

[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]

Yet another API.  Schema-first API modeling and validation for TypeScript, built on yaschema.

This package is almost entirely TypeScript types, except for a few configuration functions and utilities.  Yaschema-APIs have `routeType` metadata, which is helpful for directing traffic to different sets of servers.  See `setUrlBaseForRouteType` and `setDefaultUrlBase`.

Support for handling @taktikorg/occaecati-itaque-nemo requests server side and for making @taktikorg/occaecati-itaque-nemo requests either client or server side, is handled by other packages.

We love TypeScript and use it pretty much everywhere.  We use it for our React Native app, our React web app, as well as for our server.

We built @taktikorg/occaecati-itaque-nemo as part of our type and API spec system, to be TypeScript first -- and to still conveniently support code generation and OpenAPI spec generation as needed.

Because @taktikorg/occaecati-itaque-nemo leverages yaschema, you can define both runtime and compile-time validated types with a single definition.

## Basic Example

```typescript
export const POST = makeHttpApi({
  method: 'POST',
  routeType: 'rest',
  url: '/ping',
  isSafeToRetry: true,
  schemas: {
    request: {
      body: schema.object({
        echo: schema.string().allowEmptyString().optional()
      })
    },
    successResponse: {
      status: schema.number(StatusCodes.OK),
      body: schema.string()
    }
  }
});
```

## Thanks

Thanks for checking it out.  Feel free to create issues or otherwise provide feedback.

[API Docs](https://typescript-oss.github.io/@taktikorg/occaecati-itaque-nemo/)

Be sure to check out our other [TypeScript OSS](https://github.com/TypeScript-OSS) projects as well.

<!-- Definitions -->

[downloads-badge]: https://img.shields.io/npm/dm/@taktikorg/occaecati-itaque-nemo.svg

[downloads]: https://www.npmjs.com/package/@taktikorg/occaecati-itaque-nemo

[size-badge]: https://img.shields.io/bundlephobia/minzip/@taktikorg/occaecati-itaque-nemo.svg

[size]: https://bundlephobia.com/result?p=@taktikorg/occaecati-itaque-nemo
