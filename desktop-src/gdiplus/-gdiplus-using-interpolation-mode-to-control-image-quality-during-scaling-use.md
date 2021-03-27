---
description: O modo de interpolação de um objeto gráfico influencia a maneira como o Windows GDI+ escala (amplia e reduz) imagens.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967395"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento

O modo de interpolação de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influencia a maneira como o Windows GDI+ escala (amplia e reduz) imagens. A enumeração [**interpolamode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) em Gdiplusenums. h define vários modos de interpolação, alguns dos quais são mostrados na lista a seguir:

-   InterpolationModeNearestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Para alongar uma imagem, cada pixel da imagem original deve ser mapeado para um grupo de pixels da imagem maior. Para encolher uma imagem, cada pixel da imagem original deve ser mapeado para pixels únicos da imagem menor. A eficácia dos algoritmos que executam esses mapeamentos determina a qualidade de uma imagem dimensionada. Algoritmos que produzem imagens dimensionadas de qualidade superior tendem a exigir mais tempo de processamento. Na lista anterior, InterpolationModeNearestNeighbor é o modo de qualidade mais baixa e InterpolationModeHighQualityBicubic é o modo de qualidade mais alta.

Para definir o modo de interpolação, passe um dos membros da enumeração de [**interpolação**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) para o método **setinterpolamode** de um objeto de [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

O exemplo a seguir desenha uma imagem e reduz a imagem com três modos de interpolação diferentes:


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



A ilustração a seguir mostra a imagem original e as três imagens menores.

![ilustração mostrando uma imagem original grande e as três imagens menores de qualidade variável](images/grapes1.png)

 

 



