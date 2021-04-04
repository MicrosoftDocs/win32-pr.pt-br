---
title: OP_PACKAGE_PART_COLLECTION
description: Definição de IDL de OP_PACKAGE_PART_COLLECTION
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104008553"
---
# <a name="op_package_part_collection-structure"></a>Estrutura de OP_PACKAGE_PART_COLLECTION

Especifica uma estrutura que contém uma matriz de estruturas de OP_PACKAGE_PART.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>Membros

### <a name="cparts"></a>cParts

Contém o número de elementos em pParts.

### <a name="pparts"></a>pParts

Contém uma matriz de estruturas de OP_PACKAGE_PART.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve ser definido como todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_parte do pacote de op \_**](odj-op_package_part.md)

[**BLOB de OP \_**](odj-op_blob.md)

