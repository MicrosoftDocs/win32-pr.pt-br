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
# <a name="ray-generation-shader"></a><span data-ttu-id="b2c3b-103">Sombreador da geração de raio</span><span class="sxs-lookup"><span data-stu-id="b2c3b-103">Ray Generation Shader</span></span>

<span data-ttu-id="b2c3b-104">Um sombreador que chama [**TraceRay**](traceray-function.md) para gerar raios.</span><span class="sxs-lookup"><span data-stu-id="b2c3b-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="b2c3b-105">O payload de Ray definido pelo usuário inicial para cada raio é fornecido ao site de chamada do **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="b2c3b-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="b2c3b-106">[**CallShader**](callshader-function.md) também pode ser usado em sombreadores de geração de Ray para invocar os [sombreadores](callable-shader.md)que podem ser chamados.</span><span class="sxs-lookup"><span data-stu-id="b2c3b-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="b2c3b-107">**DispatchRays** invoca uma grade de invocações de sombreador de Ray Generation.</span><span class="sxs-lookup"><span data-stu-id="b2c3b-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="b2c3b-108">Cada invocação (thread) de um sombreador de geração de Ray sabe seu local na grade geral, pode gerar raios arbitrários por meio de [**TraceRay**](traceray-function.md)e opera independentemente de outras invocações.</span><span class="sxs-lookup"><span data-stu-id="b2c3b-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="b2c3b-109">Não há nenhuma ordem definida de execução de threads em relação umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="b2c3b-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="b2c3b-110">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b2c3b-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="b2c3b-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b2c3b-111">Example</span></span>

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

 

 




