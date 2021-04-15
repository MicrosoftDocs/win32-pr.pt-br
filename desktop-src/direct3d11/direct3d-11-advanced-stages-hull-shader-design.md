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
# <a name="how-to-design-a-hull-shader"></a>Como criar um sombreador envoltória

Um sombreador envoltória é o primeiro de três estágios que trabalham juntos para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md) (os outros dois estágios são o Tessellator e um sombreador de domínio). Este tópico mostra como criar um sombreador envoltória.

Um sombreador envoltória requer duas funções, o sombreador envoltória principal e uma função constante patch. O sombreador envoltória implementa cálculos em cada ponto de controle; o sombreador envoltória também chama a função constante patch que implementa cálculos em cada patch.

Depois de criar um sombreador envoltória, consulte [como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-create.md) para saber como criar um sombreador envoltória.

**Para criar um sombreador envoltória**

1.  Defina o controle de entrada do sombreador envoltória e os pontos de controle de saída.

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

    

2.  Definir dados constantes de patch de saída.

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

    

    Para um domínio Quad, a [VA \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) define 4 fatores de mosaico de borda (para incluír as bordas), já que a função Fixed Tessellator precisa saber o quanto a incluí. As saídas necessárias são diferentes para os domínios de triângulo e Isoline.

    A função Fixed Tessellator não examina nenhuma outra saída de sombreador envoltória, como outros dados de constante de patch ou qualquer um dos pontos de controle. O sombreador de domínio – que é invocado para cada ponto que a função fixa Tessellator gera--verá como entrada todos os pontos de controle de saída do sombreador envoltória e todos os dados constantes de patch de saída; o sombreador avalia o patch em seu local.

3.  Defina uma função de constante de patch. Uma função constante patch é executada uma vez para cada patch para calcular todos os dados que são constantes para todo o patch (em oposição aos dados de ponto por controle, que são calculados no sombreador envoltória).

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

    

    As propriedades da função constante patch incluem:

    -   Uma entrada especifica uma variável que contém uma ID de patch e é identificada pelo valor do sistema de **\_ primitiva de VA** (consulte a [semântica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) no modelo de sombreador 4).
    -   Um parâmetro de entrada são os pontos de controle de entrada, declarados na **\_ saída do \_ ponto \_ de controle vs** neste exemplo. Uma função de patch pode ver todos os pontos de controle de entrada para cada patch, há 32 pontos de controle por patch neste exemplo.
    -   No mínimo, a função deve calcular os fatores de mosaico por patch para o estágio Tessellator que são identificados [com \_ TessFactor VA](/windows/desktop/direct3dhlsl/sv-tessfactor). Um domínio Quad requer quatro fatores de mosaico para as bordas e dois fatores adicionais (identificados por [ \_ InsideTessFactor de VA](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) para o inclusão dentro do patch. A função Fixed Tessellator não examina nenhuma outra saída do sombreador envoltória (como os dados constantes do patch ou qualquer um dos pontos de controle).
    -   As saídas geralmente são definidas por uma estrutura e são identificadas **pela \_ \_ \_ saída de dados constantes HS** neste exemplo; a estrutura depende do tipo de domínio e seria diferente para domínios de triângulo ou Isoline.

    Um sombreador de domínio, por outro lado, é invocado para cada ponto que a função fixa Tessellator gera e precisa ver os pontos de controle de saída e os dados constantes de patch de saída (tanto do sombreador envoltória) para avaliar um patch em seu local.

4.  Defina um sombreador envoltória. Um sombreador envoltória identifica as propriedades de um patch, incluindo uma função constante patch. Um sombreador envoltória é invocado uma vez para cada ponto de controle de saída.

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

    

    Um sombreador envoltória usa os seguintes atributos:

    -   Um atributo de [domínio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .
    -   Um atributo de [particionamento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .
    -   Um atributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .
    -   Um atributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .
    -   Um atributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) . Um sombreador envoltória calcula pontos de controle de saída, há 16 pontos de controle de Bezier de saída neste exemplo.

Todos os pontos de controle de entrada (identificados pela saída do ponto de controle do vs) são visíveis para cada invocação de sombreador envoltória. **\_ \_ \_** Neste exemplo, há 32 pontos de controle de entrada.

Um sombreador envoltória é invocado uma vez por ponto de controle de saída (identificado com [ \_ OutputControlPointID VA](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) para cada patch (identificado com a \_ primitivaid de VA). A finalidade deste sombreador específico é calcular a saída *i*, que foi definida para ser um ponto de controle de Bézier (Este exemplo tem 16 pontos de controle de saída definidos por outputcontrolpoints).

Um sombreador envoltória executa uma rotina uma vez por patch (a função constante patch) para computar dados de constante de patch (fatores de mosaico como um mínimo). Separadamente, um sombreador envoltória executa uma função constante patch (chamada SubDToBezierConstantsHS) em cada patch para computar dados de constante de patches, como fatores de mosaico para o estágio Tessellator.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 