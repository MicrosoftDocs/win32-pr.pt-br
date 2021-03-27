---
title: Como criar um sombreador de domínio
description: Este tópico mostra como criar um sombreador de domínio.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084692"
---
# <a name="how-to-design-a-domain-shader"></a>Como criar um sombreador de domínio

Um sombreador de domínio é o terceiro de três estágios que trabalham em conjunto para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md). O sombreador de domínio gera a geometria da superfície dos pontos de controle transformados de um sombreador envoltória e das coordenadas UV. Este tópico mostra como criar um sombreador de domínio.

Um sombreador de domínio é invocado uma vez para cada ponto gerado pela função fixa Tessellator. As entradas são as \[ coordenadas UV W \] do ponto no patch, bem como todos os dados de saída do sombreador envoltória, incluindo pontos de controle e constantes de patch. A saída é um vértice definido de qualquer maneira desejada. Se a saída estiver sendo enviada para o sombreador de pixel, a saída deverá incluir uma posição (denotada com uma semântica de posição de VA \_ ).

**Para criar um sombreador de domínio**

1.  Defina o atributo de domínio.

    ```
    [domain("quad")]
    ```

    

    O domínio é definido para um patch quádruplo.

2.  Declare o local no envoltória com o valor do sistema de [local de domínio](/windows/desktop/direct3dhlsl/sv-domainlocation) .

    -   Para um patch quádruplo, use um float2.
    -   Para um patch Tri, use um float3 (para coordenadas barycentric)
    -   Para um Isoline, use um float2.

    Portanto, o local do domínio para um patch quádruplo tem esta aparência:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Defina as outras entradas.

    As outras entradas são provenientes do sombreador envoltória e são definidas pelo usuário. Isso inclui os pontos de controle de entrada para patch, dos quais pode haver entre 1 e 32 pontos e dados constantes de patch de entrada.

    Os pontos de controle são definidos pelo usuário, geralmente com uma estrutura como esta (definida em [How to: design a Shader envoltória](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Os dados constantes de patch também são definidos pelo usuário e podem ser semelhantes a este (definido em [como criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Adicionar código definido pelo usuário para computar as saídas; Isso constitui o corpo do sombreador de domínio.

    Essa estrutura contém saídas de sombreador de domínio definidas pelo usuário.

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    A função usa cada UV de entrada (do Tessellator) e avalia o patch Bezier nessa posição.

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    A função é invocada uma vez para cada ponto gerado pela função fixa Tessellator. Como este exemplo usa um patch quádruplo, o local do domínio de entrada ([VA \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) é um float2 (UV); um patch Tri teria um local de entrada float3 (coordenadas barycentric UVW) e um Isoline teria um local de domínio de entrada float2.

    As outras entradas para a função vêm do sombreador envoltória diretamente. Neste exemplo, é 16 pontos de controle, cada um sendo **um \_ \_ ponto de controle de Bézier**, bem como patches de dados constantes (**\_ \_ \_ saída de dados constante HS**). A saída é um vértice que contém qualquer **\_ saída** de dados desejada-DS neste exemplo.

Depois de criar um sombreador de domínio, consulte [como: criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-create.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 