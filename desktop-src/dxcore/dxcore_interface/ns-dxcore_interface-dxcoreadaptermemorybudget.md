---
title: DXCoreAdapterMemoryBudget
description: Descreve o orçamento de memória para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454303"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>Estrutura DXCoreAdapterMemoryBudget

Especifica o estado do adaptador <em>AdapterMemoryBudget</em> , que recupera ou solicita o orçamento de memória do adaptador no adaptador. A configuração (solicitando) um orçamento representa a memória física mínima necessária a ser reservada, em bytes, no adaptador. Recomendamos que você defina uma reserva de adaptador para denotar a quantidade de memória física que seu aplicativo não pode acessar sem. Esse valor ajuda o sistema operacional (SO) a minimizar rapidamente o impacto de grandes situações de pressão de memória.

Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo **DXCoreAdapterMemoryBudget** para *OUTPUTBUFFER*.

Ao chamar [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo **uint64_t** para *inputData*.

## <a name="syntax"></a>Sintaxe

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Membros

### <a name="budget"></a>visto

Tipo: **uint64_t**

Especifica o orçamento de memória do adaptador fornecido pelo sistema operacional, em bytes, que seu aplicativo deve ter como destino. Se *currentUsage* for maior que o *orçamento*, seu aplicativo poderá incorrer em penalidades de desempenho ou em virtude da atividade em segundo plano pelo sistema operacional, que tem o objetivo de fornecer a outros aplicativos um uso justo da memória do adaptador.

### <a name="currentusage"></a>currentUsage

Tipo: **uint64_t**

Especifica o uso de memória do adaptador atual do aplicativo, em bytes.

### <a name="availableforreservation"></a>availableForReservation

Tipo: **uint64_t**

Especifica a quantidade de memória do adaptador, em bytes, que seu aplicativo está disponível para reserva. Para reservar essa memória do adaptador, o aplicativo deve chamar [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) com o *estado* definido como [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>currentReservation

Tipo: **uint64_t**

Especifica a quantidade de memória do adaptador, em bytes, reservada pelo seu aplicativo. O sistema operacional usa a reserva como uma dica para determinar o conjunto de trabalho mínimo de seu aplicativo. Seu aplicativo deve tentar garantir que o uso de memória do adaptador possa ser cortado para atender a esse requisito.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)