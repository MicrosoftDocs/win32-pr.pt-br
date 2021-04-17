---
description: Um sombreador que chama TraceRay para gerar raios.
ms.assetid: ''
title: Sombreador da geração de raio
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
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797670"
---
# <a name="ray-generation-shader"></a>Sombreador da geração de raio

Um sombreador que chama [**TraceRay**](traceray-function.md) para gerar raios. O payload de Ray definido pelo usuário inicial para cada raio é fornecido ao site de chamada do **TraceRay** .  [**CallShader**](callshader-function.md) também pode ser usado em sombreadores de geração de Ray para invocar os [sombreadores](callable-shader.md)que podem ser chamados.

**DispatchRays** invoca uma grade de invocações de sombreador de Ray Generation.  Cada invocação (thread) de um sombreador de geração de Ray sabe seu local na grade geral, pode gerar raios arbitrários por meio de [**TraceRay**](traceray-function.md)e opera independentemente de outras invocações. Não há nenhuma ordem definida de execução de threads em relação umas com as outras.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("raygeneration")]
```



## <a name="example"></a>Exemplo

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




