---
description: Um sombreador que é invocado quando está habilitado e a visita mais próxima foi determinada ou Ray a pesquisa de interseção terminou.
ms.assetid: ''
title: Sombreador do clique mais próximo
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
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764984"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="c95c3-103">Sombreador do clique mais próximo</span><span class="sxs-lookup"><span data-stu-id="c95c3-103">Closest Hit Shader</span></span>

<span data-ttu-id="c95c3-104">Um sombreador que é invocado quando está habilitado e a visita mais próxima foi determinada ou Ray a pesquisa de interseção terminou.</span><span class="sxs-lookup"><span data-stu-id="c95c3-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="c95c3-105">Esse sombreador é onde o sombreamento de superfície e a geração de Ray adicional ocorrerão normalmente.</span><span class="sxs-lookup"><span data-stu-id="c95c3-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="c95c3-106">Os sombreadores de tecle mais próximos devem declarar um parâmetro de carga, seguido por um parâmetro Attributes.</span><span class="sxs-lookup"><span data-stu-id="c95c3-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="c95c3-107">Cada um deve ser um tipo de estrutura definido pelo usuário que corresponda a tipos usados para [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) , respectivamente, ou a [**estrutura de atributos de interseção**](intersection-attributes.md) quando a interseção de triângulo de função fixa é usada.</span><span class="sxs-lookup"><span data-stu-id="c95c3-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="c95c3-108">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c95c3-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="c95c3-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c95c3-109">Example</span></span>

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




