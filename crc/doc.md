<!-- Code generated by gomarkdoc. DO NOT EDIT -->

# crc

```go
import "github.com/intel/ixl-go/crc"
```

Package crc provides CRC calculation functions which leverage IAA hardware.

## Index

- [Constants](<#constants>)
- [func Ready() bool](<#func-ready>)
- [type Calculator](<#type-calculator>)
  - [func NewCalculator() (*Calculator, error)](<#func-newcalculator>)
  - [func (calc *Calculator) CheckSum16(data []byte, poly uint16) (uint16, error)](<#func-calculator-checksum16>)
  - [func (calc *Calculator) CheckSum32(data []byte, poly uint32) (uint32, error)](<#func-calculator-checksum32>)
  - [func (calc *Calculator) CheckSum64(data []byte, poly uint64) (uint64, error)](<#func-calculator-checksum64>)


## Constants

```go
const (
    // ISO polynomial value
    ISO uint64 = 0xD800000000000000
    // ECMA polynomial value
    ECMA uint64 = 0xC96C5795D7870F42
)
```

```go
const (
    // IEEE polynomial value
    IEEE uint32 = 0xedb88320
    // Castagnoli polynomial value
    Castagnoli uint32 = 0x82f63b78
    // Koopman polynomial value
    Koopman uint32 = 0xeb31d82e
)
```

```go
const (
    // CCITT polynomial value
    CCITT uint16 = 0x8408
    // T10DIF polynomial value
    T10DIF uint16 = 0x8BB7
)
```

## func Ready

```go
func Ready() bool
```

Ready returns true if the device is ready for use.

## type Calculator

Calculator is used for CRC64 calculation Notice: the data size should be less than your device's max\_transfer\_size.

```go
type Calculator struct {
    // contains filtered or unexported fields
}
```

### func NewCalculator

```go
func NewCalculator() (*Calculator, error)
```

NewCalculator creates a new Calculator to be used for CRC64 calculation

### func \(\*Calculator\) CheckSum16

```go
func (calc *Calculator) CheckSum16(data []byte, poly uint16) (uint16, error)
```

CheckSum16 calculates the CRC16 checksum for the given data and polynomial value

### func \(\*Calculator\) CheckSum32

```go
func (calc *Calculator) CheckSum32(data []byte, poly uint32) (uint32, error)
```

CheckSum32 calculates the CRC32 checksum for the given data and polynomial value

### func \(\*Calculator\) CheckSum64

```go
func (calc *Calculator) CheckSum64(data []byte, poly uint64) (uint64, error)
```

CheckSum64 calculates the CRC64 checksum for the given data and polynomial value



Generated by [gomarkdoc](<https://github.com/princjef/gomarkdoc>)