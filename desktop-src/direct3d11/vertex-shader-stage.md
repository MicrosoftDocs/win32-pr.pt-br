---
title: Estágio do sombreador de vértice
description: O estágio Vertex-Shader (VS) processa os vértices do montador de entrada, executando operações por vértice, como transformações, aparências, metamorfose e iluminação por vértice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a291b4abed572da54f9a2616ce19e926e1c6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007576"
---
# <a name="vertex-shader-stage"></a>Estágio do sombreador de vértice

O estágio Vertex-Shader (VS) processa os vértices do montador de entrada, executando operações por vértice, como transformações, aparências, metamorfose e iluminação por vértice. Os sombreadores de vértice sempre operam em um vértice de entrada único e produzem um vértice de saída único. O estágio do sombreador de vértice sempre deve estar ativo para que o pipeline seja executado. Se nenhuma modificação de vértice ou transformação for necessária, um sombreador de vértice de passagem deve ser criado e definido para o pipeline.

## <a name="the-vertex-shader"></a>O sombreador de vértice

Cada vértice de entrada do sombreador de vértice pode ser composto de até quatro vetores de 16 32 bits (até 4 componentes cada) e cada vértice de saída pode ser composto de um número de vetores de componentes de 16 32 bits. Todos os sombreadores de vértice devem ter pelo menos uma entrada e uma saída, que podem ter um valor escalar.

O estágio Vertex-Shader pode consumir dois valores gerados pelo sistema do assembler de entrada: Vertexid e InstanceID (consulte valores do sistema e semântica). Como VertexID e InstanceID são significativos a um nível de vértice, as IDs geradas pelo hardware podem somente ser alimentadas no primeiro estágio que as entende, esses valores de ID só podem ser alimentados no estágio de sombreador de vértice.

Os sombreadores de vértice sempre são executados em todos os vértices, incluindo vértices adjacentes nas topologias primitivas de entrada com adjacência. O número de vezes que o sombreador de vértice foi executado pode ser consultado na CPU usando a estatística de pipeline VSInvocations.

Um sombreador de vértice pode executar operações de amostragem de textura e carregamento onde não há necessidade de elementos derivados do espaço da tela (usando funções intrínsecas do HLSL: [amostra (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SampleCmpLevelZero (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero), e [SampleGrad (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 