catbox-disk [![Build Status](https://travis-ci.org/EyePulp/catbox-disk.svg?branch=master)](https://travis-ci.org/EyePulp/catbox-disk)
=============

Disk storage adapter for [catbox](https://github.com/hapijs/catbox).

Lead Maintainer - [Andrew Hughes](https://github.com/EyePulp)

Code liberally cribbed from various other adapter examples, primarily 
  - [catbox-memory](https://github.com/hapijs/catbox-memory)
  - [catbox-s3](https://github.com/fhemberger/catbox-s3)

### Options
An example invocation:
```javascript
const client = new Catbox.Client(Disk, { cachePath: '/some/existing/dir', cleanEvery: 100000 });
```
  - `cachePath` : `string` **required** - a pre-existing path you want to store your cache files in
  - `cleanEvery` : `integer` **optional** - number of milliseconds between each cache cleanup for disk space recovery. (Default 1 hour)

### Warning/TODO
This cache doesn't currently set any sort of upper limit on its growth.  Plan accordingly, and monitor your free drive space if you're not certain about behavior.  
