---
title: Estágio do sombreador de vértice
description: O estágio vs (sombreador de vértice) processa vértices do assembler de entrada, executando operações por vértice, como transformações, reticente, decodagem e iluminação por vértice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3815f4c26c97e68ac0b4b20b72849052710f2f6adc0722bb3e42f5c8bf7a1c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530404"
---
# <a name="vertex-shader-stage"></a>Estágio do sombreador de vértice

O estágio vs (sombreador de vértice) processa vértices do assembler de entrada, executando operações por vértice, como transformações, reticente, decodagem e iluminação por vértice. Os sombreadores de vértice sempre operam em um vértice de entrada único e produzem um vértice de saída único. O estágio do sombreador de vértice sempre deve estar ativo para que o pipeline seja executado. Se nenhuma modificação de vértice ou transformação for necessária, um sombreador de vértice de passagem deve ser criado e definido para o pipeline.

## <a name="the-vertex-shader"></a>O sombreador de vértice

Cada vértice de entrada do sombreador de vértice pode ser composto por até 16 vetores de 32 bits (até quatro componentes cada) e cada vértice de saída pode ser composto por até 16 vetores de 4 componentes de 32 bits. Todos os sombreadores de vértice devem ter pelo menos uma entrada e uma saída, que podem ter um valor escalar.

O estágio de sombreador de vértice pode consumir dois valores gerados pelo sistema do assembler de entrada: VertexID e InstanceID (consulte Valores do sistema e semântica). Como VertexID e InstanceID são significativos a um nível de vértice, as IDs geradas pelo hardware podem somente ser alimentadas no primeiro estágio que as entende, esses valores de ID só podem ser alimentados no estágio de sombreador de vértice.

Os sombreadores de vértice sempre são executados em todos os vértices, incluindo vértices adjacentes nas topologias primitivas de entrada com adjacência. O número de vezes que o sombreador de vértice foi executado pode ser consultado na CPU usando a estatística de pipeline VSInvocations.

Um sombreador de vértice pode executar operações de amostragem de textura e carregamento onde não há necessidade de elementos derivados do espaço da tela (usando funções intrínsecas do HLSL: [amostra (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SampleCmpLevelZero (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero), e [SampleGrad (objeto de textura do DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 