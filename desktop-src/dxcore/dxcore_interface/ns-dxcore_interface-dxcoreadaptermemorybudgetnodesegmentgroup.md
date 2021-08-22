---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Descreve um grupo de segmentos de memória para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118650"
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

Especifica o adaptador físico do dispositivo para o qual as informações de memória do adaptador são consultadas. Para uma operação de adaptador único, defina como zero. Se houver vários nós de adaptador, defina-o como o índice do nó (o adaptador físico do dispositivo) para o qual você deseja consultar as informações de memória do adaptador (consulte [sistemas de vários adaptadores](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>de segmento

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Especifica o agrupamento de segmentos de memória do adaptador que você deseja consultar.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md)

[Usar DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)

[Sistemas com vários adaptadores](../../direct3d12/multi-engine.md)