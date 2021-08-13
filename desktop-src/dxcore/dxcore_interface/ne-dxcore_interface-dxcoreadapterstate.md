---
title: DXCoreAdapterState
description: Define constantes que especificam tipos de Estados de adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6878aaccb61fd164fcf834561fcf70f13d2609de595687b6ef6301778c87f81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367076"
---
# <a name="dxcoreadapterstate-enum"></a>DXCoreAdapterState enum

Define constantes que especificam tipos de Estados de adaptador DXCore. Passe uma dessas constantes para o método [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) para recuperar o item de estado do adaptador para um tipo de estado; Passe uma constante para o método [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) para definir as informações de um adaptador para um item de estado.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Constantes

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Especifica o estado do adaptador <em>IsDriverUpdateInProgress</em> , que `true` indica quando uma atualização de driver foi iniciada no adaptador, mas ainda não foi concluída. Se a atualização do driver já tiver sido concluída, o adaptador será invalidado e a chamada de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) retornará um <b>HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o item de estado <em>IsDriverUpdateInProgress</em> tem o tipo <b>Uint8_t</b>, representando um valor booliano.

<b>Importante</b>. Este item de estado não tem suporte para [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Especifica o estado do adaptador <em>AdapterMemoryBudget</em> , que recupera ou solicita o orçamento de memória do adaptador no adaptador.

Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> para *OUTPUTBUFFER*.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)