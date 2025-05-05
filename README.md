# Time Bucket Calculator

A simple web-based tool that splits a time range into equal-sized buckets. This tool is useful for time series analysis, data visualization, and scheduling applications.

## Features

- Split any time range into equal-sized buckets
- User-friendly datetime picker interface
- Real-time calculation
- Error handling for invalid inputs
- Pretty-printed JSON output
- Responsive design
- No external dependencies

## How It Works

### Core Functionality

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

## Usage

1. Open `index.html` in any modern web browser
2. The form will be pre-filled with:
   - Current time as start time
   - Tomorrow at the same time as end time
   - 14 buckets by default

3. Adjust the inputs as needed:
   - Use the datetime picker to select start and end times
   - Enter the desired number of buckets (minimum: 1)

4. Click "Calculate Buckets" to see the results
   - The boundaries will be displayed in ISO 8601 format
   - Each timestamp represents the start of a bucket
   - The last timestamp represents the end of the final bucket

## Error Handling

The calculator handles several error cases:
- Invalid date formats
- End time before or equal to start time
- Invalid number of buckets

## Technical Details

- Built with vanilla JavaScript (no frameworks)
- Uses native HTML5 datetime-local input
- Responsive CSS for all screen sizes
- ISO 8601 timestamp format for precision
- JSON formatting for easy data consumption

## Browser Support

Works in all modern browsers that support:
- HTML5 datetime-local input
- ES6 JavaScript features
- CSS3

## License

This project is open source and available under the MIT License. 