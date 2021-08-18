---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA IDL Definition
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 02762a80be9bd60b7f9c8648c9bfb848f3d76184f249567c9e9522189692e0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064346"
---
# <a name="odj_provision_data-structure"></a>ODJ_PROVISION_DATA estrutura

Especifica a estrutura de serialização mais externa usada pelas APIs de junção de domínio offline.

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

Aponta para uma matriz de ODJ_BLOB estruturas.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)

[**ODJ \_ BLOB**](odj-odj_blob.md)


