# Concurrent downloader

Downloads all links from within selected file. May be used as a console script with custom arguments (use `--help`). By default uses 100 threads, does not wait between downloads and uses random User-Agent. Why not, if we can.

### Requirements

* `eventlet`

### Usage

`downloader.py [options] links-file`

### Options

* `--threads=N`  	Number of threads to download with
* `--dir=str`		Directory to download to (default=`links-file_downloaded_files`)
* `--randomnames`	Give downloaded files random names
* `--wait=float`	Max time to wait between connections

Default values will be shown on launch with `--help`.

### Links file format

```
link1 [name1]
link2 [name2]
link3 [name3]
...
```

So, link `link1` will be downloaded either to default directory, if `name1` was not given, or it will be `name1` in current working directory.
