---
description: Você pode usar a classe Image para carregar e exibir imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Desenhar, posicionar e clonar imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165464"
---
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="75e23-103">Desenhar, posicionar e clonar imagens</span><span class="sxs-lookup"><span data-stu-id="75e23-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="75e23-104">Você pode usar a classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) para carregar e exibir imagens rasterizadas (bitmaps) e imagens de vetor (metaarquivos).</span><span class="sxs-lookup"><span data-stu-id="75e23-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="75e23-105">Para exibir uma imagem, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de **imagem** .</span><span class="sxs-lookup"><span data-stu-id="75e23-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="75e23-106">O objeto **Graphics** fornece o método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , que recebe o endereço do objeto **Image** como um argumento.</span><span class="sxs-lookup"><span data-stu-id="75e23-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="75e23-107">O exemplo a seguir constrói um objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo Climber.jpg e, em seguida, exibe a imagem.</span><span class="sxs-lookup"><span data-stu-id="75e23-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="75e23-108">O ponto de destino do canto superior esquerdo da imagem, (10, 10), é especificado no segundo e terceiro parâmetros do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="75e23-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="75e23-109">O código anterior, junto com um arquivo específico, Climber.jpg, produziu a saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="75e23-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![captura de tela de uma janela que contém uma foto](images/aboutgdip03-art04.png)

<span data-ttu-id="75e23-111">Você pode construir objetos de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) de uma variedade de formatos de arquivos gráficos: BMP, GIF, JPEG, EXIF, png, TIFF, WMF, EMF e Icon.</span><span class="sxs-lookup"><span data-stu-id="75e23-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="75e23-112">O exemplo a seguir constrói objetos de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) de uma variedade de tipos de arquivo e, em seguida, exibe as imagens.</span><span class="sxs-lookup"><span data-stu-id="75e23-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


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



<span data-ttu-id="75e23-113">A [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fornece um [**método Image:: clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que você pode usar para fazer uma cópia de uma **imagem**, um [**metarquivo**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)ou um objeto de [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existente.</span><span class="sxs-lookup"><span data-stu-id="75e23-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="75e23-114">O método [clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) é sobrecarregado na classe **bitmap** e uma das variações tem um parâmetro de retângulo de origem que você pode usar para especificar a parte da imagem original que você deseja copiar.</span><span class="sxs-lookup"><span data-stu-id="75e23-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="75e23-115">O exemplo a seguir cria um objeto de **bitmap** clonando a metade superior de um objeto de **bitmap** existente.</span><span class="sxs-lookup"><span data-stu-id="75e23-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="75e23-116">Então, ambas as imagens são exibidas.</span><span class="sxs-lookup"><span data-stu-id="75e23-116">Then both images are displayed.</span></span>


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



<span data-ttu-id="75e23-117">O código anterior, junto com um arquivo específico, Spiral.png, produziu a saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="75e23-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![ilustração de uma imagem, seguida pela metade superior da imagem original](images/aboutgdip03-art05.png)

 

 
