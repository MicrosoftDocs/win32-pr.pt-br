---
title: Cortando e dimensionando imagens de GDI+
description: A classe Graphics fornece vários métodos DrawImage, alguns dos quais têm parâmetros de retângulo de origem e de destino que você pode usar para cortar e dimensionar imagens.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987957"
---
# <a name="cropping-and-scaling-gdi-images"></a>Cortando e dimensionando imagens de GDI+

A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece vários métodos **DrawImage** , alguns dos quais têm parâmetros de retângulo de origem e de destino que você pode usar para cortar e dimensionar imagens.

O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Apple.gif. O código desenha a imagem inteira de maçã em seu tamanho original. Em seguida, o código chama o método **DrawImage** de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma parte da imagem da Apple em um retângulo de destino maior do que a imagem original da Apple.

O método **DrawImage** determina qual parte da Apple deve ser desenhada examinando o retângulo de origem, que é especificado pelo terceiro, quarto, quinto e sexto argumentos. Nesse caso, a maçã é cortada para 75% de sua largura e 75 por cento de sua altura.

O método **DrawImage** determina onde desenhar a Apple cortada e o tamanho da Apple, observando o retângulo de destino, que é especificado pelo segundo argumento. Nesse caso, o retângulo de destino é 30% a mais largo e 30 por cento mais alto que a imagem original.


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



A ilustração a seguir mostra a maçã original e a maçã dimensionada e cortada.

![ilustração mostrando uma Apple e uma parte ampliada da Apple original](images/cropscale1.png)

 

 



