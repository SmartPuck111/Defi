async with aiohttp.ClientSession() as session:
            async with session.post(url, json=request, headers=headers) as response:
            if response.content_type == 'text/event-stream':

            ...

            elif response.content_type == 'text/plain':
                    # PROCESS TEXT EVENTS
                    result = await asyncio.wait_for(response.text(), timeout=timeout)
            else:
                raise ValueError(f"Invalid response content type: {response.content_type}")
