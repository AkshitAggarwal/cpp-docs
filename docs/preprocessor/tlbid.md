---
title: "tlbid | Microsoft Docs"
ms.custom: ""
ms.date: "10/18/2018"
ms.technology: ["cpp-tools"]
ms.topic: "reference"
f1_keywords: ["tlbid"]
dev_langs: ["C++"]
helpviewer_keywords: ["tlbid attribute"]
ms.assetid: 54b06785-191b-4e77-a9a5-485f2b4acb09
author: "corob-msft"
ms.author: "corob"
ms.workload: ["cplusplus"]
---
# tlbid

**C++ Specific**

Allows for loading libraries other than the primary type library.

## Syntax

```
tlbid(number)
```

### Parameters

*number*<br/>
The number of the type library in `filename`.

## Remarks

If multiple type libraries are built into a single DLL, it possible to load libraries other than the primary type library by using **tlbid**.

For example:

```cpp
#import <MyResource.dll> tlbid(2)
```

is equivalent to:

```cpp
LoadTypeLib("MyResource.dll\\2");
```

**END C++ Specific**

## See Also

[#import Attributes](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import Directive](../preprocessor/hash-import-directive-cpp.md)