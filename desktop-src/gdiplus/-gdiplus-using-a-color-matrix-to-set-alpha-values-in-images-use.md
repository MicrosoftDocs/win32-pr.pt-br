---
description: A classe de bitmap (que herda da classe Image) e a classe ImageAttributes fornecem funcionalidade para obter e definir valores de pixel.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Uso de uma matriz de cores para definir valores alfa em imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501658"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Uso de uma matriz de cores para definir valores alfa em imagens

A classe de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (que herda da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) e a classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) fornecem funcionalidade para obter e definir valores de pixel. Você pode usar a classe **ImageAttributes** para modificar os valores Alfa de uma imagem inteira ou pode chamar o método [**bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) da classe **bitmap** para modificar valores de pixel individuais. Para obter mais informações sobre como definir valores de pixel individuais, consulte [definindo os valores Alfa de pixels individuais](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).

O exemplo a seguir desenha uma linha preta larga e, em seguida, exibe uma imagem opaca que cobre parte dessa linha.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



A ilustração a seguir mostra a imagem resultante, que é desenhada em (30, 0). Observe que a linha preta larga não é mostrada por meio da imagem.

![ilustração mostrando uma imagem opaca sobrepondo um retângulo preto fino e largo](images/image1.png)

A classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) tem muitas propriedades que você pode usar para modificar imagens durante a renderização. No exemplo a seguir, um objeto **ImageAttributes** é usado para definir todos os valores alfa como 80% do que eles eram. Isso é feito inicializando uma matriz de cores e configurando o valor de escala alfa na matriz para 0,8. O endereço da matriz de cores é passado para o método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) do objeto **ImageAttributes** , e o endereço do objeto **ImageAttributes** é passado para o método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



Durante o processamento, os valores alfa no bitmap são convertidos em 80 por cento do que eram. Isso resulta em uma imagem que é combinada com a tela de fundo. Como mostra a ilustração a seguir, a imagem de bitmap é transparente; é possível ver a linha preta sólida através dela.

![ilustração semelhante à anterior, mas a imagem é sem transparência](images/image2.png)

Nos pontos em que a imagem está sobre a parte branca da tela de fundo, ela é combinada com a cor branca. Nos pontos em que imagem cruza a linha preta, ela é combinada a cor preta.

 

 



