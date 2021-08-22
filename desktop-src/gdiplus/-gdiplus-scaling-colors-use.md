---
description: Uma transformação de dimensionamento multiplica um ou mais dos quatro componentes de cor por um número. As entradas de matriz de cores que representam o dimensionamento são dadas na tabela a seguir.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Escalando cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7877db07ff1a11dcb985f8b0ca8ec3cc017f25fe45f00e989c9108891f8ff1ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036364"
---
# <a name="scaling-colors"></a>Escalando cores

Uma transformação de dimensionamento multiplica um ou mais dos quatro componentes de cor por um número. As entradas de matriz de cores que representam o dimensionamento são dadas na tabela a seguir.



| Componentes que serão escalados | Entrada da matriz |
|------------------------|--------------|
| Vermelho                    | \[0 \] \[ 0\]   |
| Verde                  | \[1 \] \[ 1\]   |
| Azul                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

O exemplo a seguir constrói [**um objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo ColorBars2.bmp. Depois o código escala o componente azul de cada pixel na imagem por um fator de 2. A imagem original é desenhada ao lado da imagem transformada.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



A ilustração a seguir mostra a imagem original à esquerda e a imagem em escala à direita.

![Mostra quatro barras coloridas e, em seguida, as mesmas barras com cores diferentes.](images/colortrans3.png)

A tabela a seguir mostra os vetores de cores para as quatro barras antes e depois do dimensionamento azul. Veja que o componente azul na quarta barra de cores foi de 0,8 para 0,6. Isso porque GDI+ retém apenas a parte fracionada do resultado. Por exemplo, (2)(0,8) = 1,6, e a parte fracionária de 1,6 é 0,6. Reter apenas a parte fracionada garante que o resultado sempre está no intervalo \[ 0, 1 \] .



| Original           | Em escala             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

O exemplo a seguir constrói [**um objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo ColorBars2.bmp. Depois, o código escala os componentes vermelho, verde e azul de cada pixel na imagem. Os componentes vermelhos são reduzidos em 25 por cento, os componentes verdes são reduzidos em 35 por cento e os componentes azuis são reduzidos em 50 por cento.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



A ilustração a seguir mostra a imagem original à esquerda e a imagem em escala à direita.

![ilustração mostrando quatro barras coloridas e, em seguida, as barras com cores diferentes](images/colortrans4.png)

A tabela a seguir mostra os vetores de cores para as quatro barras antes e depois do dimensionamento vermelho, verde e azul.



| Original           | Em escala               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



