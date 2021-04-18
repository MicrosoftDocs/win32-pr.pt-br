---
description: Os valores de largura, altura e profundidade da estrutura de D3D12_DISPATCH_RAYS_DESC especificada na chamada DispatchRays de origem.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760627"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="c8ad8-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="c8ad8-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="c8ad8-104">A largura, a altura e os valores de profundidade da estrutura desc de raios de expedição de D3D12 especificadas na chamada de [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) de origem. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ad8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8ad8-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="c8ad8-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8ad8-106">Remarks</span></span>

<span data-ttu-id="c8ad8-107">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="c8ad8-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="c8ad8-108">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="c8ad8-109">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="c8ad8-110">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="c8ad8-111">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="c8ad8-112">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="c8ad8-113">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="c8ad8-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8ad8-114">See also</span></span>

* [<span data-ttu-id="c8ad8-115">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c8ad8-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
