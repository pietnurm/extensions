# Gatsby Preview (beta)

**Note:** Gatsby Preview is still in beta, please be mindful when using this extension.

This UI Extension connects to [Gatsby Preview](https://www.gatsbyjs.com/preview/) to see content changes in Contentful updated in real time in your Gatsby site.

![Demo of the extension](demo.gif)

## Overview

The extension has the following features:

- monitor changes on content as you type
- real time preview updates (de-bounced by 1000 ms)
- manual preview updates

The extension has the following spec:

- it is a sidebar extension used in a [custom sidebar](https://www.contentful.com/developers/docs/extensibility/custom-sidebar/)
- uses the Contentful design system [Forma 36](https://f36.contentful.com/)
- installation parameter to set global `projectId`
- instance parameters to
  - set an optional `slug` fragment for each content type
  - toggle auto-update when typing

![Screenshot of the extension](screenshot.png)

## Requirements

In order to use this extension, you need:

- a [Gatbsy Preview](https://www.gatsbyjs.com/preview/) setup to use this extension
- a space and the Contentful CLI installed

## Usage

After cloning, install the dependencies

```bash
npm install
```

To bundle the extension

```bash
npm run build
```

To host the extension for development on `http://localhost:1234`

```bash
npm run start
```

To install the extension:

```bash
contentful extension update --force --installation-parameters '{"projectId": "yourGatsbyPreviewId"}'
```