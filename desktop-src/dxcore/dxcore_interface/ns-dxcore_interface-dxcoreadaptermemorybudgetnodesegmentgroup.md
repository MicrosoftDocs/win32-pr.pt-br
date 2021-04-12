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
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="0e20f-103">Estrutura DXCoreAdapterMemoryBudgetNodeSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="0e20f-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="0e20f-104">Descreve um grupo de segmentos de memória para um adaptador.</span><span class="sxs-lookup"><span data-stu-id="0e20f-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e20f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e20f-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="0e20f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0e20f-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="0e20f-107">nodeIndex</span><span class="sxs-lookup"><span data-stu-id="0e20f-107">nodeIndex</span></span>

<span data-ttu-id="0e20f-108">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="0e20f-108">Type: **uint32_t**</span></span>

<span data-ttu-id="0e20f-109">Especifica o adaptador físico do dispositivo para o qual as informações de memória do adaptador são consultadas.</span><span class="sxs-lookup"><span data-stu-id="0e20f-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="0e20f-110">Para uma operação de adaptador único, defina como zero.</span><span class="sxs-lookup"><span data-stu-id="0e20f-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="0e20f-111">Se houver vários nós de adaptador, defina-o como o índice do nó (o adaptador físico do dispositivo) para o qual você deseja consultar as informações de memória do adaptador (consulte [sistemas de vários adaptadores](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="0e20f-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="0e20f-112">de segmento</span><span class="sxs-lookup"><span data-stu-id="0e20f-112">segmentGroup</span></span>

<span data-ttu-id="0e20f-113">Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="0e20f-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="0e20f-114">Especifica o agrupamento de segmentos de memória do adaptador que você deseja consultar.</span><span class="sxs-lookup"><span data-stu-id="0e20f-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e20f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e20f-115">See also</span></span>

[<span data-ttu-id="0e20f-116">Referência de DXCore</span><span class="sxs-lookup"><span data-stu-id="0e20f-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="0e20f-117">Usar DXCore para enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="0e20f-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="0e20f-118">Sistemas com vários adaptadores</span><span class="sxs-lookup"><span data-stu-id="0e20f-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)