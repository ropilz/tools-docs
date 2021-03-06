---
title: Installing
order: 201
description: How to install the GraphQL Server
---

GraphQL server is a flexible, community driven, production-ready HTTP GraphQL server plugin for Node.js.

It works with any GraphQL schema built with GraphQL.js, Facebook's reference JavaScript execution library, and you can use GraphQL Server with all popular JavaScript HTTP servers, including Express, Connect, Hapi, Koa, Restify, and Lambda.

This server can be queried from any popular GraphQL client, such as [Apollo](http://dev.apollodata.com) or [Relay](https://facebook.github.io/relay) because it supports all of the common semantics for sending GraphQL over HTTP, as [documented on graphql.org](http://graphql.org/learn/serving-over-http/). GraphQL Server also supports some small extensions to the protocol, such as sending multiple GraphQL operations in one request. Read more on the [sending requests](/tools/graphql-server/requests.html) page.

Install it with:

```bash
# Pick the one that matches your server framework
npm install graphql graphql-server-express  # for Express or Connect
npm install graphql graphql-server-hapi
npm install graphql graphql-server-koa
npm install graphql graphql-server-restify
npm install graphql graphql-server-lambda
```

The following features distinguish GraphQL Server from [express-graphql](https://github.com/graphql/express-graphql), Facebook's reference HTTP server implementation:

- GraphQL Server has a simpler interface and allows fewer ways of sending queries, which makes it a bit easier to reason about what's going on.
- GraphQL Server serves GraphiQL on a separate route, giving you more flexibility to decide when and how to serve it.
- GraphQL Server supports [query batching](https://medium.com/apollo-stack/query-batching-in-apollo-63acfd859862) which can help reduce load on your server.
- GraphQL Server has built-in support for persisted queries, which can make your app faster and your server more secure.
