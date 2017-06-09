## Summary
Perform multipart upload to Amazon S3 of data read from stdin.

## Example
`tar -C / -cpjO /home | 2s3 com-example-backup home.tar.bz2`

## Usage
```
Usage: 2s3 [OPTIONS] BUCKET OBJECT

  Send data from standard input to OBJECT in your S3 or S3-like BUCKET

Options:
  -p, --profile PROFILE  Amazon profile (configure in ~/.aws/...)
  -H, --host HOST        Hostname or IP of the AWS endpoint
  -i, --insecure         Insecure HTTP connection
  -o, --ordinary         Use ordinary calling format instead of subdomain
                         calling format
  -s, --size SIZE        Split upload in CHUNK_SIZE  [default: 5MB]
  -t, --time TIME        Time in seconds to wait until retry upload a failed
                         part again. Default is 5  [default: 5]
  -d, --debug            Print debug information
  -h, --help             Show this message and exit.
```
