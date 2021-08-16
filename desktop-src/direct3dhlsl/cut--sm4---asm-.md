---
title: recortar (sm4-ASM)
description: Instrução Geometry Shader que conclui a topologia primitiva atual (se algum vértice tiver sido emitido) e iniciará uma nova topologia do tipo declarado pelo sombreador Geometry.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908820"
---
# <a name="cut-sm4---asm"></a>recortar (sm4-ASM)

Instrução Geometry Shader que conclui a topologia primitiva atual (se algum vértice tiver sido emitido) e iniciará uma nova topologia do tipo declarado pelo sombreador Geometry.



| recortar |
|-----|



 

## <a name="remarks"></a>Comentários

Quando o **recorte** é executado, a primeira coisa que acontece é que qualquer topologia emitida anteriormente pela invocação do sombreador de geometria é concluída. Se não forem emitidos vértices suficientes para a topologia primitiva anterior, eles serão descartados. Como as únicas topologias de saída disponíveis para o sombreador Geometry são PointList, linestrip e Trianglestrip, nunca há vértices sobrantes após o **corte**.

Depois que a topologia anterior, se houver, for concluída, **Cut** fará com que uma nova topologia comece, usando a topologia declarada como a saída do sombreador de geometria.

## <a name="restrictions"></a>Restrições

-   A instrução **Cut** aplica-se somente ao sombreador Geometry.
-   **recortar** pode aparecer qualquer número de vezes no sombreador de geometria, incluindo dentro do controle de fluxo.
-   Se o sombreador de geometria terminar e os vértices tiverem sido emitidos, a topologia que ele está compilando será concluída, como se um **recorte** fosse executado como a última instrução.
-   Se os fluxos tiverem sido declarados, o [ \_ fluxo de recorte](cut-stream---sm5---asm-.md) deverá ser usado em vez de **recortado**.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




