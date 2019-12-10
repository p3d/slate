---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the South Coast Science API! You can use our API to access message and device data.

This example API documentation page was created with [Slate](https://github.com/lord/slate).

# Topics

## Get Topics starting with a string

```shell
curl "https://qzr7tpid94.execute-api.eu-west-2.amazonaws.com/dev/bylines?topic=south-coast-science&api_key=APIKEY"
```

> The above command returns JSON structured like this:

```json
[
  {
    "last_write": "2019-11-13T11:41:46Z",
    "topic": "south-coast-science-demo/brighton/device/praxis-000401/climate",
    "device": "scs-bgx-401"
  },
  {
    "last_write": "2019-11-13T11:41:46Z",
    "topic": "south-coast-science-demo/brighton/device/praxis-000401/gases",
    "device": "scs-bgx-401"
  },
  {...}
]
```

### Query Parameters

| Parameter | Required | Description                                                |
| --------- | -------- | ---------------------------------------------------------- |
| api_key   | true     | Your api key                                               |
| topic     | true     | A string matching the start of a topic you have access to. |
