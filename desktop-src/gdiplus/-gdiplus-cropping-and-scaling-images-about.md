---
title: Sobre o corte e dimensionamento de imagens de GDI+
description: Você pode usar o método DrawImage da classe Graphics para desenhar e posicionar imagens.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091473"
---
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="6d0a5-103">Sobre o corte e dimensionamento de imagens de GDI+</span><span class="sxs-lookup"><span data-stu-id="6d0a5-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="6d0a5-104">Você pode usar o método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar e posicionar imagens.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="6d0a5-105">O DrawImage é um método sobrecarregado, portanto, há várias maneiras pelas quais você pode fornecê-lo com argumentos.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="6d0a5-106">Uma variação do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) recebe o endereço de um objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e uma referência a um objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) .</span><span class="sxs-lookup"><span data-stu-id="6d0a5-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="6d0a5-107">O retângulo especifica o destino para a operação de desenho; ou seja, ele especifica o retângulo no qual a imagem será desenhada.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="6d0a5-108">Se o tamanho do retângulo de destino for diferente do tamanho da imagem original, a escala dela será ajustada para caber no retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="6d0a5-109">O exemplo a seguir desenha a mesma imagem três vezes: uma vez sem dimensionamento, uma vez com uma expansão e uma vez com uma compactação.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="6d0a5-110">O código anterior, junto com um arquivo específico, Spiral.png, produziu a saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![ilustração mostrando três versões de uma imagem: normal, ampliada e reduzida para metade do tamanho original](images/aboutgdip03-art06.png)

<span data-ttu-id="6d0a5-112">Algumas variações do método [**Graphics::D RawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) têm um parâmetro de retângulo de origem, bem como um parâmetro de retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="6d0a5-113">O retângulo de origem especifica a parte da imagem original que será desenhada.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="6d0a5-114">O retângulo de destino especifica onde a parte da imagem será desenhada.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="6d0a5-115">Se o tamanho do retângulo de destino for diferente do tamanho do retângulo de origem, a imagem será dimensionada para se ajustar ao retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="6d0a5-116">O exemplo a seguir constrói um objeto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) a partir do arquivo Runner.jpg.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="6d0a5-117">Toda a imagem é desenhada sem nenhuma escala em (0, 0).</span><span class="sxs-lookup"><span data-stu-id="6d0a5-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="6d0a5-118">Em seguida, uma pequena parte da imagem é desenhada duas vezes: uma expandida e outra compactada.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


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



<span data-ttu-id="6d0a5-119">A ilustração a seguir mostra a imagem sem escala e as partes da imagem compactada e expandida.</span><span class="sxs-lookup"><span data-stu-id="6d0a5-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![captura de tela mostrando uma imagem, uma parte da imagem compactada e, em seguida, a mesma parte expandida](images/aboutgdip03-art07.png)

 

 



