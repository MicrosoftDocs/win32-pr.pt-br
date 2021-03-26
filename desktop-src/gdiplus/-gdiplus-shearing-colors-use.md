---
description: A distorção aumenta ou diminui um componente de cor em uma quantidade proporcional a outro componente de cor.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Distorcendo cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091462"
---
# <a name="shearing-colors"></a>Distorcendo cores

A distorção aumenta ou diminui um componente de cor em uma quantidade proporcional a outro componente de cor. Por exemplo, considere a transformação em que o componente vermelho é aumentado pela metade do valor do componente azul. Nessa transformação, a cor (0,2, 0,5, 1) seria (0,7, 0,5, 1). O novo componente vermelho é 0,2 + (1/2)(1) = 0,7.

O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo ColorBars4.bmp. Em seguida, o código se aplica à transformação de distorção descrita no parágrafo anterior para cada pixel da imagem.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



A ilustração a seguir mostra a imagem original à esquerda e a imagem distorcida à direita.

![ilustração mostrando quatro barras coloridas e, em seguida, as mesmas barras com cores diferentes](images/colortrans6.png)

A tabela a seguir mostra os vetores de cor para as quatro barras antes e depois da transformação distorção.



| Original           | Distorcido            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



