---
title: OP_BLOB
description: Definição de IDL de OP_BLOB
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796886"
---
# <a name="op_blob-structure"></a>Estrutura de OP_BLOB

Contém um buffer de bytes opaco.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Membros

### <a name="cbblob"></a>cbBlob

Especifica o tamanho de pBlob em bytes.

### <a name="pblob"></a>pBlob

Aponta para um buffer de bytes.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)
