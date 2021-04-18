---
description: Um sombreador que é invocado quando Ray interseções não são opacas.
ms.assetid: ''
title: Sombreador de todos os cliques
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788768"
---
# <a name="any-hit-shader"></a><span data-ttu-id="ae238-103">Sombreador de todos os cliques</span><span class="sxs-lookup"><span data-stu-id="ae238-103">Any Hit Shader</span></span>

<span data-ttu-id="ae238-104">Um sombreador que é invocado quando Ray interseções não são opacas.</span><span class="sxs-lookup"><span data-stu-id="ae238-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="ae238-105">Qualquer sombreador de acesso deve declarar um parâmetro de carga seguido por um parâmetro Attributes.</span><span class="sxs-lookup"><span data-stu-id="ae238-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="ae238-106">Cada um desses parâmetros deve ser um tipo de estrutura definido pelo usuário tipos de correspondência usados para [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) , respectivamente, ou a [**estrutura de atributos de interseção**](intersection-attributes.md) quando a interseção de triângulo de função fixa é usada.</span><span class="sxs-lookup"><span data-stu-id="ae238-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="ae238-107">Qualquer sombreador de acesso pode executar os seguintes tipos de operações:</span><span class="sxs-lookup"><span data-stu-id="ae238-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="ae238-108">Ler e modificar a carga do Ray: (Inout payload_t rayPayload)</span><span class="sxs-lookup"><span data-stu-id="ae238-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="ae238-109">Ler os atributos de interseção: (em atributos de attr_t)</span><span class="sxs-lookup"><span data-stu-id="ae238-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="ae238-110">Chame [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), que aceita a visita atual, termina o [sombreador de qualquer clique](any-hit-shader.md), termina o [sombreador de interseção](intersection-shader.md) se houver um presente e executa o [sombreador de pressionamentos mais próximo](closest-hit-shader.md) no próximo acesso até o momento, se estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="ae238-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="ae238-111">Chame [**IgnoreHit**](ignorehit-function.md), que termina o sombreador de qualquer clique e informa ao sistema para continuar pesquisando ocorrências, incluindo o controle de retorno para um sombreador de interseção, se estiver em execução no momento, retornando false do site de chamada [**ReportHit**](reporthit-function.md)\*.</span><span class="sxs-lookup"><span data-stu-id="ae238-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="ae238-112">Return sem chamar nenhum desses intrínsecos, que aceita a ocorrência atual e informa ao sistema para continuar pesquisando ocorrências, incluindo o controle de retorno para o sombreador de interseção, se houver um, retornando true no site de chamada [**ReportHit**](reporthit-function.md) para indicar que o acerto foi aceito.</span><span class="sxs-lookup"><span data-stu-id="ae238-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="ae238-113">Mesmo que uma invocação de sombreador de clique seja encerrada por [**IgnoreHit**](ignorehit-function.md) ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), todas as modificações feitas na carga de Ray até o momento ainda devem ser retidas.</span><span class="sxs-lookup"><span data-stu-id="ae238-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="ae238-114">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ae238-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="ae238-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ae238-115">Example</span></span>

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
