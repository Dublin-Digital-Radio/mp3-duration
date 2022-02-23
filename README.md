# mp3-duration ![Travis-Build](https://travis-ci.org/ddsol/mp3-duration.svg?branch=master)

> Calculate duration of an MP3 in seconds


## Install

```
$ npm install --save mp3-duration
```

## Usage

```javascript
import mp3Duration = from 'mp3-duration';

try {
  const duration = await mp3Duration('file.mp3');
  console.log('Your file is ' + duration + ' seconds long');
} catch (err) {
  console.log(err.message);
}
```

## API

## mp3Duration(filePathOrBuffer [, cbrEstimate])

### filePathOrBuffer

Type: `string` | `Buffer`

Path to the file or a buffer with the file's contents

### cbrEstimate

Defaults to `false`. When set to `true`, will estimate the length of a
constant-bitrate mp3. This speeds up the calculation a lot but isn't
guaranteed to be accurate.


### Return value

`duration` is the duration of the mp3 in `seconds` (including fractional seconds).

## License

MIT © Han de Boer
