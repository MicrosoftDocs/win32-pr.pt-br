---
description: Um float que representa o ponto de partida paramétrica atual para o raio.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762354"
---
# <a name="raytmin"></a><span data-ttu-id="02331-103">RayTMin</span><span class="sxs-lookup"><span data-stu-id="02331-103">RayTMin</span></span>

<span data-ttu-id="02331-104">Um float que representa o ponto de partida paramétrica atual para o raio.</span><span class="sxs-lookup"><span data-stu-id="02331-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="02331-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02331-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="02331-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="02331-106">Remarks</span></span>

<span data-ttu-id="02331-107">**RayTMin** define o ponto de partida do raio de acordo com a seguinte fórmula: origem + (direção \* RayTMin).</span><span class="sxs-lookup"><span data-stu-id="02331-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="02331-108">A *origem* e a *direção* podem estar no espaço do mundo ou do objeto, o que resulta em um ponto de partida do mundo ou do espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="02331-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="02331-109">**RayTMin** é especificado na chamada para [**TraceRay**](traceray-function.md)e é constante para a duração dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="02331-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="02331-110">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="02331-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="02331-111">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="02331-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="02331-112">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="02331-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="02331-113">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="02331-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="02331-114">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="02331-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="02331-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="02331-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02331-116">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="02331-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




