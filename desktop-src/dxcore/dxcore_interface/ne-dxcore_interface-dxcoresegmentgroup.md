---
title: DXCoreSegmentGroup
description: Define constantes que especificam o agrupamento de segmentos de memória de um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105816043"
---
# <a name="dxcoresegmentgroup-enum"></a>DXCoreSegmentGroup enum

Define constantes que especificam o agrupamento de segmentos de memória de um adaptador.

## <a name="syntax"></a>Syntax

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

## <a name="see-also"></a>Consulte também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)