---
description: Um float que representa o ponto final paramétrica atual para o raio.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793232"
---
# <a name="raytcurrent"></a><span data-ttu-id="24d8d-103">RayTCurrent</span><span class="sxs-lookup"><span data-stu-id="24d8d-103">RayTCurrent</span></span>

<span data-ttu-id="24d8d-104">Um float que representa o ponto final paramétrica atual para o raio.</span><span class="sxs-lookup"><span data-stu-id="24d8d-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="24d8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24d8d-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="24d8d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="24d8d-106">Remarks</span></span>

<span data-ttu-id="24d8d-107">**RayTCurrent** define o ponto final atual do raio de acordo com a seguinte fórmula: origem + (direção \* RayTCurrent).</span><span class="sxs-lookup"><span data-stu-id="24d8d-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="24d8d-108">A *origem* e a *direção* podem estar no espaço do mundo ou do objeto, o que resulta em um ponto de extremidade de espaço de objeto ou em um mundo.</span><span class="sxs-lookup"><span data-stu-id="24d8d-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="24d8d-109">**RayTCurrent** é inicializado na chamada Call [**TraceRay**](traceray-function.md) com o valor [**RayDesc:: tmax**](raydesc.md) e, em seguida, é atualizado durante a consulta de rastreamento, pois as interseções são relatadas (em qualquer um deles) e aceitas.</span><span class="sxs-lookup"><span data-stu-id="24d8d-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="24d8d-110">No [sombreador de interseção](intersection-shader.md), ele representa a distância para a interseção mais próxima encontrada até o momento.</span><span class="sxs-lookup"><span data-stu-id="24d8d-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="24d8d-111">Ele será atualizado após () para o valor de THit fornecido se o pressionamento tiver sido aceito.</span><span class="sxs-lookup"><span data-stu-id="24d8d-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="24d8d-112">No [sombreador qualquer clique](any-hit-shader.md), ele representa a distância para a interseção atual que está sendo relatada.</span><span class="sxs-lookup"><span data-stu-id="24d8d-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="24d8d-113">No [sombreador de clique mais próximo](closest-hit-shader.md), ele representa a distância para a interseção mais próxima aceita.</span><span class="sxs-lookup"><span data-stu-id="24d8d-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="24d8d-114">No [sombreador ausente](miss-shader.md), é igual a *tmax* passado para a chamada **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="24d8d-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="24d8d-115">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="24d8d-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="24d8d-116">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="24d8d-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="24d8d-117">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="24d8d-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="24d8d-118">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="24d8d-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="24d8d-119">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="24d8d-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="24d8d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="24d8d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d8d-121">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="24d8d-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




