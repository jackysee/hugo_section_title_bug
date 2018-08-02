- Hugo V0.46 Extened Version, Windows 64 bit

Error

```
C:\workspace\web\hugo\sectionTitleDemo>hugo server -D
Building sites … ERROR 2018/08/02 09:24:01 Failed to render "_default\\list.html": runtime error: invalid memory address or nil pointer dereference
ERROR 2018/08/02 09:24:01 Stack Trace:
goroutine 91 [running]:
github.com/gohugoio/hugo/hugolib.stackTrace(0x4b0, 0xf2ee9e, 0x17)
        /go/src/github.com/gohugoio/hugo/hugolib/page.go:280 +0x7d
github.com/gohugoio/hugo/hugolib.(*Site).renderForLayouts.func1(0xc0427698a0, 0xc04241e300)
        /go/src/github.com/gohugoio/hugo/hugolib/site.go:1742 +0x13c
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
text/template.errRecover(0xc042769790)
        /usr/local/go/src/text/template/exec.go:137 +0x1db
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
text/template.errRecover(0xc042768b28)
        /usr/local/go/src/text/template/exec.go:137 +0x1db
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
github.com/gohugoio/hugo/hugolib.(*Page).Title(0x0, 0x0, 0x0)
        /go/src/github.com/gohugoio/hugo/hugolib/page.go:1183 +0x5
reflect.Value.call(0xedac00, 0xc0425d1a68, 0x13293, 0xee0969, 0x4, 0x18a5f60, 0x0, 0x0, 0xed5400, 0x1, ...)
        /usr/local/go/src/reflect/value.go:447 +0x970
reflect.Value.Call(0xedac00, 0xc0425d1a68, 0x13293, 0x18a5f60, 0x0, 0x0, 0xc0425baf18, 0x13, 0x4c)
        /usr/local/go/src/reflect/value.go:308 +0xab
text/template.(*state).evalCall(0xc042792aa8, 0xedd040, 0xc0426c2000,
ERROR 2018/08/02 09:24:01 Stack Trace:
goroutine 89 [running]:
github.com/gohugoio/hugo/hugolib.stackTrace(0x4b0, 0xf2ee9e, 0x17)
        /go/src/github.com/gohugoio/hugo/hugolib/page.go:280 +0x7d
github.com/gohugoio/hugo/hugolib.(*Site).renderForLayouts.func1(0xc0425c78a0, 0xc04241e300)
        /go/src/github.com/gohugoio/hugo/hugolib/site.go:1742 +0x13c
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
text/template.errRecover(0xc0425c7790)
        /usr/local/go/src/text/template/exec.go:137 +0x1db
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
text/template.errRecover(0xc0425c6b28)
        /usr/local/go/src/text/template/exec.go:137 +0x1db
panic(0xdf5660, 0x17fe180)
        /usr/local/go/src/runtime/panic.go:502 +0x237
github.com/gohugoio/hugo/hugolib.(*Page).Title(0x0, 0x0, 0x0)
        /go/src/github.com/gohugoio/hugo/hugolib/page.go:1183 +0x5
reflect.Value.call(0xedac00, 0xc042438a58, 0x13293, 0xee0969, 0x4, 0x18a5f60, 0x0, 0x0, 0xed5400, 0x1, ...)
        /usr/local/go/src/reflect/value.go:447 +0x970
reflect.Value.Call(0xedac00, 0xc042438a58, 0x13293, 0x18a5f60, 0x0, 0x0, 0xc042004d70, 0x13, 0x4c)
        /usr/local/go/src/reflect/value.go:308 +0xab
text/template.(*state).evalCall(0xc0425c6aa8, 0xedd040, 0xc0426c2500,
Total in 21 ms
Error: Error building site: logged 3 error(s)
```

The offending line seems to be in `themes\mysite\layouts\partials\header.html`, `{{ .CurrentSection.Title }}`
