---
description: Uma conversão adiciona um valor a um ou mais dos componentes de quatro cores. As entradas de matriz de cores que representam as conversões são fornecidas na tabela a seguir.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Traduzindo cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608a0653423d854e6d77bd624949f24ec03cce6c4ed063d4c740dd142b1dfb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036334"
---
# <a name="translating-colors"></a>Traduzindo cores

Uma conversão adiciona um valor a um ou mais dos componentes de quatro cores. As entradas de matriz de cores que representam as conversões são fornecidas na tabela a seguir.



| Componente a ser convertido | Entrada da matriz |
|----------------------------|--------------|
| Vermelho                        | \[4 \] \[ 0\]   |
| Verde                      | \[4 \] \[ 1\]   |
| Azul                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

O exemplo a seguir constrói [**um objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo ColorBars.bmp. Em seguida, o código adiciona 0,75 ao componente vermelho de cada pixel na imagem. A imagem original é desenhada ao lado da imagem transformada.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



A ilustração a seguir mostra a imagem original à esquerda e a imagem transformada à direita.

![ilustração mostrando quatro barras coloridas e, em seguida, as mesmas barras com cores diferentes](images/colortrans2.png)

A tabela a seguir lista os vetores de cores para as quatro barras antes e depois da conversão em vermelho. Observe que, como o valor máximo para um componente de cor é 1, o componente vermelho na segunda linha não será alterado. (Da mesma forma, o valor mínimo para um componente de cor é 0).



| Original           | Traduzido      |
|--------------------|-----------------|
| Preto (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Vermelho (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Verde (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Azul (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



