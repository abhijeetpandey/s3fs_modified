s3fs_modified
=============

It's a fuse based file system which is taken from https://code.google.com/p/s3fs/ and is modified to add some additional headers

What's modified/added ?
=============

Added new headers 'cache_control' and 'expires' in the code. They can be used using -oexpiry_days | -oexpiry_years | -ocache_control
<br/>
e.g. 
* -oexpiry_days=100
* -oexpiry_years=5
* -ocache_control=324000 <-- this is max-age in seconds

Usage
=============

s3fs -o allow_other -oexpiry_years=5 -ocache_control=8440000 -odefault_acl=public-read <bucket_name> <mount-point>
