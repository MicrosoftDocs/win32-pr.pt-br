---
description: O pipeline programável do Direct3D 10 foi projetado para gerar gráficos para aplicativos de jogos em tempo real. O diagrama a seguir mostra o fluxo de dados de entrada para saída por meio de cada um dos estágios programáveis.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Estágios de pipeline (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942e2594f1f2eeb83f92b3ee517804a68b6074d85bf5c9205828a08e024112df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119967"
---
# <a name="pipeline-stages-direct3d-10"></a>Estágios de pipeline (Direct3D 10)

O pipeline programável do Direct3D 10 foi projetado para gerar gráficos para aplicativos de jogos em tempo real. O diagrama a seguir mostra o fluxo de dados de entrada para saída por meio de cada um dos estágios programáveis.

![diagrama do fluxo de dados no pipeline programável do Direct3D 10](images/d3d10-pipeline-stages.png)

Todos os estágios podem ser configurados usando a API. Os estágios que apresentam núcleos de sombreamento comuns (os blocos retangulares arredondados) são programáveis usando a linguagem de programação HLSL. Como você verá, isso torna o pipeline extremamente flexível e adaptável. A finalidade de cada um dos estágios é listada abaixo.

-   [Entrada – estágio do assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) -o estágio Input-Assembler é responsável por fornecer dados (triângulos, linhas e pontos) para o pipeline.
-   [Estágio do sombreador de vértice](https://www.bing.com/search?q=Vertex-Shader+Stage) – Esse estágio processa vértices, normalmente realizando operações como transformações, aplicação de capas e iluminação. Um sombreador de vértice sempre usa um único vértice de entrada para produzir um vértice de saída.
-   [Geometry-Shader Stage](https://www.bing.com/search?q=Geometry-Shader+Stage) -o estágio Geometry-Shader processa primitivos inteiros. Sua entrada é um primitivo completo (que é três vértices para um triângulo, dois vértices para uma linha ou um único vértice para um ponto). Além disso, cada primitivo também pode incluir os dados de vértice de qualquer primitiva de borda adjacente. Isso pode incluir, no máximo, três vértices adicionais para um triângulo ou dois vértices adicionais para uma linha. O sombreador de geometria também dá suporte à amplificação e cancelamento de amplificação de geometria. Dado um primitivo de entrada, o sombreador de geometria pode descartar o primitivo ou emitir um ou mais primitivos novos.
-   [Fluxo-etapa de saída](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) – o estágio Stream-output é projetado para transmitir dados primitivos do pipeline para a memória de sua maneira para o rasterizador. Os dados podem ser transmitidos para fora do rasterizador e/ou passados para ele. Os dados transmitidos para a memória podem ser reenviados para o pipeline como dados de entrada ou lidos pela CPU.
-   [Estágio do rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) – o rasterizador é responsável pelo recorte de primitivas, preparação de primitivas para o sombreador de pixel e determinação de como invocar sombreadores de pixel.
-   [Estágio do sombreador de pixel](https://www.bing.com/search?q=Pixel-Shader+Stage) – Esse estágio recebe dados interpolados para uma primitiva e gera dados por pixel, como cor.
-   [Saída – estágio da mesclagem](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) -o estágio de mesclagem de saída é responsável por combinar vários tipos de dados de saída (valores de sombreador de pixel, profundidade e informações de estêncil) com o conteúdo dos buffers de destino de renderização e profundidade/estêncil para gerar o resultado final do pipeline.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
