---
description: Remapeamento é o processo de conversão de cores em uma imagem seguindo uma tabela de remapeamento de cores. A tabela de remapa de cores é uma matriz de estruturas ColorMap. Cada estrutura ColorMap na matriz tem um membro oldColor e um membro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso de uma tabela de remapeamento de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036294"
---
# <a name="using-a-color-remap-table"></a>Uso de uma tabela de remapeamento de cores

Remapeamento é o processo de conversão de cores em uma imagem seguindo uma tabela de remapeamento de cores. A tabela de remapa de cores é uma matriz de [**estruturas ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Cada **estrutura ColorMap** na matriz tem um **membro oldColor** e um **membro newColor.**

Quando GDI+ desenha uma imagem, cada pixel da imagem é comparado com a matriz de cores antigas. Se a cor do pixel corresponde a uma cor anterior, sua cor é alterada para a nova cor correspondente. As cores são alteradas apenas para renderização – os valores de cor da imagem em si (armazenados em uma [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ou objeto [**Bitmap)**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) não são alterados.

Para desenhar uma imagem remapped, inicialize uma matriz de [**estruturas ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Passe o endereço dessa matriz para o método [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) de um objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e, em seguida, passe o endereço do objeto **ImageAttributes** para o [método DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de [**um objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

O exemplo a seguir cria [**um objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo RemapInput.bmp. O código cria uma tabela de remapa de cores que consiste em uma única [**estrutura ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) O **membro oldColor** da estrutura **ColorMap** é vermelho e o **membro newColor** é azul. A imagem é desenhada uma vez sem remapeamento e uma vez com remapeamento. O processo de remapeamento transforma todos os pixels vermelhos em azul.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

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



A ilustração a seguir mostra a imagem original à esquerda e a imagem remapeada à direita.

![ilustração mostrando duas versões de uma imagem multicolorida; a região vermelha na primeira versão é azul na segunda versão](images/colortrans7.png)

 

 



