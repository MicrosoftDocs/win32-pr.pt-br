---
title: Como criar um sombreador envoltória
description: Este tópico mostra como criar um sombreador envoltória.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988657"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="ad290-103">Como criar um sombreador envoltória</span><span class="sxs-lookup"><span data-stu-id="ad290-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="ad290-104">Um sombreador envoltória é o primeiro de três estágios que trabalham juntos para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md) (os outros dois estágios são o Tessellator e um sombreador de domínio).</span><span class="sxs-lookup"><span data-stu-id="ad290-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="ad290-105">Este tópico mostra como criar um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="ad290-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="ad290-106">Um sombreador envoltória requer duas funções, o sombreador envoltória principal e uma função constante patch.</span><span class="sxs-lookup"><span data-stu-id="ad290-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="ad290-107">O sombreador envoltória implementa cálculos em cada ponto de controle; o sombreador envoltória também chama a função constante patch que implementa cálculos em cada patch.</span><span class="sxs-lookup"><span data-stu-id="ad290-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="ad290-108">Depois de criar um sombreador envoltória, consulte [como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-create.md) para saber como criar um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="ad290-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="ad290-109">**Para criar um sombreador envoltória**</span><span class="sxs-lookup"><span data-stu-id="ad290-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="ad290-110">Defina o controle de entrada do sombreador envoltória e os pontos de controle de saída.</span><span class="sxs-lookup"><span data-stu-id="ad290-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="ad290-111">Definir dados constantes de patch de saída.</span><span class="sxs-lookup"><span data-stu-id="ad290-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="ad290-112">Para um domínio Quad, a [VA \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) define 4 fatores de mosaico de borda (para incluír as bordas), já que a função Fixed Tessellator precisa saber o quanto a incluí.</span><span class="sxs-lookup"><span data-stu-id="ad290-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="ad290-113">As saídas necessárias são diferentes para os domínios de triângulo e Isoline.</span><span class="sxs-lookup"><span data-stu-id="ad290-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="ad290-114">A função Fixed Tessellator não examina nenhuma outra saída de sombreador envoltória, como outros dados de constante de patch ou qualquer um dos pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="ad290-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="ad290-115">O sombreador de domínio – que é invocado para cada ponto que a função fixa Tessellator gera--verá como entrada todos os pontos de controle de saída do sombreador envoltória e todos os dados constantes de patch de saída; o sombreador avalia o patch em seu local.</span><span class="sxs-lookup"><span data-stu-id="ad290-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="ad290-116">Defina uma função de constante de patch.</span><span class="sxs-lookup"><span data-stu-id="ad290-116">Define a patch constant function.</span></span> <span data-ttu-id="ad290-117">Uma função constante patch é executada uma vez para cada patch para calcular todos os dados que são constantes para todo o patch (em oposição aos dados de ponto por controle, que são calculados no sombreador envoltória).</span><span class="sxs-lookup"><span data-stu-id="ad290-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="ad290-118">As propriedades da função constante patch incluem:</span><span class="sxs-lookup"><span data-stu-id="ad290-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="ad290-119">Uma entrada especifica uma variável que contém uma ID de patch e é identificada pelo valor do sistema de **\_ primitiva de VA** (consulte a [semântica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) no modelo de sombreador 4).</span><span class="sxs-lookup"><span data-stu-id="ad290-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="ad290-120">Um parâmetro de entrada são os pontos de controle de entrada, declarados na **\_ saída do \_ ponto \_ de controle vs** neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="ad290-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="ad290-121">Uma função de patch pode ver todos os pontos de controle de entrada para cada patch, há 32 pontos de controle por patch neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="ad290-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="ad290-122">No mínimo, a função deve calcular os fatores de mosaico por patch para o estágio Tessellator que são identificados [com \_ TessFactor VA](/windows/desktop/direct3dhlsl/sv-tessfactor).</span><span class="sxs-lookup"><span data-stu-id="ad290-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="ad290-123">Um domínio Quad requer quatro fatores de mosaico para as bordas e dois fatores adicionais (identificados por [ \_ InsideTessFactor de VA](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) para o inclusão dentro do patch.</span><span class="sxs-lookup"><span data-stu-id="ad290-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="ad290-124">A função Fixed Tessellator não examina nenhuma outra saída do sombreador envoltória (como os dados constantes do patch ou qualquer um dos pontos de controle).</span><span class="sxs-lookup"><span data-stu-id="ad290-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="ad290-125">As saídas geralmente são definidas por uma estrutura e são identificadas **pela \_ \_ \_ saída de dados constantes HS** neste exemplo; a estrutura depende do tipo de domínio e seria diferente para domínios de triângulo ou Isoline.</span><span class="sxs-lookup"><span data-stu-id="ad290-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="ad290-126">Um sombreador de domínio, por outro lado, é invocado para cada ponto que a função fixa Tessellator gera e precisa ver os pontos de controle de saída e os dados constantes de patch de saída (tanto do sombreador envoltória) para avaliar um patch em seu local.</span><span class="sxs-lookup"><span data-stu-id="ad290-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="ad290-127">Defina um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="ad290-127">Define a hull shader.</span></span> <span data-ttu-id="ad290-128">Um sombreador envoltória identifica as propriedades de um patch, incluindo uma função constante patch.</span><span class="sxs-lookup"><span data-stu-id="ad290-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="ad290-129">Um sombreador envoltória é invocado uma vez para cada ponto de controle de saída.</span><span class="sxs-lookup"><span data-stu-id="ad290-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="ad290-130">Um sombreador envoltória usa os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="ad290-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="ad290-131">Um atributo de [domínio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .</span><span class="sxs-lookup"><span data-stu-id="ad290-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="ad290-132">Um atributo de [particionamento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .</span><span class="sxs-lookup"><span data-stu-id="ad290-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="ad290-133">Um atributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .</span><span class="sxs-lookup"><span data-stu-id="ad290-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="ad290-134">Um atributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .</span><span class="sxs-lookup"><span data-stu-id="ad290-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="ad290-135">Um atributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) .</span><span class="sxs-lookup"><span data-stu-id="ad290-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="ad290-136">Um sombreador envoltória calcula pontos de controle de saída, há 16 pontos de controle de Bezier de saída neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="ad290-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="ad290-137">Todos os pontos de controle de entrada (identificados pela saída do ponto de controle do vs) são visíveis para cada invocação de sombreador envoltória. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad290-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="ad290-138">Neste exemplo, há 32 pontos de controle de entrada.</span><span class="sxs-lookup"><span data-stu-id="ad290-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="ad290-139">Um sombreador envoltória é invocado uma vez por ponto de controle de saída (identificado com [ \_ OutputControlPointID VA](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) para cada patch (identificado com a \_ primitivaid de VA).</span><span class="sxs-lookup"><span data-stu-id="ad290-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="ad290-140">A finalidade deste sombreador específico é calcular a saída *i*, que foi definida para ser um ponto de controle de Bézier (Este exemplo tem 16 pontos de controle de saída definidos por outputcontrolpoints).</span><span class="sxs-lookup"><span data-stu-id="ad290-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="ad290-141">Um sombreador envoltória executa uma rotina uma vez por patch (a função constante patch) para computar dados de constante de patch (fatores de mosaico como um mínimo).</span><span class="sxs-lookup"><span data-stu-id="ad290-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="ad290-142">Separadamente, um sombreador envoltória executa uma função constante patch (chamada SubDToBezierConstantsHS) em cada patch para computar dados de constante de patches, como fatores de mosaico para o estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="ad290-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad290-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad290-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad290-144">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ad290-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="ad290-145">Visão geral do mosaico</span><span class="sxs-lookup"><span data-stu-id="ad290-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 