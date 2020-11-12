# Golang protobuf FieldMask utils

[![Build Status](https://cloud.drone.io/api/badges/mennanov/fmutils/status.svg?ref=refs/heads/main)](https://cloud.drone.io/mennanov/fmutils)
[![Coverage Status](https://coveralls.io/repos/github/mennanov/fmutils/badge.svg?branch=main)](https://coveralls.io/github/mennanov/fmutils?branch=main)

### Filter a protobuf message with a FieldMask applied

```go
// Keep the fields mentioned in the paths untouched, all the other fields will be cleared.
fmutils.Filter(protoMessage, []string{"a.b.c", "d"})
```

### Prune a protobuf message with a FieldMask applied

```go
// Clear all the fields mentioned in the paths, all the other fields will be left untouched.
fmutils.Prune(protoMessage, []string{"a.b.c", "d"})
```

### Examples

See the [examples_test.go](https://github.com/mennanov/fmutils/blob/main/examples_test.go) for real life examples.
