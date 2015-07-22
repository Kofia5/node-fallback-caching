# Node Fallback Caching

Will use node-cached to create a ~getAndSetORFallbackOnCache-esque function
inputs: generator function, cache name (optional: setting timing logic)

# Default behavior:
1) use generator function to get data
2a) if good data, return data
3a) set data to cache if setting timing logic says so (default: always set)

2b) if bad data, hit cache for data
3b) if cache has data, return data (optional? try to generate fresh data after fallback)
3c) if no data, return error
