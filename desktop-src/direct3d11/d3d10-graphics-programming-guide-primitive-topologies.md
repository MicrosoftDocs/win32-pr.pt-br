---
title: Topologias primitivas
description: O Direct3D 10 e superior dá suporte a vários tipos primitivos (ou topologias) que são representados pelo \_ \_ tipo enumerado da topologia primitiva do D3D. Esses tipos definem como os vértices são interpretados e renderizados pelo pipeline.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294087"
---
# <a name="primitive-topologies"></a>Topologias primitivas

O Direct3D 10 e superior dá suporte a vários tipos primitivos (ou topologias) que são representados pelo tipo enumerado da [**\_ \_ topologia primitiva do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Esses tipos definem como os vértices são interpretados e renderizados pelo pipeline.

-   [Tipos primitivos básicos](#basic-primitive-types)
-   [Adjacência primitiva](#primitive-adjacency)
-   [Direção do enrolamento e posições de vértice à esquerda](#winding-direction-and-leading-vertex-positions)
-   [Gerando várias faixas](#generating-multiple-strips)
-   [Tópicos relacionados](#related-topics)

## <a name="basic-primitive-types"></a>Tipos primitivos básicos

Há suporte para os seguintes tipos primitivos básicos:

-   [Lista de pontos](/windows/desktop/direct3d9/point-lists)
-   [Lista de linhas](/windows/desktop/direct3d9/line-lists)
-   [Faixa de linha](/windows/desktop/direct3d9/line-strips)
-   [Lista de triângulos](/windows/desktop/direct3d9/triangle-lists)
-   [Faixa triange](/windows/desktop/direct3d9/triangle-strips)

Para uma visualização de cada tipo primitivo, consulte o diagrama mais adiante neste tópico em [direção de enrolamento e posições de vértice à esquerda](#winding-direction-and-leading-vertex-positions).

O estágio de montagem de entrada lê dados de um vértice e de buffers de índice, monta os dados nesses primitivos e, em seguida, envia os dados para os estágios de pipeline restantes. (Você pode usar o método [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) para especificar o tipo primitivo para o estágio de Assembler de entrada.)

## <a name="primitive-adjacency"></a>Adjacência primitiva

Todos os tipos primitivos de Direct3D 10 e superiores (exceto a lista de pontos) estão disponíveis em duas versões: um tipo primitivo com adjacência e um tipo primitivo sem adjacência. Primitivas com adjacência contêm alguns dos vértices ao redor, enquanto primitivas sem adjacência contêm apenas os vértices da primitiva de destino. Por exemplo, a lista de linhas primitiva (representada pelo valor de **\_ \_ \_ linha da topologia primitiva de D3D** ) tem um primitivo de lista de linhas correspondente que inclui uma adjacência (representada pelo valor de **\_ \_ \_ \_ adj da linha de line da topologia primitiva do D3D** .)

Primitivas adjacentes foram projetadas para fornecer mais informações sobre sua geometria e só ficam visíveis por meio de um sombreador de geometria. A adjacência é útil para sombreadores de geometria que usam a detecção de silhueta, extrusão de volume de sombra e assim por diante.

Por exemplo, suponha que você deseja desenhar uma lista de triângulos com adjacência. Uma lista de triângulos que contém 36 vértices (com adjacência) produzirá 6 primitivas concluídas. Primitivas com adjacência (exceto faixas de linha) contêm exatamente o dobro dos vértices que a primitiva equivalente sem adjacência, onde cada vértice adicional é um vértice adjacente.

## <a name="winding-direction-and-leading-vertex-positions"></a>Direção do enrolamento e posições de vértice à esquerda

Conforme mostrado na ilustração a seguir, um vértice principal é o primeiro vértice não adjacente em uma primitiva. Um tipo primitivo poderá ter vários vértices principais definidos, desde que cada um deles seja usado para uma primitiva diferente. Para uma faixa de triângulos com adjacência, os vértices principais são 0, 2, 4, 6 e assim por diante. Para uma faixa de linha com adjacência, os vértices principais são 1, 2, 3 e assim por diante. Uma primitiva adjacente, por outro lado, não tem nenhum vértice principal.

A ilustração a seguir mostra a ordem de vértices para todos os tipos primitivos que o assembler de entrada pode produzir.

![diagrama da ordem dos vértices para tipos primitivos](images/d3d10-primitive-topologies.png)

Os símbolos na ilustração anterior estão descritos na tabela a seguir.



| Símbolo                                                                                   | Name              | Descrição                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![símbolo de um vértice](images/d3d10-primitive-topologies-vertex.png)                     | Vértice            | Um ponto no espaço 3D.                                                                                                                                                                               |
| ![símbolo da direção de rotação](images/d3d10-primitive-topologies-winding-direction.png) | Direção de rotação | A ordem de vértice ao montar uma primitiva. Pode ser no sentido horário ou anti-horário; Especifique isso chamando [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1). |
| ![símbolo de vértice principal](images/d3d10-primitive-topologies-leading-vertex.png)       | Vértice principal    | O primeiro vértice não adjacente em uma primitiva que contém dados por constante.                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>Gerando várias faixas

Você pode gerar várias faixas por meio de corte de faixa. Você pode executar um corte de faixa explicitamente chamando a função HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip), ou inserindo um valor de índice especial para o buffer de índice. Esse valor é -1, que é 0xffffffff para índices de 32 bits ou 0xffff para índices de 16 bits. Um índice de – 1 indica um "corte" ou "reinício" explícito da faixa atual. O índice anterior conclui a primitiva anterior, ou a faixa, e o próximo índice inicia um novo primitivo ou faixa. Para obter mais informações sobre a geração de várias faixas, consulte o [estágio Geometry-Shader](/previous-versions//bb205146(v=vs.85)).

> [!Note]  
> Você precisa de [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 ou superior, pois nem todos os hardwares 10level9 implementam essa funcionalidade.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o estágio de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 