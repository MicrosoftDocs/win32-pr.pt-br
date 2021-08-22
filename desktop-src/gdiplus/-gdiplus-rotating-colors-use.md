---
description: É difícil de visualizar a rotação em um espaço de cor quadridimensional.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Cores de rotação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036424"
---
# <a name="rotating-colors"></a>Cores de rotação

É difícil de visualizar a rotação em um espaço de cor quadridimensional. Podemos pode facilitar a visualização da rotação concordando em manter um dos componentes de cor fixos. Suponha que concordamos em manter o componente alfa fixo em 1 (completamente opaco). Em seguida, é possível visualizar um espaço de cores tridimensional com os eixos vermelho, verde e azul como mostrado na ilustração a seguir.

![ilustração de uma exibição em perspectiva de um espaço de cores tridimensional com eixos rotulados como vermelho, verde e azul](images/recoloring03.png)

Podemos pensar em uma cor como um ponto no espaço 3D. Por exemplo, o ponto (1, 0, 0) no espaço representa a cor vermelha e o ponto (0, 1, 0) no espaço representa a cor verde.

A ilustração a seguir mostra o que significa girar a cor (1, 0, 0) por meio de um ângulo de 60 graus no plano vermelho-verde. Podemos pensar no giro de um plano paralelo ao plano vermelho-verde como um giro sobre o eixo azul.

![ilustração que mostra o ponto (1, 0, 0) girado 60 graus para (0,5, 0,866, 0)](images/recoloring04.png)

A ilustração a seguir mostra como inicializar uma matriz de cores para executar giros de cada um dos três eixos de coordenadas (vermelho, verde e azul).

![ilustração mostrando matrizes de cores que executam rotações sobre cada um dos três eixos de coordenadas](images/recoloring05.png)

O exemplo a seguir usa uma imagem que aparece em uma cor (1, 0, 0,6) e aplica um giro de 60 graus sobre o eixo azul. O ângulo da rotação é removido em um plano que é paralelo ao plano de Red-Green.


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



A ilustração a seguir mostra a imagem original à esquerda e a imagem com giro de cor à direita.

![ilustração mostrando retângulos preenchidos com a imagem original (violeta vermelha) e imagem girada em cores (verde-marinho)](images/colortrans5.png)

A rotação de cores executada no exemplo de código anterior pode ser visualizada da seguinte maneira.

![ilustração mostrando um espaço de cores 3D e o ponto (1, 0, 0,6) girado 60 graus para (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



