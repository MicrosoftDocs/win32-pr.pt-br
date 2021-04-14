---
description: As texturas são sempre endereçadas linearmente de (0,0, 0,0) no canto superior esquerdo para (1,0, 1,0) no canto inferior direito, conforme mostrado na ilustração a seguir.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtragem de textura bilinear (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370484"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Filtragem de textura bilinear (Direct3D 9)

As texturas são sempre endereçadas linearmente de (0,0, 0,0) no canto superior esquerdo para (1,0, 1,0) no canto inferior direito, conforme mostrado na ilustração a seguir.

![ilustração de textura 4 x 4 com blocos sólidas de cor](images/bilinear-fig7a.png)

As texturas geralmente são representadas como se fossem compostas de blocos sólidos de cor, mas é mais correto pensar nas texturas da mesma maneira que você pensaria na exibição de rasterização: cada texel é definido no centro exato de uma célula de grade, conforme mostrado na ilustração a seguir.

![ilustração de textura 4 x 4 com texels definidos no centro das células de grade](images/bilinear-fig7b.png)

Se você solicitar a amostra de textura para a cor dessa textura nas coordenadas UV (0,375, 0,375), você receberá vermelho sólido (255, 0, 0). Isso faz sentido perfeito porque o centro exato da célula vermelha Texel está na UV (0,375, 0,375). E se você pedir a amostra de cor da textura UV (0,25, 0,25)? Isso não é tão fácil, porque o ponto na UV (0,25, 0,25) está no canto exato de 4 texels.

O esquema mais simples é simplesmente fazer com que a amostra retorne a cor do Texel mais próximo; Isso é chamado de filtragem de ponto (consulte a [amostragem de ponto mais próximo (Direct3D 9)](nearest-point-sampling.md)) e geralmente é indesejável devido a resultados granulares ou de blocos. A amostragem de pontos de nossa textura em UV (0,25, 0,25) mostra outro problema sutil com filtragem por ponto mais próximo: há quatro texels equidistantes do ponto de amostra, por isso não há um único texel mais próximo. Um desses quatro texels será escolhido como a cor retornada, mas a seleção depende de como a coordenada é arredondada, o que pode introduzir artefatos que causam danos (consulte o artigo sobre amostragem por ponto mais próximo no SDK).

Um esquema de filtragem um pouco mais preciso e mais comum é calcular a média ponderada do 4 texels mais próximo ao ponto de amostragem; Isso é chamado de filtragem bilinear, e o custo computacional extra geralmente é insignificante porque essa rotina é implementada em hardware de gráficos moderno. Veja as cores que obtemos em alguns pontos de amostragem diferentes usando a filtragem bilinear:


```
UV: (0.5, 0.5)
```



Esse ponto fica localizado na borda exata entre os texels vermelhos, verdes, azuis e brancos. A cor retornada pela amostragem é cinza:


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



Esse ponto fica localizado no ponto intermediário da borda entre os texels vermelhos e verdes. A cor retornada pela amostragem é amarelo-cinza (observe que as contribuições de texels azuis e brancos são dimensionadas como 0):


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



Esse é o endereço do texel vermelho, que é a cor retornada (todos os outros texels do cálculo de filtragem são ponderados para 0):


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Compare esses cálculos com a ilustração a seguir, que mostra o que acontece se o cálculo de filtragem bilinear for executado em cada endereço de textura na textura de 4 x 4.

![Ilustração de textura 4 x 4 com filtragem bilinear realizada em todos os endereços de textura](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 



