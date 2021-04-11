---
title: DXCoreAdapterState
description: Define constantes que especificam tipos de Estados de adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294201"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="5456a-103">DXCoreAdapterState enum</span><span class="sxs-lookup"><span data-stu-id="5456a-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="5456a-104">Define constantes que especificam tipos de Estados de adaptador DXCore.</span><span class="sxs-lookup"><span data-stu-id="5456a-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="5456a-105">Passe uma dessas constantes para o método [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) para recuperar o item de estado do adaptador para um tipo de estado; Passe uma constante para o método [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) para definir as informações de um adaptador para um item de estado.</span><span class="sxs-lookup"><span data-stu-id="5456a-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="5456a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5456a-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="5456a-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="5456a-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="5456a-108">IsDriverUpdateInProgress</span><span class="sxs-lookup"><span data-stu-id="5456a-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="5456a-109">Especifica o estado do adaptador <em>IsDriverUpdateInProgress</em> , que `true` indica quando uma atualização de driver foi iniciada no adaptador, mas ainda não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5456a-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="5456a-110">Se a atualização do driver já tiver sido concluída, o adaptador será invalidado e a chamada de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) retornará um <b>HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span><span class="sxs-lookup"><span data-stu-id="5456a-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="5456a-111">Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o item de estado <em>IsDriverUpdateInProgress</em> tem o tipo <b>Uint8_t</b>, representando um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="5456a-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="5456a-112"><b>Importante</b>.</span><span class="sxs-lookup"><span data-stu-id="5456a-112"><b>Important</b>.</span></span> <span data-ttu-id="5456a-113">Este item de estado não tem suporte para [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span><span class="sxs-lookup"><span data-stu-id="5456a-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="5456a-114">AdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="5456a-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="5456a-115">Especifica o estado do adaptador <em>AdapterMemoryBudget</em> , que recupera ou solicita o orçamento de memória do adaptador no adaptador.</span><span class="sxs-lookup"><span data-stu-id="5456a-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="5456a-116">Ao chamar [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), o estado do adaptador <em>AdapterMemoryBudget</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* e o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> para *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="5456a-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="5456a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5456a-117">See also</span></span>

<span data-ttu-id="5456a-118">[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="5456a-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>