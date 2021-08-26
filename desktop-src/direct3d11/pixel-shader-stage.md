---
title: Estágio do Sombreador de Pixel
description: O PS (estágio de sombreador de pixel) permite técnicas avançadas de sombreamento, como iluminação por pixel e pós-processamento.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd58bbc55bbc2fb7d590036bceb061f2a304c0be16ff058d04f226021dfe3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988156"
---
# <a name="pixel-shader-stage"></a>Estágio do Sombreador de Pixel

O PS (estágio de sombreador de pixel) permite técnicas avançadas de sombreamento, como iluminação por pixel e pós-processamento. Um sombreador de pixel é um programa que combina variáveis constantes, dados de textura, valores interpolados por vértice e outros dados para produzir saídas por pixel. O estágio do rasterizador invoca um sombreador de pixel uma vez para cada pixel coberto por um primitivo, no entanto, é possível especificar um sombreador **NULL** para evitar a execução de um sombreador.

## <a name="the-pixel-shader"></a>O sombreador de pixel

Ao coletar várias amostras de uma textura, um sombreador de pixel é invocado uma vez quando ocorre um teste de profundidade/estêncil para as várias amostras cobertas. Amostras que passarem no teste de profundidade/estêncil serão atualizadas com a cor de saída do sombreador de pixel.

As funções intrínsecas do sombreador de pixel produzem ou usam derivadas de quantidades em relação ao espaço da tela x e y. O uso mais comum para derivadas é calcular o nível de detalhe para a amostragem de textura e, no caso de uma filtragem anisotrópica, selecionar amostras ao longo do eixo de anisotropia. Normalmente, uma implementação de hardware executa um sombreador de pixel em vários pixels (por exemplo, uma grade 2x2) ao mesmo tempo para que derivadas de quantidades calculadas no sombreador de pixel possam ser razoavelmente aproximadas como deltas dos valores no mesmo ponto de execução em pixels adjacentes.

### <a name="inputs"></a>Entradas

Quando o pipeline é configurado sem um sombreador de geometria, um sombreador de pixel é limitado a 16 entradas de 32 bits de 4 componentes. Caso contrário, um sombreador de pixel pode levar até 32 entradas de 32 bits de 4 componentes.

Os dados de entrada de sombreador de pixel incluem atributos de vértice (que podem ser interpolados com ou sem correção de perspectiva) ou podem ser tratados como constantes por primitivo. As entradas do sombreador de pixel são interpoladas dos atributos de vértice do primitivo que está sendo rasterizado, com base no modo de interpolação declarado. Se um primitivo for recortado antes da varredura, o modo de interpolação também será aplicado durante o processo de recorte.

Atributos de vértice são interpolados (ou avaliados) em locais de centro de sombreador de pixel. Modos de interpolação de atributo de sombreador de pixel são declarados em uma declaração de registro de entrada, de acordo com o elemento, em um [argumento](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) ou um [entrada estrutura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct). Os atributos podem ser interpolados linearmente ou com [amostragem de centroide](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx). A avaliação de centroides é relevante apenas durante a coleta de várias amostras para cobrir casos onde um pixel é coberto por um primitivo, mas um centro de pixel pode não estar; a avaliação de centroides ocorre o mais próximo possível do centro de pixel (não coberto).

Entradas também podem ser declaradas com uma [semântica de valor do sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), que marca um parâmetro que é consumido pelos outros estágios de pipeline. Por exemplo, uma posição de pixel deve ser marcada com a semântica \_ posição SV. O estágio ia pode produzir um escalar para um sombreador de pixel (usando SV PrimitiveID); o estágio de rasterizador também pode gerar um escalar para um \_ sombreador de pixel (usando SV \_ IsFrontFace).

### <a name="outputs"></a>outputs

Um sombreador de pixel pode gerar até 8 cores de 4 componentes de 32 bits, ou nenhuma cor se o pixel for descartado. Os componentes de registro de saída de sombreador de pixel devem ser declarados antes que possam ser usados; uma máscara de gravação de saída distinta é permitida para cada registro.

Use o estado de habilitação de gravação detalhada (no estágio de fusão de saída) para controlar se os dados de profundidade são gravados em um buffer de profundidade (ou use a instrução discard para descartar dados para esse pixel). Um sombreador de pixel também pode saída de um valor opcional de 32 bits, 1 componente, ponto flutuante, profundidade para teste de profundidade (usando a semântica de Profundidade \_ SV). O valor de profundidade tem saída no registro oDepth e substitui o valor de profundidade interpolado para teste de profundidade (supondo que o teste de profundidade está habilitado). Não há como alternar dinamicamente entre usar a profundidade de função fixa ou oDepth do sombreador.

Um sombreador de pixel não pode retornar um valor de estêncil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 