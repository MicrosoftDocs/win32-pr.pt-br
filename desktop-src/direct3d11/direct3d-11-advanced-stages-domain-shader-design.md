---
title: Como criar um sombreador de domínio
description: Este tópico mostra como criar um sombreador de domínio.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46733bc9147f67cf33a127d8254f16c5813d8ebc2f0cb96c2071ae15589e34bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566176"
---
# <a name="how-to-design-a-domain-shader"></a>Como criar um sombreador de domínio

Um sombreador de domínio é o terceiro de três estágios que trabalham juntos para implementar [o mosaico](direct3d-11-advanced-stages-tessellation.md). O sombreador de domínio gera a geometria da superfície dos pontos de controle transformados de um sombreador de chassi e as coordenadas UV. Este tópico mostra como criar um sombreador de domínio.

Um sombreador de domínio é invocado uma vez para cada ponto gerado pelo mosaico de função fixa. As entradas são as coordenadas UV W do ponto no patch, bem como todos os dados de saída do sombreador de chassi, incluindo pontos de controle e \[ \] constantes de patch. A saída é um vértice definido de qualquer maneira desejada. Se a saída estiver sendo enviada para o sombreador de pixel, a saída deverá incluir uma posição (denotada com uma semântica \_ de Posição SV).

**Para criar um sombreador de domínio**

1.  Defina o atributo de domínio.

    ```
    [domain("quad")]
    ```

    

    O domínio é definido para um patch quad.

2.  Declare o local no chassi com o valor [do sistema de localização](/windows/desktop/direct3dhlsl/sv-domainlocation) de domínio.

    -   Para um patch quad, use um float2.
    -   Para um patch tri, use um float3 (para coordenadas centradas em barras)
    -   Para uma isoline, use um float2.

    Portanto, o local de domínio para um patch quad tem esta aparência:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Defina as outras entradas.

    As outras entradas vêm do sombreador de chassi e são definidas pelo usuário. Isso inclui os pontos de controle de entrada para patch, dos quais pode haver entre 1 e 32 pontos e dados constantes de patch de entrada.

    Os pontos de controle são definidos pelo usuário, geralmente com uma estrutura como esta (definida em [Como criar um sombreador de chassi](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Os dados constantes de patch também são definidos pelo usuário e podem ser parecidos com este (definido em [Como criar um sombreador de chassi):](direct3d-11-advanced-stages-hull-shader-design.md)

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Adicionar código definido pelo usuário para calcular as saídas; isso com torna o corpo do sombreador de domínio.

    Essa estrutura contém saídas do sombreador de domínio definido pelo usuário.

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

    

    A função pega cada UV de entrada (do mosaico) e avalia o patch do Bezier nessa posição.

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

    

    A função é invocada uma vez para cada ponto gerado pelo mosaico de função fixa. Como este exemplo usa um patch quad, o local do domínio de entrada ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) é um float2 (UV); um patch tri teria um local de entrada float3 (coordenadas centradas em UVW) e uma isoline teria um local de domínio de entrada float2.

    As outras entradas para a função vêm diretamente do sombreador de chassi. Neste exemplo, são 16 pontos de controle cada um sendo um PONTO DE CONTROLE **\_ \_ BEZIER,** bem como dados constantes de patch ( SAÍDA DE DADOS **\_ CONSTANTES \_ \_ do HS).** A saída é um vértice que contém todos os dados desejados – **DS \_ OUTPUT** neste exemplo.

Depois de criar um sombreador de domínio, [consulte Como criar um sombreador de domínio.](direct3d-11-advanced-stages-domain-shader-create.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 