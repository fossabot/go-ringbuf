# go-ringbuf

![Go](https://github.com/hedzr/go-ringbuf/workflows/Go/badge.svg)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/hedzr/go-ringbuf.svg?label=release)](https://github.com/hedzr/go-ringbuf/releases)
[![GoDoc](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat)](https://godoc.org/github.com/hedzr/go-ringbuf) [![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fhedzr%2Fgo-ringbuf.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fhedzr%2Fgo-ringbuf?ref=badge_shield)

[![Go Report Card](https://goreportcard.com/badge/github.com/hedzr/go-ringbuf)](https://goreportcard.com/report/github.com/hedzr/go-ringbuf)
[![Coverage Status](https://coveralls.io/repos/github/hedzr/go-ringbuf/badge.svg?branch=master&.9)](https://coveralls.io/github/hedzr/go-ringbuf?branch=master)
<!--
[![Build Status](https://travis-ci.org/hedzr/go-ringbuf.svg?branch=master)](https://travis-ci.org/hedzr/go-ringbuf)
[![codecov](https://codecov.io/gh/hedzr/go-ringbuf/branch/master/graph/badge.svg)](https://codecov.io/gh/hedzr/go-ringbuf) 
-->


`go-ringbuf` provides a high-performance, lock-free circular queue (ring buffer) implementation in golang.

MPMC (multiple-producers and multiple consumers) enabled.

## History

WIP:
 - english documentation not completed yet
 - documentation at: https:

## Getting Start

```bash
go get -v github.com/hedzr/go-ringbuf
```

### Import

```go
import "github.com/hedzr/go-ringbuf/fast"

func main() {
	var err error
	var rb = fast.New(80)
	err = rb.Enqueue(3)
	errChk(err)
	
	var item interface{}
	item, err = rb.Dequeue()
	errChk(err)
	fmt.Printf("dequeue ok: %v\n", item)
}

func errChk(err error) {
	if err != nil {
		log.Fatal(err)
	}
}
```








## Contrib

Welcome


## LICENSE

MIT


[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fhedzr%2Fgo-ringbuf.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fhedzr%2Fgo-ringbuf?ref=badge_large)