---
title: Recursos do Direct3D 11
description: O guia de programação contém informações sobre como usar o pipeline programável do Direct3D 11 para criar gráficos 3D em tempo real para jogos e para aplicativos científicos e de área de trabalho.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008575"
---
# <a name="direct3d-11-features"></a>Recursos do Direct3D 11

O guia de programação contém informações sobre como usar o pipeline programável do Direct3D 11 para criar gráficos 3D em tempo real para jogos e para aplicativos científicos e de área de trabalho.

-   [Sombreador de computação](#compute-shader)
-   [Vinculação de sombreador dinâmico](#dynamic-shader-linking)
-   [Multithread](#multithreading)
-   [Mosaico](#tessellation)
-   [Lista completa de recursos](#full-listing-of-features)
-   [Recursos adicionados em versões anteriores](#features-added-in-previous-releases)
-   [Tópicos relacionados](#related-topics)

## <a name="compute-shader"></a>Sombreador de computação

Um sombreador de computação é um sombreador programável projetado para processamento paralelo de dados de uso geral. Em outras palavras, os sombreadores de computação permitem que uma GPU seja usada como um processador paralelo de finalidade geral. O sombreador de computação é semelhante aos outros sombreadores de pipeline programáveis (como vértice, pixel, geometria) no modo como ele acessa entradas e saídas. A tecnologia de sombreador de computação também é conhecida como a tecnologia DirectCompute. Um sombreador de computação é integrado ao Direct3D e pode ser acessado por meio de um dispositivo Direct3D. Ele pode compartilhar diretamente recursos de memória com sombreadores gráficos usando o dispositivo Direct3D. No entanto, ele não está conectado diretamente a outros estágios de sombreador.

Um sombreador de computação é projetado para aplicativos de mercado em massa que realizam cálculos em tarifas interativas, quando o custo de transição entre a API (e sua pilha de software associada) e uma CPU consumir muita sobrecarga.

Um sombreador de computação tem seu próprio conjunto de Estados. Um sombreador de computação não necessariamente tem um mapeamento de 1-1 forçado para registros de entrada (como um sombreador de vértice) ou registros de saída (como o sombreador de pixel). Há suporte para alguns recursos do sombreador de gráficos, mas outros foram removidos para que novos recursos específicos do sombreador de computação pudessem ser adicionados.

Para dar suporte aos recursos específicos do sombreador de computação, vários novos tipos de recursos agora estão disponíveis, como buffers de leitura/gravação, texturas e buffers estruturados.

Consulte [visão geral do sombreador de computação](direct3d-11-advanced-stages-compute-shader.md) para obter informações adicionais.

## <a name="dynamic-shader-linking"></a>Vinculação de sombreador dinâmico

Os sistemas de renderização devem lidar com complexidade significativa quando gerenciam sombreadores, ao mesmo tempo em que oferecem a oportunidade de otimizar o código do sombreador. Isso se torna um desafio ainda maior porque os sombreadores devem dar suporte a uma variedade de materiais diferentes em uma cena renderizada em várias configurações de hardware. Para resolver esse desafio, os desenvolvedores de sombreador costumam recorrer a uma das duas abordagens gerais. Eles criaram sombreadores de uso geral grandes e completos, que podem ser usados por uma ampla variedade de itens de cena, que compensam algum desempenho em relação à flexibilidade ou criamos sombreadores individuais para cada fluxo de geometria, tipo de material ou combinação de tipo claro necessário.

Esses sombreadores grandes de uso geral lidam com esse desafio recompilando o mesmo sombreador com definições de pré-processador diferentes, e o último método usa a capacidade de desenvolvedor de força bruta para obter o mesmo resultado. A explosão de permuta de sombreador muitas vezes foi um problema para os desenvolvedores que agora devem gerenciar milhares de permutações de sombreador diferentes no jogo e no pipeline de ativos.

O Direct3D 11 e o Shader Model 5 introduzem constructos de linguagem orientada a objeto e fornecem suporte em tempo de execução de vinculação de sombreador para ajudar os desenvolvedores de programadores.

Consulte [vinculação dinâmica](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) para obter informações adicionais.

## <a name="multithreading"></a>Multithreading

Muitos aplicativos gráficos são associados à CPU devido a atividades dispendiosas, como travessia de grafo de cena, classificação de objetos e simulações de física. Como os sistemas de vários núcleos estão se tornando cada vez mais disponíveis, o Direct3D 11 melhorou seu suporte multithreading para permitir uma interação eficiente entre vários threads de CPU e as APIs de gráficos de D3D11.

O Direct3D 11 permite a seguinte funcionalidade para dar suporte a multithreading:

-   Os objetos simultâneos agora são criados em threads separados, fazendo com que as funções de ponto de entrada que criam objetos de forma livre possibilitam que vários threads criem objetos simultaneamente. Por exemplo, um aplicativo agora pode compilar um sombreador ou carregar uma textura em um thread durante a renderização em outro.
-   As listas de comandos podem ser criadas em vários threads — uma lista de comandos é uma sequência gravada de comandos gráficos. Com o Direct3D 11, você pode criar listas de comandos em vários threads de CPU, o que permite a passagem paralela do banco de dados de cena ou do processamento de física em vários threads. Isso libera o thread de renderização principal para distribuir buffers de comando para o hardware.

Consulte [multithreading](overviews-direct3d-11-render-multi-thread.md) para obter informações adicionais.

## <a name="tessellation"></a>Mosaico

O mosaico pode ser usado para renderizar um único modelo com vários níveis de detalhes. Essa abordagem gera um modelo mais preciso e geométrico que depende do nível de detalhe necessário para uma cena. Use o mosaico em uma cena em que o nível de detalhe permite um modelo de geometria inferior, o que reduz a demanda de largura de banda de memória consumida durante a renderização.

No Direct3D, o mosaico é implementado na GPU para calcular uma superfície curva mais suave de um patch de entrada grosso (menos detalhado). Cada face de patch (quad ou triângulo) é subdividida em faces triangulares menores que melhoram a superfície que você deseja.

Para obter informações sobre como implementar o mosaico no pipeline de gráficos, consulte [visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md).

## <a name="full-listing-of-features"></a>Lista completa de recursos

Esta é uma lista completa dos recursos do Direct3D 11.

-   Você pode executar o Direct3D 11 no [hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md) especificando um [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) ao criar um dispositivo.
-   Você pode executar o mosaico (consulte [visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)) usando os seguintes tipos de sombreador:

    -   {1&gt;Sombreador Hull&lt;1}
    -   Sombreador de domínio

-   O Direct3D 11 dá suporte a multithreading (consulte [multithreading](overviews-direct3d-11-render-multi-thread.md))

    -   Recurso multithread/sombreador/criação de objeto
    -   Criação da lista de exibição multi-threaded

-   O Direct3D 11 expande os sombreadores com os seguintes recursos (consulte o [modelo do sombreador 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))

    -   Recursos endereçáveis – texturas, buffers de constantes e amostras
    -   Tipos de recursos adicionais, como buffers de leitura/gravação e texturas (consulte [novos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)).
    -   Sub-rotinas
    -   Sombreador de computação (consulte [visão geral do sombreador de computação](direct3d-11-advanced-stages-compute-shader.md)) – um sombreador que acelera os cálculos dividindo o espaço do problema entre vários threads de software ou grupos de threads e compartilhando dados entre os registros de sombreador para reduzir significativamente a quantidade de dados necessária para entrada em um sombreador. Os algoritmos que o sombreador de computação pode melhorar significativamente incluem o pós-processamento, a animação, a física e a inteligência artificial.
    -   Sombreador de geometria (consulte [recursos de sombreador de geometria](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))

        -   Instanciação – permite que o sombreador de geometria gere um máximo de 1024 vértices ou qualquer combinação de instâncias e vértices até 1024 (máximo de 32 instâncias de 32 vértices cada).

    -   Sombreador de pixel

        -   Cobertura como entrada de PS
        -   Interpolação programável de entradas – o sombreador de pixel pode avaliar atributos dentro do pixel, em qualquer lugar na grade de multiamostras
        -   A amostragem de atributos de centróide deve obedecer às seguintes regras:

            -   Se todos os exemplos no primitivo forem cobertos, o atributo será avaliado no centro do pixel, independentemente de o padrão de exemplo ter um local de exemplo no pixel Center.
            -   Caso contrário, o atributo será avaliado na primeira amostra coberta, ou seja, o exemplo com o índice mais baixo entre todos os índices de exemplo. Nessa situação, a cobertura de exemplo é determinada após a aplicação da operação AND lógica à cobertura e ao estado do rasterizador de máscara de exemplo.
            -   Se nenhum exemplo for coberto (como em pixels auxiliares que são executados fora dos limites de um primitivo para preencher carimbos de pixel 2x2), o atributo será avaliado de uma das seguintes maneiras:

                -   Se o estado do rasterizador de máscara de exemplo for um subconjunto dos exemplos no pixel, o primeiro exemplo coberto pelo estado do rasterizador de máscara de exemplo será o ponto de avaliação.
                -   Caso contrário, na condição de máscara de exemplo completa, o pixel Center é o ponto de avaliação.

-   O Direct3D 11 expande texturas (consulte a [visão geral das texturas](overviews-direct3d-11-resources-textures.md)) com os seguintes recursos

    -   Gather4

        -   Suporte para texturas de vários componentes – especifique um canal para carregar
        -   Suporte para deslocamentos programáveis

    -   Streaming

        -   Coloca de textura para limitar o pré-carregamento de WDDM

    -   os limites de textura de 16K
    -   Exigir 8 bits de subtexel e precisão submip na filtragem de textura
    -   Novos formatos de compactação de textura (1 novo formato LDR e um novo formato HDR)

-   O Direct3D 11 dá suporte a oDepth conservador – esse algoritmo permite que um sombreador de pixel Compare o valor de profundidade por pixel do sombreador de pixel com aquele no rasterizador. O resultado permite operações de remoção de profundidade antecipada enquanto mantém a capacidade de gerar oDepth de um sombreador de pixel.
-   O Direct3D 11 dá suporte à memória grande

    -   Permitir recursos > 4GB
    -   Manter índices de recursos 32 bits, mas o recurso é maior

-   O Direct3D 11 dá suporte a melhorias de saída de fluxo

    -   Saída de fluxo endereçável
    -   Aumentar a contagem de saída de fluxo para 4
    -   Alterar todos os buffers de saída de fluxo para que sejam de vários elementos

-   O Direct3D 11 dá suporte ao modelo de sombreador 5 (consulte o [modelo de sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Duplo com as normas
    -   Instrução set de bits de contagem
    -   Instrução localizar primeiro conjunto de bits
    -   Manipulação de transporte/estouro
    -   Instruções de estorno de bits para FFTs
    -   Troca condicional intrínseca
    -   ResInfo em buffers
    -   Recíproca de precisão reduzida
    -   Instruções de conversão de sombreador – FP16 para FP32 e vice-versa
    -   Buffer estruturado, que é um novo tipo de buffer que contém elementos estruturados.

-   O Direct3D 11 dá suporte a exibições de profundidade ou de estêncil somente leitura

    -   Desabilita as gravações na parte que é somente leitura, permite o uso de textura como entrada e a remoção de profundidade

-   O Direct3D 11 dá suporte ao Draw indireto – o Direct3D 10 implementa DrawAuto, que usa o conteúdo (gerado pela GPU) e o renderiza (na GPU). O Direct3D 11 generaliza o DrawAuto para que ele possa ser chamado por um sombreador de computação usando DrawInstanced e DrawIndexedInstanced.
-   O Direct3D 11 dá suporte a recursos diversos

    -   Visores de ponto flutuante
    -   Fixação MSS mipmap por recurso
    -   Tendência de profundidade – esse algoritmo atualiza o comportamento da tendência de profundidade, usando o estado do rasterizador. O resultado elimina os cenários em que a tendência calculada poderia ser NaN.
    -   Limites de recursos-os índices de recursos ainda precisam ser <= 32 bits, mas os recursos podem ser maiores que 4 GB.
    -   Precisão do rasterizador
    -   Requisitos de MSAA
    -   Contadores reduzidos
    -   Formato de 1 bit e filtro de texto removidos

## <a name="features-added-in-previous-releases"></a>Recursos adicionados em versões anteriores

Para obter a lista dos recursos adicionados em versões anteriores, consulte os seguintes tópicos:

-   [O que há de novo no SDK de agosto de 2009 do Windows 7/Direct3D 11](dx11-whats-new.md)
-   [O que há de novo na visualização técnica do Direct3D 11 de novembro de 2008](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 