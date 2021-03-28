---
description: Em vez de desenhar uma linha ou curva com uma cor sólida, você pode desenhar com uma textura.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Desenhando uma linha preenchida com uma textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967775"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="06b87-103">Desenhando uma linha preenchida com uma textura</span><span class="sxs-lookup"><span data-stu-id="06b87-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="06b87-104">Em vez de desenhar uma linha ou curva com uma cor sólida, você pode desenhar com uma textura.</span><span class="sxs-lookup"><span data-stu-id="06b87-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="06b87-105">Para desenhar linhas e curvas com uma textura, crie um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e passe o endereço desse objeto **TextureBrush** para um construtor de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="06b87-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="06b87-106">A imagem associada ao pincel de textura é usada para dividir o plano (invisivelmente) e, quando a caneta desenha uma linha ou curva, o traço da caneta descobre determinados pixels da textura do lado lateral.</span><span class="sxs-lookup"><span data-stu-id="06b87-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="06b87-107">O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo Texture1.jpg.</span><span class="sxs-lookup"><span data-stu-id="06b87-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="06b87-108">Essa imagem é usada para construir um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e o objeto **TextureBrush** é usado para construir um objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="06b87-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="06b87-109">A chamada para [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) desenha a imagem com seu canto superior esquerdo em (0, 0).</span><span class="sxs-lookup"><span data-stu-id="06b87-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="06b87-110">A chamada para [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa o objeto **Pen** para desenhar uma elipse texturizada.</span><span class="sxs-lookup"><span data-stu-id="06b87-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="06b87-111">A ilustração a seguir mostra a imagem e a elipse texturizada.</span><span class="sxs-lookup"><span data-stu-id="06b87-111">The following illustration shows the image and the textured ellipse.</span></span>

![ilustração mostrando uma pequena imagem retangular, um segmento de linha elíptico preenchido com a imagem original](images/pens7.png)

 

 
