---
title: DXCoreSegmentGroup
description: Define constantes que especificam o agrupamento de segmentos de memória de um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279618"
---
# <a name="dxcoresegmentgroup-enum"></a>DXCoreSegmentGroup enum

Define constantes que especificam o agrupamento de segmentos de memória de um adaptador.

## <a name="syntax"></a>Sintaxe

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Constantes

### <a name="local"></a>Local

Especifica um agrupamento de segmentos que é considerado local para o adaptador e representa a memória mais rápida disponível para a GPU. Seu aplicativo deve ter como destino o grupo de segmentos local como o tamanho de destino para seu conjunto de trabalho.

### <a name="nonlocal"></a>Diagnóstico não locais

Especifica um agrupamento de segmentos que é considerado não local para o adaptador e pode ter um desempenho mais lento do que o grupo de segmentos local.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)