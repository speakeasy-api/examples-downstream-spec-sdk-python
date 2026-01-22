<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
from example_api import ExampleAPI


with ExampleAPI() as ea_client:

    res = ea_client.list_users()

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.

```python
# Asynchronous Example
import asyncio
from example_api import ExampleAPI

async def main():

    async with ExampleAPI() as ea_client:

        res = await ea_client.list_users_async()

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->