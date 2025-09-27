# Default Starter Kit For TypeScript

[![Deploy to Fastly](https://deploy.edgecompute.app/button)](https://deploy.edgecompute.app/deploy)

Get to know the Fastly Compute environment with a basic starter in TypeScript that demonstrates routing, simple synthetic responses and code comments that cover common patterns.

**For more details about other starter kits for Compute, see the [Fastly Documentation Hub](https://www.fastly.com/documentation/solutions/starters)**

## Features
* TypeScript source files
* `tsconfig.json` file to use as a starting point
* Allow only requests with particular HTTP methods
* Match request URL path and methods for routing
* Build synthetic responses at the edge

## Understanding the code

This starter kit is written in TypeScript and illustrates the same features as the [Compute JavaScript default starter kit](https://github.com/fastly/compute-starter-kit-typescript-default). It is intentionally lightweight, and requires no dependencies aside from the [`@fastly/js-compute`](https://www.npmjs.com/package/@fastly/js-compute) npm package. It will help you understand the basics of processing requests at the edge using Fastly. This starter includes implementations of common patterns explained in our [using Compute](https://www.fastly.com/documentation/guides/compute/javascript/) and [VCL migration](https://www.fastly.com/documentation/guides/compute/migrate/) guides. The starter doesn't require the use of any backends. Once deployed, you will have a Fastly service running on Compute that can generate synthetic responses at the edge.

The Compute JavaScript SDK [has built-in support](https://www.fastly.com/documentation/guides/compute/developer-guides/javascript/#built-in-typescript) for executing TypeScript source files that contain only erasable TypeScript syntax. In this mode, type checking is not performed.

The SDK does not directly refer to the `tsconfig.json` file, but one is included to aid your IDE in coding support as well as to illustrate the recommended practice of running `tsc --noEmit` in a `prebuild` script to check for TypeScript errors, since the SDK does not perform type checking.

## Running the application

To create an application using this starter kit, create a new directory for your application and switch to it, and then type the following command:

```shell
npm create @fastly/compute@latest -- --language=typescript --default-starter-kit
```

To build and run your new application in the local development environment, type the following command:

```shell
npm run start
```

To build and deploy your application to your Fastly account, type the following command. The first time you deploy the application, you will be prompted to create a new service in your account.

```shell
npm run deploy
```

## Security issues

Please see our [SECURITY.md](SECURITY.md) for guidance on reporting security-related issues.
