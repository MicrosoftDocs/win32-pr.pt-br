---
description: Você pode usar a classe Image para carregar e exibir imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Desenhar, posicionar e clonar imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37e53ce3937d4f10b91a92e64feec57c6b39e718e7b551e4e4130569d4dd90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015146"
---
# <a name="drawing-positioning-and-cloning-images"></a>Desenhar, posicionar e clonar imagens

Você pode usar a classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) para carregar e exibir imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos). Para exibir uma imagem, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de **imagem** . O objeto **Graphics** fornece o método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , que recebe o endereço do objeto **Image** como um argumento.

O exemplo a seguir constrói um objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Climber.jpg e, em seguida, exibe a imagem. O ponto de destino do canto superior esquerdo da imagem, (10, 10), é especificado no segundo e terceiro parâmetros do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



O código anterior, junto com um arquivo específico, Climber.jpg, produziu a saída a seguir.

![captura de tela de uma janela que contém uma foto](images/aboutgdip03-art04.png)

Você pode construir objetos de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) de uma variedade de formatos de arquivos gráficos: BMP, GIF, JPEG, EXIF, png, TIFF, WMF, EMF e Icon.

O exemplo a seguir constrói objetos de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) de uma variedade de tipos de arquivo e, em seguida, exibe as imagens.


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



A [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fornece um [**método Image:: clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que você pode usar para fazer uma cópia de uma **imagem**, um [**metarquivo**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)ou um objeto de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existente. O método [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) é sobrecarregado na classe **bitmap** e uma das variações tem um parâmetro de retângulo de origem que você pode usar para especificar a parte da imagem original que você deseja copiar. O exemplo a seguir cria um objeto de **bitmap** clonando a metade superior de um objeto de **bitmap** existente. Então, ambas as imagens são exibidas.


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



O código anterior, junto com um arquivo específico, Spiral.png, produziu a saída a seguir.

![ilustração de uma imagem, seguida pela metade superior da imagem original](images/aboutgdip03-art05.png)

 

 
