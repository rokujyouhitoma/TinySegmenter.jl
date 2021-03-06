# TinySegmenter

[![Build Status](https://travis-ci.org/chezou/TinySegmenter.jl.svg?branch=master)](https://travis-ci.org/chezou/TinySegmenter.jl)

TinySegmenter.jl is a Julia version of [TinySegmenter](http://chasen.org/~taku/software/TinySegmenter/), which is an extremely compact Japanese tokenizer
originaly written in JavaScript by Mr. Taku Kudo.

## Usage

```jl
using TinySegmenter

join(tokenize("私の名前は中野です"), " | ")
# "私 | の | 名前 | は | 中野 | です"
```

The return value of `tokenize` is an array of substrings of the string input,
giving the locations of the tokens in the text.  (Substrings are represented
by the `SubString` Julia type.)
