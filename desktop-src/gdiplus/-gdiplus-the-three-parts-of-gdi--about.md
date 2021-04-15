---
description: 'Os serviços do Windows GDI+ se enquadram nas três categorias amplas a seguir:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: As três partes do GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988858"
---
# <a name="the-three-parts-of-gdi"></a>As três partes do GDI+

Os serviços do Windows GDI+ se enquadram nas três categorias amplas a seguir:

-   [gráficos vetoriais 2D](#2-d-vector-graphics)
-   [Geração de imagens](#imaging)
-   [Tipografia](#typography)

## <a name="2-d-vector-graphics"></a>gráfico vetorial 2D

Os gráficos vetoriais envolvem primitivas de desenho (como linhas, curvas e figuras) que são especificadas por conjuntos de pontos em um sistema de coordenadas. Por exemplo, uma linha reta pode ser especificada por seus dois pontos de extremidade, e um retângulo pode ser especificado por um ponto dando o local de seu canto superior esquerdo e um par de números que dão sua largura e altura. Um caminho simples pode ser especificado por uma matriz de pontos a ser conectada por linhas retas. Uma spline de Bézier é uma curva sofisticada especificada por quatro pontos de controle.

O GDI+ fornece classes que armazenam informações sobre os próprios primitivos, classes que armazenam informações sobre como os primitivos devem ser desenhados e classes que realmente fazem o desenho. Por exemplo, a classe **Rect** armazena o local e o tamanho de um retângulo; a classe Pen armazena informações sobre a cor da linha, a largura da linha e o estilo **da** linha; e a classe **Graphics** tem métodos para desenhar linhas, retângulos, caminhos e outras figuras. Há também várias classes de **pincel** que armazenam informações sobre como figuras e caminhos fechados devem ser preenchidos com cores ou padrões.

## <a name="imaging"></a>Geração de imagens

Determinados tipos de imagens são difíceis ou impossíveis de exibir com as técnicas de gráficos vetoriais. Por exemplo, as imagens nos botões da barra de ferramentas e as imagens que aparecem como ícones seriam difíceis de especificar como coleções de linhas e curvas. Uma fotografia digital de alta resolução de um estádio de beisebol lotado seria ainda mais difícil de criar com técnicas vetoriais. As imagens desse tipo são armazenadas como bitmaps, matrizes de números que representam as cores de pontos individuais na tela. As estruturas de dados que armazenam informações sobre bitmaps tendem a ser mais complexas do que aquelas necessárias para gráficos vetoriais, portanto, há várias classes em GDI+ dedicadas a essa finalidade. Um exemplo de tal classe é **CachedBitmap**, que é usado para armazenar um bitmap na memória para acesso rápido e exibição.

## <a name="typography"></a>Tipografia

A tipografia se preocupa com a exibição de texto em uma variedade de fontes, tamanhos e estilos. O GDI+ fornece uma grande quantidade de suporte para essa tarefa complexa. Um dos novos recursos do GDI+ é a suavização de subpixel, o que dá ao texto renderizado em uma tela de LCD uma aparência mais suave.

 

 



