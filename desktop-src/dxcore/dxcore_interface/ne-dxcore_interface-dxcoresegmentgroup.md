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
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="6d1f3-103">DXCoreSegmentGroup enum</span><span class="sxs-lookup"><span data-stu-id="6d1f3-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="6d1f3-104">Define constantes que especificam o agrupamento de segmentos de memória de um adaptador.</span><span class="sxs-lookup"><span data-stu-id="6d1f3-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d1f3-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="6d1f3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6d1f3-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="6d1f3-107">Local</span><span class="sxs-lookup"><span data-stu-id="6d1f3-107">Local</span></span>

<span data-ttu-id="6d1f3-108">Especifica um agrupamento de segmentos que é considerado local para o adaptador e representa a memória mais rápida disponível para a GPU.</span><span class="sxs-lookup"><span data-stu-id="6d1f3-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="6d1f3-109">Seu aplicativo deve ter como destino o grupo de segmentos local como o tamanho de destino para seu conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6d1f3-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="6d1f3-110">Diagnóstico não locais</span><span class="sxs-lookup"><span data-stu-id="6d1f3-110">NonLocal</span></span>

<span data-ttu-id="6d1f3-111">Especifica um agrupamento de segmentos que é considerado não local para o adaptador e pode ter um desempenho mais lento do que o grupo de segmentos local.</span><span class="sxs-lookup"><span data-stu-id="6d1f3-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d1f3-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d1f3-112">See also</span></span>

<span data-ttu-id="6d1f3-113">[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="6d1f3-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>