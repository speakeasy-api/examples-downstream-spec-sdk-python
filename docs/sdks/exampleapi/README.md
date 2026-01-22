# ExampleAPI SDK

## Overview

Example API: A simple example API to demonstrate spec repo SDK generation workflow

### Available Operations

* [list_users](#list_users) - List all users
* [create_user](#create_user) - Create a user
* [get_user](#get_user) - Get a user

## list_users

Returns a list of users

### Example Usage

<!-- UsageSnippet language="python" operationID="listUsers" method="get" path="/users" -->
```python
from example_api import ExampleAPI


with ExampleAPI() as ea_client:

    res = ea_client.list_users()

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[List[models.User]](../../models/.md)**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ExampleAPIDefaultError | 4XX, 5XX                      | \*/\*                         |

## create_user

Creates a new user

### Example Usage

<!-- UsageSnippet language="python" operationID="createUser" method="post" path="/users" -->
```python
from example_api import ExampleAPI


with ExampleAPI() as ea_client:

    res = ea_client.create_user(email="Aglae92@gmail.com", name="<value>")

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `email`                                                             | *str*                                                               | :heavy_check_mark:                                                  | User's email address                                                |
| `name`                                                              | *str*                                                               | :heavy_check_mark:                                                  | User's full name                                                    |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.User](../../models/user.md)**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ExampleAPIDefaultError | 4XX, 5XX                      | \*/\*                         |

## get_user

Returns a single user by ID

### Example Usage

<!-- UsageSnippet language="python" operationID="getUser" method="get" path="/users/{id}" -->
```python
from example_api import ExampleAPI


with ExampleAPI() as ea_client:

    res = ea_client.get_user(id="<id>")

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `id`                                                                | *str*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.User](../../models/user.md)**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ExampleAPIDefaultError | 4XX, 5XX                      | \*/\*                         |