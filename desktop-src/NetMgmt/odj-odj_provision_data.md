---
title: ODJ_PROVISION_DATA
description: Definição de IDL de ODJ_PROVISION_DATA
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105772759"
---
# <a name="odj_provision_data-structure"></a>Estrutura de ODJ_PROVISION_DATA

Especifica a estrutura de serialização mais externa usada pelas APIs de ingresso no domínio offline.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Membros

### <a name="ulversion"></a>ulVersion

Isso deve ser definido como 1.

### <a name="ulcblobs"></a>ulcBlobs

Isso deve ser definido como o número de elementos na matriz pBlobs.

### <a name="pblobs"></a>pBlobs

Aponta para uma matriz de estruturas de ODJ_BLOB.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_blob ODJ**](odj-odj_blob.md)


