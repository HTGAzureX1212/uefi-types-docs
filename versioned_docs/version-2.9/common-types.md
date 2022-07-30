---
sidebar_position: 2
---

# Common UEFI Data Types

This section defines the common data types specified in the UEFI specification.

## Primitives

| Data Type | Description                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------|
| `BOOLEAN` | A logical boolean value. It is a 1-byte value with `0` <br/>defined as `FALSE` and `1` defined as `TRUE`. |
| `INTN`    | A signed integer value of native width.                                                                   |
| `UINTN`   | An unsigned integer value of native width.                                                                |
| `INT8`    | An 8-bit signed integer value.                                                                            |
| `UINT8`   | An 8-bit unsigned integer value.                                                                          |
| `INT16`   | A 16-bit signed integer value.                                                                            |
| `UINT16`  | A 16-bit unsigned integer value.                                                                          |
| `INT32`   | A 32-bit signed integer value.                                                                            |
| `UINT32`  | A 32-bit unsigned integer value.                                                                          |
| `INT64`   | A 64-bit signed integer value.                                                                            |
| `UINT64`  | A 64-bit unsigned integer value.                                                                          |
| `INT128`  | A 128-bit signed integer value.                                                                           |
| `UINT128` | A 128-bit unsigned integer value.                                                                         |
| `CHAR8`   | An 8-bit character.                                                                                       |
| `CHAR16`  | A 16-bit character.                                                                                       |
| `VOID`    | Undeclared type.                                                                                          |

## UEFI Data Types

### 1. `EFI_GUID`

A 128-bit buffer containing a unique identifier value.

```c
typedef struct {
    UINT32 Data1;
    UINT16 Data2;
    UINT16 Data3;
    UINT8 Data4[8];
} EFI_GUID;
```

Unless otherwise specified, `EFI_GUID` is aligned on a 64-bit boundary.

### 2. `EFI_STATUS`

An EFI status code.

```c
typedef UINTN EFI_STATUS;
```

### 3. `EFI_HANDLE`

A collection of related interfaces.

```c
typedef VOID *EFI_HANDLE;
```

### 4. `EFI_EVENT`

Handle to an EFI event structure.

```c
typedef VOID *EFI_EVENT;
```

### 5. `EFI_LBA`

A logical block address.

```c
typedef UINT64 EFI_LBA;
```

### 6. `EFI_TPL`

A task priority level.

```c
typedef UINTN EFI_TPL;
```

### 7. `EFI_MAC_ADDRESS`

A 32-byte buffer containing a network Media Access Control address.

```c
typedef struct {
    UINT8 Addr[32];
} EFI_MAC_ADDRESS;
```
