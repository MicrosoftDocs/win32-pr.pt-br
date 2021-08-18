---
description: Em vez de desenhar uma linha ou curva com uma cor sólida, você pode desenhar com uma textura.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Desenhando uma linha preenchida com uma textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467026"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Desenhando uma linha preenchida com uma textura

Em vez de desenhar uma linha ou curva com uma cor sólida, você pode desenhar com uma textura. Para desenhar linhas e curvas com uma textura, crie um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e passe o endereço desse objeto **TextureBrush** para um construtor de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . A imagem associada ao pincel de textura é usada para dividir o plano (invisivelmente) e, quando a caneta desenha uma linha ou curva, o traço da caneta descobre determinados pixels da textura do lado lateral.

O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo Texture1.jpg. Essa imagem é usada para construir um objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e o objeto **TextureBrush** é usado para construir um objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . A chamada para [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) desenha a imagem com seu canto superior esquerdo em (0, 0). A chamada para [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa o objeto **Pen** para desenhar uma elipse texturizada.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



A ilustração a seguir mostra a imagem e a elipse texturizada.

![ilustração mostrando uma pequena imagem retangular, um segmento de linha elíptico preenchido com a imagem original](images/pens7.png)

 

 
