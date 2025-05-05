# Time Bucket Calculator


The calculator uses the `computeBuckets` function which:

1. Takes three parameters:
   - `startIso`: Start time in ISO format
   - `endIso`: End time in ISO format
   - `buckets`: Number of buckets to split the time range into (default: 14)

2. Performs the following steps:
   - Converts ISO timestamps to milliseconds
   - Validates the input dates
   - Calculates the total duration and bucket size
   - Generates boundary timestamps for each bucket

### Example

If you input:
- Start time: 2024-03-20 00:00:00
- End time: 2024-03-21 00:00:00
- Buckets: 14

The calculator will split the 24-hour period into 14 equal buckets, each approximately 1 hour and 43 minutes long.


3. Adjust the inputs as needed:
   - Use the datetime picker to select start and end times
   - Enter the desired number of buckets (minimum: 1)

4. Click "Calculate Buckets" to see the results
   - The boundaries will be displayed in ISO 8601 format
   - Each timestamp represents the start of a bucket
   - The last timestamp represents the end of the final bucket


## Technical Details


- ISO 8601 timestamp format for precision
- JSON formatting for easy data consumption

