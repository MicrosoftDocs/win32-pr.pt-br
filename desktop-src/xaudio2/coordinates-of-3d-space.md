---
description: 'A posição, a velocidade e a orientação das fontes de som e dos ouvintes no espaço 3D são representadas por coordenadas cartesianas, que são valores em três eixos: o eixo x, o eixo y e o eixo z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordenadas do espaço 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170281"
---
# <a name="coordinates-of-3d-space"></a>Coordenadas do espaço 3D

A posição, a velocidade e a orientação das fontes de som e dos ouvintes no espaço 3D são representadas por coordenadas cartesianas, que são valores em três eixos: o eixo x, o eixo y e o eixo z.

Os eixos são relativos a um ponto de vista estabelecido pelo aplicativo. Os valores no eixo x aumentam da esquerda para a direita, no eixo y de baixo para cima e no eixo z de perto de longe.

A estrutura de **\_ vetor X3DAUDIO** contém valores que descrevem a posição, a velocidade ou a orientação nos três eixos.

De forma convencional, os vetores são expressos como três valores entre parênteses e separados por vírgulas, na ordem (x, y, z).

Para posição, os valores estão em unidades mundiais definidas pelo usuário.

Para a velocidade, o vetor descreve a taxa de movimentação ao longo de cada eixo em unidades mundiais por segundo.

Para orientação, os valores estão em unidades arbitrárias e são relativos uns aos outros. Por exemplo, se a exibição de base do mundo 3D estiver voltada para o norte em direção ao horizonte, e a orientação do ouvinte for (-1, 0, 1), o ouvinte voltará para o noroeste. Como os valores dentro de um vetor não estão em unidades absolutas, o vetor igualmente poderia ser expresso como (-5, 0, 5) ou (-0,25, 0, 0,25).

os vetores 3D funcionam de maneira muito semelhante a vetores 2D, mas com um eixo adicional na direção de cima para baixo. Você pode ver como os vetores funcionam em espaço 2D desenhando-os em uma folha de papel gráfico. Deixe os valores aumentarem de baixo para a parte superior do papel e da esquerda para a direita. Uma linha desenhada de (0, 0) para (1, 1) tem a mesma orientação, ou direção, como uma desenhada de (0, 0) para (5, 5). No entanto, a segunda linha indica uma maior distância ou velocidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos comuns de áudio](common-audio-concepts.md)
</dt> <dt>

[Visão geral do X3DAudio](x3daudio-overview.md)
</dt> </dl>

 

 



