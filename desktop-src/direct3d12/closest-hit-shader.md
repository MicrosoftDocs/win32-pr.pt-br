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
ms.openlocfilehash: 6560ceb072307d52c45fca208bd95c5af2f3c39dd7f51215b5a4ac8a754b3c5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808258"
---
# <a name="closest-hit-shader"></a>Sombreador do clique mais próximo

Um sombreador que é invocado quando está habilitado e a visita mais próxima foi determinada ou Ray a pesquisa de interseção terminou. Esse sombreador é onde o sombreamento de superfície e a geração de Ray adicional ocorrerão normalmente.  Os sombreadores de tecle mais próximos devem declarar um parâmetro de carga, seguido por um parâmetro Attributes.  Cada um deve ser um tipo de estrutura definido pelo usuário que corresponda a tipos usados para [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) , respectivamente, ou a [**estrutura de atributos de interseção**](intersection-attributes.md) quando a interseção de triângulo de função fixa é usada.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("closesthit")]
```



## <a name="example"></a>Exemplo

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

 

 




