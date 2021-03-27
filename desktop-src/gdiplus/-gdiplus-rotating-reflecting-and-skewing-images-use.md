---
description: Você pode girar, refletir e distorcer uma imagem especificando pontos de destino para os cantos superior esquerdo, superior direito e inferior esquerdo da imagem original.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Girando, refletindo e distorcendo imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921427"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Girando, refletindo e distorcendo imagens

Você pode girar, refletir e distorcer uma imagem especificando pontos de destino para os cantos superior esquerdo, superior direito e inferior esquerdo da imagem original. Os três pontos de destino determinam uma transformação afim que mapeia a imagem retangular original para um paralelogramo. (O canto inferior direito da imagem original é mapeado para o quarto canto do paralelogramo, que é calculado a partir dos três pontos de destino especificados.)

Por exemplo, suponha que a imagem original é um retângulo com o canto superior esquerdo em (0, 0), o canto superior direito em (100, 0) e o canto inferior esquerdo em (0, 50). Agora suponha que mapeiemos esses três pontos para os pontos de destino da seguinte maneira.



| Ponto original       | Ponto de destino |
|----------------------|-------------------|
| Superior esquerdo (0, 0)    | (200, 20)         |
| Superior direito (100, 0) | (110, 100)        |
| Inferior esquerdo (0, 50)   | (250, 30)         |



 

A ilustração a seguir mostra a imagem original e a imagem mapeada para o paralelogramo. A imagem original foi distorcida, refletida, girada e movida. O eixo x ao longo da borda superior da imagem original é mapeado para a linha que percorre (200, 20) e (110, 100). O eixo y ao longo da borda esquerda da imagem original é mapeado para a linha que percorre (200, 20) e (250, 30).

![ilustração mostrando faixas coloridas na origem dos eixos de coordenadas e nas mesmas faixas inclinadas e em um local, rotação e tamanho diferentes](images/stripes1.png)

O exemplo a seguir produz as imagens mostradas na ilustração anterior.


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



A ilustração a seguir mostra uma transformação semelhante aplicada a uma imagem fotográfica.

![ilustração mostrando a mesma foto duas vezes; o segundo é invertido, inclinado, e tem tamanho, rotação e local diferentes](images/transformedclimber.png)

A ilustração a seguir mostra uma transformação semelhante aplicada a um metarquivo.

![ilustração mostrando formas e texto, em seguida, novamente, mas invertido, inclinado e com localização, rotação e tamanho diferentes](images/transformedmetafile.png)

 

 



