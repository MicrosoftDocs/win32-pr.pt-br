---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Uma união de tipos escalares.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417023"
---
# <a name="dml_scalar_union-union-directmlh"></a>DML_SCALAR_UNION união (directml.h)
Uma união de tipos escalares.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a>Membros

`Bytes`

Uma matriz de 8 byte.


`Int8`

Um inteiro com sinal de 8 bits.


`UInt8`

Um inteiro de 8 bits sem sinal.


`Int16`

Um inteiro de 16 bits com sinal.


`UInt16`

Um inteiro sem sinal de 16 bits.


`Int32`

Um inteiro com sinal de 32 bits.


`UInt32`

Um inteiro sem sinal de 32 bits.


`Int64`

Um inteiro com sinal de 64 bits.


`UInt64`

Um inteiro sem sinal de 64 bits.


`Float32`

Um número de ponto flutuante de precisão simples.


`Float64`

Um número de ponto flutuante de precisão dupla.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |