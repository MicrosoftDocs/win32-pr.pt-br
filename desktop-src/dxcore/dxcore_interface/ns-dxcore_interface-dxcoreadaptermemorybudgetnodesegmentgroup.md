---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Descreve um grupo de segmentos de memória para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366157"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>Estrutura DXCoreAdapterMemoryBudgetNodeSegmentGroup

Descreve um grupo de segmentos de memória para um adaptador.

## <a name="syntax"></a>Sintaxe

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Membros

### <a name="nodeindex"></a>nodeIndex

Tipo: **uint32_t**

Especifica o adaptador físico do dispositivo para o qual as informações de memória do adaptador são consultadas. Para uma operação de adaptador único, defina como zero. Se houver vários nós de adaptador, defina-o como o índice do nó (o adaptador físico do dispositivo) para o qual você deseja consultar as informações de memória do adaptador (consulte [sistemas de vários adaptadores](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>de segmento

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Especifica o agrupamento de segmentos de memória do adaptador que você deseja consultar.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md)

[Usar DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)

[Sistemas com vários adaptadores](../../direct3d12/multi-engine.md)