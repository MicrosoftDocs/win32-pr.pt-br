---
title: OP_BLOB
description: Definição de IDL de OP_BLOB
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366870"
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
