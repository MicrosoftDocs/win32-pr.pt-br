---
title: Pipeline de gráficos
description: Esta seção descreve o pipeline programável do Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8e6b0b4d249c46dafe960f4f25a9a7598d6e2c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366933"
---
# <a name="graphics-pipeline"></a>Pipeline de gráficos

O pipeline programável do Direct3D 11 foi projetado para gerar gráficos para aplicativos de jogos em tempo real. Esta seção descreve o pipeline programável do Direct3D 11. O diagrama a seguir mostra o fluxo de dados de entrada para saída por meio de cada um dos estágios programáveis.

![diagrama do fluxo de dados no pipeline programável do direct3d 11](images/d3d11-pipeline-stages.jpg)

O pipeline de gráficos para o Microsoft Direct3D 11 dá suporte aos mesmos estágios que o [pipeline de gráficos do Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), com estágios adicionais para dar suporte a recursos avançados.

Você pode usar o 11API do Direct3D para configurar todos os estágios. Estágios que apresentam núcleos comuns de sombreador (os blocos retangulares arredondados) são programáveis usando a linguagem de programação [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl). Como você verá, isso torna o pipeline extremamente flexível e adaptável.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estágio de Assembler de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | A API do Direct3D 10 e superior separa áreas funcionais do pipeline em estágios; o primeiro estágio no pipeline é o estágio de IA (assembler de entrada).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Estágio do sombreador de vértice](vertex-shader-stage.md)<br/>                                      | O estágio Vertex-Shader (VS) processa os vértices do montador de entrada, executando operações por vértice, como transformações, aparências, metamorfose e iluminação por vértice. Os sombreadores de vértice sempre operam em um vértice de entrada único e produzem um vértice de saída único. O estágio do sombreador de vértice sempre deve estar ativo para que o pipeline seja executado. Se nenhuma modificação de vértice ou transformação for necessária, um sombreador de vértice de passagem deve ser criado e definido para o pipeline.<br/> |
| [Estágios de mosaico](direct3d-11-advanced-stages-tessellation.md)<br/>                 | O tempo de execução do Direct3D 11 dá suporte a três novos estágios que implementam mosaico, que converte as superfícies de subdivisão de detalhe baixo em primitivos de detalhes mais altos na GPU. O bloco de mosaico organiza (ou decompõe) as superfícies de ordem superior em estruturas adequadas para renderização.<br/>                                                                                                                                                                                                                 |
| [Estágio do sombreador Geometry](geometry-shader-stage.md)<br/>                                  | O estágio Geometry-Shader (GS) executa o código do sombreador especificado pelo aplicativo com vértices como entrada e a capacidade de gerar vértices na saída.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Fluxo-estágio de saída](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | A finalidade do estágio Stream-output é gerar continuamente (ou transmitir) dados de vértice do estágio Geometry-Shader (ou o estágio Vertex-Shader se o estágio Geometry-Shader estiver inativo) em um ou mais buffers na memória (consulte [introdução com o estágio Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)). <br/>                                                                                                                       |
| [Estágio de rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | O estágio de rasterização converte as informações de vetor (compostas de formas ou primitivas) em uma imagem de rasterizador (composta de pixels) para fins de exibição de gráficos 3D em tempo real. <br/>                                                                                                                                                                                                                                                                                                 |
| [Estágio do sombreador de pixel](pixel-shader-stage.md)<br/>                                        | O estágio pixel-shader (PS) permite técnicas de sombreamento avançadas, como iluminação por pixel e pós-processamento. Um sombreador de pixel é um programa que combina variáveis constantes, dados de textura, valores interpolados por vértice e outros dados para produzir saídas por pixel. O estágio do rasterizador invoca um sombreador de pixel uma vez para cada pixel coberto por um primitivo, no entanto, é possível especificar um sombreador **nulo** para evitar a execução de um sombreador.<br/>                                          |
| [Estágio de fusão de saída](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | O estágio de fusão de saída (OM) gera a cor de pixel renderizada final usando uma combinação de estado de pipeline, os dados de pixel gerados pelos sombreadores de pixel, o conteúdo dos destinos de renderização e o conteúdo dos buffers de profundidade/estêncil. O estágio OM é a etapa final para determinar quais pixels são visíveis (com o teste de estêncil de profundidade) e misturar as cores de pixel final.<br/>                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreador de computação](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

