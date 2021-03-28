---
title: cut_stream (SM5-ASM)
description: A instrução Geometry Shader que conclui a topologia primitiva atual no fluxo especificado, se quaisquer vértices tiverem sido emitidos para ele e iniciar uma nova topologia do tipo declarado pelo sombreador Geometry nesse fluxo.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365201"
---
# <a name="cut_stream-sm5---asm"></a>Recortar \_ fluxo (SM5-ASM)

A instrução Geometry Shader que conclui a topologia primitiva atual no fluxo especificado, se quaisquer vértices tiverem sido emitidos para ele e iniciar uma nova topologia do tipo declarado pelo sombreador Geometry nesse fluxo.



| Recortar \_ fluxo streamIndex |
|-------------------------|



 



| Item                                                                                                               | Descrição                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[no \] índice de fluxo.<br/> |



 

## <a name="remarks"></a>Comentários

Quando essa instrução é executada, qualquer topologia emitida anteriormente pela invocação do sombreador de geometria é concluída. Se não houver vértices suficientes emitidos para a topologia primitiva anterior, eles serão descartados. Como as únicas topologias de saída disponíveis para o sombreador Geometry são PointList, linestrip e Trianglestrip, nunca há vértices sobrantes.

*streamIndex* deve ser um valor imediato \[ 0.. 3 \] para um fluxo declarado.

Depois que a topologia anterior, se houver, for concluída, essa instrução fará com que uma nova topologia comece, usando a topologia declarada como a saída do sombreador de geometria.

### <a name="restrictions"></a>Restrições

-   Essa instrução aplica-se somente ao sombreador Geometry.
-   **recortar \_ fluxo** pode aparecer qualquer número de vezes no sombreador Geometry, incluindo dentro do controle de fluxo.
-   Se o sombreador de geometria terminar e os vértices tiverem sido emitidos, a topologia que ele está compilando será concluída, como se uma instrução **Cut \_ Stream** fosse executada como a última instrução.
-   Se os fluxos não tiverem sido declarados, você deverá usar [recortar](cut--sm4---asm-.md) em vez de **recortar \_ fluxo**.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





