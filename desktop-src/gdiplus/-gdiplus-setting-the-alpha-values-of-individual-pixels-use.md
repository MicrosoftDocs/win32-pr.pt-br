---
description: O tópico Usando uma matriz de cores para definir valores alfa em imagens mostra um método não estruturativo para alterar os valores alfa de uma imagem.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Definindo os valores alfa de pixels individuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c88c7ef8cc343b99f7a50c3fad012b62ef2a8d79ab38de6988efb6b5643e0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830726"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Definindo os valores alfa de pixels individuais

O tópico [Usando uma matriz de cores para definir](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) valores alfa em imagens mostra um método não estruturativo para alterar os valores alfa de uma imagem. O exemplo nesse tópico renderiza uma imagem semitransparentemente, mas os dados de pixel no bitmap não são alterados. Os valores alfa são alterados somente durante a renderização.

O exemplo a seguir mostra como alterar os valores alfa de pixels individuais. O código no exemplo realmente altera as informações alfa em um [**objeto Bitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) A abordagem é muito mais lenta do que usar uma matriz de cores e um [**objeto ImageAttributes,**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) mas fornece controle sobre os pixels individuais no bitmap.


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



A ilustração a seguir mostra a imagem resultante.

![ilustração mostrando uma imagem que obtém mais opaca da esquerda para a direita, sobre um retângulo preto](images/image3.png)

O exemplo de código anterior usa loops aninhados para alterar o valor alfa de cada pixel no bitmap. Para cada pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtém a cor existente, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) cria uma cor temporária que contém o novo valor alfa e, em seguida, [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) define a nova cor. O valor alfa é definido com base na coluna do bitmap. Na primeira coluna, alfa é definido como 0. Na última coluna, alfa é definido como 255. Portanto, a imagem resultante vai de totalmente transparente (na borda esquerda) para totalmente opaco (na borda direita).

[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) e [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) dão a você controle dos valores de pixel individuais. No entanto, usar **Bitmap::GetPixel** e **Bitmap::SetPixel** não é tão rápido quanto usar a classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e a estrutura [**ColorMatrix.**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)

 

 



