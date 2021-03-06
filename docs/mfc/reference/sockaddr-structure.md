---
title: "SOCKADDR Structure"
ms.date: "11/04/2016"
f1_keywords: ["SOCKADDR"]
helpviewer_keywords: ["SOCKADDR structure [MFC]"]
ms.assetid: df1ed66a-f4b8-43f8-8db8-8c2533d25f68
---
# SOCKADDR Structure

The `SOCKADDR` structure is used to store an Internet Protocol (IP) address for a machine participating in a Windows Sockets communication.

## Syntax

```
struct sockaddr {
    unsigned short sa_family;
    char sa_data[14];
};
```

#### Parameters

*sa_family*<br/>
Socket address family.

*sa_data*<br/>
Maximum size of all the different socket address structures.

## Remarks

The Microsoft TCP/IP Sockets Developer's Kit only supports the Internet address domains. To actually fill in values for each part of an address, you use the `SOCKADDR_IN` data structure, which is specifically for this address format. The `SOCKADDR` and the `SOCKADDR_IN` data structures are the same size. You simply cast to switch between the two structure types.

## Requirements

**Header:** winsock2.h

## See Also

[Structures, Styles, Callbacks, and Message Maps](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[SOCKADDR_IN Structure](../../mfc/reference/sockaddr-in-structure.md)<br/>
[CAsyncSocket::Create](../../mfc/reference/casyncsocket-class.md#create)<br/>
[CSocket::Create](../../mfc/reference/csocket-class.md#create)

