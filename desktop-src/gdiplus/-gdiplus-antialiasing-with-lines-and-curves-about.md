---
description: ao usar Windows GDI+ para desenhar uma linha, você fornece o ponto inicial e o ponto final da linha, mas não precisa fornecer informações sobre os pixels individuais na linha.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Suavização com linhas e curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697105"
---
# <a name="antialiasing-with-lines-and-curves"></a>Suavização com linhas e curvas

ao usar Windows GDI+ para desenhar uma linha, você fornece o ponto inicial e o ponto final da linha, mas não precisa fornecer informações sobre os pixels individuais na linha. GDI+ trabalha em conjunto com o software de driver de vídeo para determinar quais pixels serão ativados para mostrar a linha em um dispositivo de vídeo específico.

Considere uma linha vermelha reta que vai do ponto (4, 2) até o ponto (16, 10). Suponha que o sistema de coordenadas tem sua origem no canto superior esquerdo e que a unidade de medida é o pixel. Suponha também que o eixo X aponta para a direita e o eixo Y aponta para baixo. A ilustração a seguir mostra uma exibição ampliada da linha vermelha desenhada em uma tela de fundo multicolorida.

![ilustração mostrando pixels vermelhos sólidos em um plano de fundo multicolorido](images/aboutgdip02-art33.png)

Observe que os pixels vermelhos usados para renderizar a linha são opacos. Não há pixels parcialmente transparentes envolvidos na exibição da linha. Esse tipo de renderização de linha dá à linha uma aparência irregular e a linha parece um pouco como uma escada. Essa técnica de representar uma linha com uma escada é chamada de serrilhado; a escada é um alias para a linha teórica.

Uma técnica mais sofisticada para renderizar uma linha envolve o uso de pixels parcialmente transparentes juntamente com pixels puros de vermelho. Os pixels são definidos como vermelho puro ou com alguma mistura de vermelho e a cor do plano de fundo, dependendo de quão perto eles estão para a linha. Esse tipo de renderização é chamado de suavização e resulta em uma linha que o olho humano percebe como mais suave. A ilustração a seguir mostra como determinados pixels são mesclados com a tela de fundo para produzir uma linha suavizada.

![ilustração mostrando pixels que são tons de vermelho no mesmo plano de fundo](images/aboutgdip02-art34.png)

A anti-aliasing (suavização) também pode ser aplicada a curvas. A ilustração a seguir mostra uma exibição ampliada de uma elipse suavizada.

![ilustração de uma elipse composta por diferentes tons de pixels azuis em um plano de fundo branco](images/aboutgdip02-art35.png)

A ilustração a seguir mostra a mesma elipse em seu tamanho real, uma vez sem suavização e outra com suavização.

![captura de tela de duas elipses: a que está com a suavização aparece mais suave](images/aboutgdip02-art36.png)

Para desenhar linhas e curvas que usam anti-aliasing, crie um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passe *SmoothingModeAntiAlias* para o método [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) . Em seguida, chame um dos métodos de desenho do mesmo objeto de **gráfico** .


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** é um elemento da enumeração [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .

 

 



