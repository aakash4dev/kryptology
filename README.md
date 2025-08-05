 This is a fork of [coinbase/kryptology](https://github.com/coinbase/kryptology) with fixes for specific bugs in v1.8.0.

 ## Usage

 To use this fork in your Go project, update your `go.mod` file:

 ```go
 go 1.17

 require github.com/coinbase/kryptology v1.8.0

 replace github.com/coinbase/kryptology => github.com/aakash4dev/kryptology v1.8.1
 ```

 Then run:
 ```bash
 go mod tidy
 go build
 ```

 ## Bug Fixes

 This fork (v1.8.1) fixes the following errors in `coinbase/kryptology` v1.8.0, specifically in `pkg/core/curves/bls12377_curve.go`:

 ```
 ../../../go/pkg/mod/github.com/coinbase/kryptology@v1.8.0/pkg/core/curves/bls12377_curve.go:352:22: undefined: bls12377.HashToCurveG1Svdw
 ../../../go/pkg/mod/github.com/coinbase/kryptology@v1.8.0/pkg/core/curves/bls12377_curve.go:626:22: undefined: bls12377.HashToCurveG2Svdw
 ```

 These errors were resolved by modifying `pkg/core/curves/bls12377_curve.go`.

 ## Notes
 - The original repository is archived and no longer maintained.
 - If you encounter `internal` package errors, ensure the module path is updated to `github.com/aakash4dev/kryptology` (see below).

 