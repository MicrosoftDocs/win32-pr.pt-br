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
# <a name="cropping-and-scaling-gdi-images"></a><span data-ttu-id="a5327-103">Cortando e dimensionando imagens de GDI+</span><span class="sxs-lookup"><span data-stu-id="a5327-103">Cropping and scaling GDI+ images</span></span>

<span data-ttu-id="a5327-104">A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece vários métodos **DrawImage** , alguns dos quais têm parâmetros de retângulo de origem e de destino que você pode usar para cortar e dimensionar imagens.</span><span class="sxs-lookup"><span data-stu-id="a5327-104">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several **DrawImage** methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>

<span data-ttu-id="a5327-105">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Apple.gif.</span><span class="sxs-lookup"><span data-stu-id="a5327-105">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Apple.gif.</span></span> <span data-ttu-id="a5327-106">O código desenha a imagem inteira de maçã em seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="a5327-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="a5327-107">Em seguida, o código chama o método **DrawImage** de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma parte da imagem da Apple em um retângulo de destino maior do que a imagem original da Apple.</span><span class="sxs-lookup"><span data-stu-id="a5327-107">The code then calls the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>

<span data-ttu-id="a5327-108">O método **DrawImage** determina qual parte da Apple deve ser desenhada examinando o retângulo de origem, que é especificado pelo terceiro, quarto, quinto e sexto argumentos.</span><span class="sxs-lookup"><span data-stu-id="a5327-108">The **DrawImage** method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="a5327-109">Nesse caso, a maçã é cortada para 75% de sua largura e 75 por cento de sua altura.</span><span class="sxs-lookup"><span data-stu-id="a5327-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>

<span data-ttu-id="a5327-110">O método **DrawImage** determina onde desenhar a Apple cortada e o tamanho da Apple, observando o retângulo de destino, que é especificado pelo segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="a5327-110">The **DrawImage** method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="a5327-111">Nesse caso, o retângulo de destino é 30% a mais largo e 30 por cento mais alto que a imagem original.</span><span class="sxs-lookup"><span data-stu-id="a5327-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>


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



<span data-ttu-id="a5327-112">A ilustração a seguir mostra a maçã original e a maçã dimensionada e cortada.</span><span class="sxs-lookup"><span data-stu-id="a5327-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>

![ilustração mostrando uma Apple e uma parte ampliada da Apple original](images/cropscale1.png)

 

 



