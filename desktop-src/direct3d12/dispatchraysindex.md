---
description: Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor do sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrínseco.
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "105781349"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="2de27-103">DispatchRaysIndex </span><span class="sxs-lookup"><span data-stu-id="2de27-103">DispatchRaysIndex</span></span>

<span data-ttu-id="2de27-104">Obtém o local atual dentro da largura, altura e profundidade obtidas com o valor do sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrínseco.</span><span class="sxs-lookup"><span data-stu-id="2de27-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de27-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="2de27-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2de27-106">Remarks</span></span>

<span data-ttu-id="2de27-107">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing.</span><span class="sxs-lookup"><span data-stu-id="2de27-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="2de27-108">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="2de27-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="2de27-109">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="2de27-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="2de27-110">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="2de27-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="2de27-111">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="2de27-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="2de27-112">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="2de27-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="2de27-113">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="2de27-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="2de27-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de27-114">See also</span></span>

* [<span data-ttu-id="2de27-115">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2de27-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
