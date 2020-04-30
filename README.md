# About

Demo is about a simple worklfow that tries to get over all operations required to upload, download and delete a file to an arbitrary path.

Please refer to **lib/workflow.py** source code and its comments for detailed information.

*Notice: since authentication APIs send passwords in clear text, it is advised to configure BIMcloud to get accessible by using https endpoints from the Internet.*

# Installation

The demo console application requires Python 3.7+ with installed [requests](https://2.python-requests.org/) library to run.

The easiest way to obtain this is just installing the standard [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/distribution/#download-section) environment. It has every requirement provided by default.

With [invidual Python 3 environment](https://www.python.org/downloads/), [requests](https://2.python-requests.org/) should get installed by [using pip or easy_install](https://2.python-requests.org/en/v2.9.1/user/install/).

Eg.:

```bash
pip install requests
```

# Run

The demo is a basic commandline application. Entering:

```bash
python ./demo.py --help
```

provides:

```
usage: demo.py [-h] -m MANAGER -u USER -p PASSWORD -c CLIENTID [-d]

optional arguments:
  -h, --help            show this help message and exit
  -m MANAGER, --manager MANAGER
                        Url of BIMcloud Manager.
  -u USER, --user USER  User name.
  -p PASSWORD, --password PASSWORD
                        Password.
  -c CLIENTID, --clientid CLIENTID
                        3rd party client id (arbitrary unique string, your
                        domain for example).
  -d, --debug           Debug exceptions.
```

That should be obvious. Enter this for example to get the demo rolling:

```bash
python ./demo.py -m=http://localhost:22000 -u=masteradmin -p=123 -clientid=graphisoft.com
```