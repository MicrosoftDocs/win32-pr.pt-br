---
description: Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora).
ms.assetid: ''
title: Sombreador de interseção
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786308"
---
# <a name="intersection-shader"></a><span data-ttu-id="10cf5-103">Sombreador de interseção</span><span class="sxs-lookup"><span data-stu-id="10cf5-103">Intersection Shader</span></span>

<span data-ttu-id="10cf5-104">Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora).</span><span class="sxs-lookup"><span data-stu-id="10cf5-104">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span> 

<span data-ttu-id="10cf5-105">O sombreador de interseção não tem acesso à carga Ray, mas define os atributos de interseção para cada um deles através de uma chamada para [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="10cf5-105">The intersection shader does not have access to the ray payload, but defines the intersection attributes for each hit through a call to [**ReportHit**](reporthit-function.md).</span></span>  <span data-ttu-id="10cf5-106">O tratamento de **ReportHit** pode parar o sombreador de interseção cedo, se o **sinalizador Ray Flag ray \_ \_ aceitar \_ primeiro \_ HIT_ \AND \_ \END \_ Search** estiver definido ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) for chamado de um sombreador any.</span><span class="sxs-lookup"><span data-stu-id="10cf5-106">The handling of **ReportHit** may stop the intersection shader early, if the ray flag **RAY\_FLAG\_ACCEPT\_FIRST\_HIT_\AND\_\END\_SEARCH** is set, or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) is called from an any hit shader.</span></span>  <span data-ttu-id="10cf5-107">Caso contrário, retornará true se o pressionamento for aceito ou false se o pressionamento for rejeitado.</span><span class="sxs-lookup"><span data-stu-id="10cf5-107">Otherwise, it returns true if the hit was accepted or false if the hit was rejected.</span></span>  <span data-ttu-id="10cf5-108">Isso significa que um sombreador qualquer clique, se presente, deve ser executado antes que o controle retorne condicionalmente para o sombreador de interseção.</span><span class="sxs-lookup"><span data-stu-id="10cf5-108">This means that an any hit shader, if present, must execute before control conditionally returns to the intersection shader.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="10cf5-109">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="10cf5-109">Shader Type attribute</span></span>


```
[shader("intersection")]
```



## <a name="example"></a><span data-ttu-id="10cf5-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10cf5-110">Example</span></span>

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




