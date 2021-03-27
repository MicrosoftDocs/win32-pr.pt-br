---
description: O tópico usando uma matriz de cores para definir valores Alfa em imagens mostra um método não destrutivo para alterar os valores Alfa de uma imagem.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Definindo os valores Alfa de pixels individuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501662"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Definindo os valores Alfa de pixels individuais

O tópico [usando uma matriz de cores para definir valores Alfa em imagens](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) mostra um método não destrutivo para alterar os valores Alfa de uma imagem. O exemplo nesse tópico renderiza uma imagem semitransparentemente, mas os dados de pixel no bitmap não são alterados. Os valores Alfa são alterados somente durante a renderização.

O exemplo a seguir mostra como alterar os valores Alfa de pixels individuais. O código no exemplo realmente altera as informações alfa em um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . A abordagem é muito mais lenta do que usar uma matriz de cores e um objeto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , mas lhe dá controle sobre os pixels individuais no bitmap.


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

![ilustração mostrando uma imagem que fica mais opaca da esquerda para a direita, em um retângulo preto](images/image3.png)

O exemplo de código anterior usa loops aninhados para alterar o valor alfa de cada pixel no bitmap. Para cada pixel, [**bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) Obtém a cor existente, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) cria uma cor temporária que contém o novo valor alfa e, em seguida, [**bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) define a nova cor. O valor alfa é definido com base na coluna do bitmap. Na primeira coluna, alfa é definido como 0. Na última coluna, alfa é definido como 255. Portanto, a imagem resultante vai de totalmente transparente (na borda esquerda) para totalmente opaca (na borda direita).

[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) e [**bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) lhe dão controle dos valores de pixel individuais. No entanto, o uso de **bitmap:: GetPixel** e **bitmap:: SetPixel** não é tão rápido quanto usar a classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e a estrutura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .

 

 



