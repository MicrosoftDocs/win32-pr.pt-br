---
title: Estágio do sombreador Geometry
description: O estágio Geometry-Shader (GS) executa o código do sombreador especificado pelo aplicativo com vértices como entrada e a capacidade de gerar vértices na saída.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3099ed5ede8dd89dc607ed838ff6e3fabfb16a69
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335360"
---
# <a name="geometry-shader-stage"></a>Estágio do sombreador Geometry

O estágio Geometry-Shader (GS) executa o código do sombreador especificado pelo aplicativo com vértices como entrada e a capacidade de gerar vértices na saída.

## <a name="the-geometry-shader"></a>O sombreador Geometry

Ao contrário dos sombreadores de vértice, que operam em um único vértice, as entradas do sombreador de geometria são os vértices de um primitivo completo (dois vértices para linhas, três vértices para triângulos ou um único vértice para ponto). Os sombreadores de geometria também podem trazer os dados de vértice para os primitivos adjacentes de borda como entrada (dois vértices adicionais para uma linha, três adicionais para um triângulo). A ilustração a seguir mostra um triângulo e uma linha com vértices adjacentes.

![ilustração de um triângulo e uma linha com vértices adjacentes](images/d3d10-gs.png)

|     | Tipo                |
|-----|-----------------|
| **TV**  | Vértice do triângulo |
| **AV**  | Vértice adjacentes |
| **LV**  | Vértice de linha     |



 

O estágio Geometry-Shader pode consumir o \_ [valor gerado pelo sistema](d3d10-graphics-programming-guide-input-assembler-stage-using.md) da VA primitivaid que é gerado automaticamente pelo ia. Isso permite que os dados por primitivo sejam buscados ou calculados, se desejado.

O estágio Geometry-Shader é capaz de produzir vários vértices que formam uma única topologia selecionada (as topologias de saída do estágio GS disponíveis são: tristrip, linestrip e PointList). O número de primitivos emitidos pode variar livremente dentro de qualquer chamada do sombreador de geometria, embora o número máximo de vértices que podem ser emitidos deva ser declarado estaticamente. Os tamanhos de faixa emitidos a partir de uma chamada de sombreador de geometria podem ser arbitrários, e novas faixas podem ser criadas por meio da função HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip).

A saída do sombreador de geometria pode ser alimentada no estágio do rasterizador e/ou em um buffer de vértice na memória através do estágio de saída de fluxo. A saída alimentada na memória é expandida em listas de linhas/pontos/triângulos individuais (exatamente da forma como seriam passados para o rasterizador).

Quando um sombreador de geometria está ativo, ele é chamado uma vez para cada primitivo passado para baixo ou gerado anteriormente no pipeline. Cada invocação do sombreador de geometria vê como entrada os dados para a invocação do primitivo, independentemente de ser um único ponto, uma única linha ou um único triângulo. Uma faixa de triângulos de versões anteriores no pipeline resultaria em uma chamada de sombreador de geometria de cada triângulo individual na faixa (como se a faixa fosse expandida em uma lista de triângulos). Todos os dados de entrada para cada vértice no primitivo individual estão disponíveis (ou seja, três vértices para triângulo), além de dados de vértice adjacentes, se aplicável/disponíveis.

Um sombreador de geometria produz um vértice de dados por vez, acrescentando vértices a um objeto de fluxo de saída. A topologia dos fluxos é determinada por uma declaração fixa, escolhendo um destes: PointStream, LineStream ou TriangleStream como a saída para o estágio GS. Há três tipos de objetos de fluxo disponíveis, PointStream, LineStream e TriangleStream que são todos os objetos modelo. A topologia da saída é determinada pelo seu tipo de objeto correspondente, enquanto o formato dos vértices acrescentado ao fluxo é determinado pelo tipo de modelo. A execução de uma instância do sombreador de geometria é atômica das outras chamadas, exceto pelo fato dos dados adicionados aos fluxos serem seriais. As saídas de uma determinada chamada de um sombreador de geometria são independentes de outras chamadas (porém a ordem é respeitada). Um sombreador de geometria gerando faixas de triângulos iniciará uma faixa tira em cada chamada.

Quando uma saída de sombreador de geometria é identificada como um valor interpretado do sistema (por exemplo, \_ RenderTargetArrayIndex de VA ou posição de VA \_ ), o hardware examina esses dados e executa algum comportamento dependente do valor, além de ser capaz de passar os dados em si para o próximo estágio de sombreamento para entrada. Quando essa saída de dados do sombreador de geometria tem significado para o hardware por primitivo (como VA \_ RenderTargetArrayIndex ou VA \_ ViewportArrayIndex), em vez de por vértice (como a VA \_ ClipDistance \[ n \] ou a \_ posição da VA), os dados por primitivos são obtidos do vértice principal emitido para o primitivo.

Os primitivos parcialmente concluídos podem ser gerados pelo sombreador de geometria, se o sombreador de geometria terminar e o primitivo estiver incompleto. Primitivos incompletos são descartados silenciosamente. Isso é semelhante à maneira como o IA trata primitivos parcialmente concluídas.

O sombreador de geometria pode executar operações de amostragem de textura e carregamento onde não há necessidade de elementos derivados do espaço da tela (samplelevel, samplecmplevelzero, samplegrad).

Os algoritmos que podem ser implementados no sombreador de geometria incluem:

-   Expansão de sprites de ponto
-   Sistemas de partículas dinâmicas
-   Geração de pele/barbatana
-   Geração de volume de sombra
-   Única passagem de renderização para Cubemap
-   Troca de material por primitivo
-   Configuração de material do Per-Primitive-incluindo a geração de coordenadas barycentric como dados primitivos para que um sombreador de pixel possa executar a interpolação de atributo personalizado (para obter um exemplo de interpolação normal de ordem superior, consulte o [exemplo de CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 