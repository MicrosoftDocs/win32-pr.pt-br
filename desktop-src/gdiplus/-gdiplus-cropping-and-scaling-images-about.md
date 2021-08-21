---
title: Sobre o corte e dimensionamento de imagens de GDI+
description: Você pode usar o método DrawImage da classe Graphics para desenhar e posicionar imagens.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e69adb7f817c36b955ed313290cf0b762c279b4296e06ad52aa6175ff2c467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036834"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Sobre o corte e dimensionamento de imagens de GDI+

Você pode usar o método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar e posicionar imagens. O DrawImage é um método sobrecarregado, portanto, há várias maneiras pelas quais você pode fornecê-lo com argumentos. Uma variação do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) recebe o endereço de um objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e uma referência a um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) . O retângulo especifica o destino para a operação de desenho; ou seja, ele especifica o retângulo no qual a imagem será desenhada. Se o tamanho do retângulo de destino for diferente do tamanho da imagem original, a escala dela será ajustada para caber no retângulo de destino. O exemplo a seguir desenha a mesma imagem três vezes: uma vez sem dimensionamento, uma vez com uma expansão e uma vez com uma compactação.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



O código anterior, junto com um arquivo específico, Spiral.png, produziu a saída a seguir.

![ilustração mostrando três versões de uma imagem: normal, ampliada e reduzida para metade do tamanho original](images/aboutgdip03-art06.png)

Algumas variações do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) têm um parâmetro de retângulo de origem, bem como um parâmetro de retângulo de destino. O retângulo de origem especifica a parte da imagem original que será desenhada. O retângulo de destino especifica onde a parte da imagem será desenhada. Se o tamanho do retângulo de destino for diferente do tamanho do retângulo de origem, a imagem será dimensionada para se ajustar ao retângulo de destino.

O exemplo a seguir constrói um objeto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) a partir do arquivo Runner.jpg. Toda a imagem é desenhada sem nenhuma escala em (0, 0). Em seguida, uma pequena parte da imagem é desenhada duas vezes: uma expandida e outra compactada.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



A ilustração a seguir mostra a imagem sem escala e as partes da imagem compactada e expandida.

![captura de tela mostrando uma imagem, uma parte da imagem compactada e, em seguida, a mesma parte expandida](images/aboutgdip03-art07.png)

 

 



