---
description: A distorção aumenta ou diminui um componente de cor em uma quantidade proporcional a outro componente de cor.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Distorcendo cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091462"
---
# <a name="shearing-colors"></a><span data-ttu-id="59538-103">Distorcendo cores</span><span class="sxs-lookup"><span data-stu-id="59538-103">Shearing Colors</span></span>

<span data-ttu-id="59538-104">A distorção aumenta ou diminui um componente de cor em uma quantidade proporcional a outro componente de cor.</span><span class="sxs-lookup"><span data-stu-id="59538-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="59538-105">Por exemplo, considere a transformação em que o componente vermelho é aumentado pela metade do valor do componente azul.</span><span class="sxs-lookup"><span data-stu-id="59538-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="59538-106">Nessa transformação, a cor (0,2, 0,5, 1) seria (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="59538-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="59538-107">O novo componente vermelho é 0,2 + (1/2)(1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="59538-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="59538-108">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="59538-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="59538-109">Em seguida, o código se aplica à transformação de distorção descrita no parágrafo anterior para cada pixel da imagem.</span><span class="sxs-lookup"><span data-stu-id="59538-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="59538-110">A ilustração a seguir mostra a imagem original à esquerda e a imagem distorcida à direita.</span><span class="sxs-lookup"><span data-stu-id="59538-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![ilustração mostrando quatro barras coloridas e, em seguida, as mesmas barras com cores diferentes](images/colortrans6.png)

<span data-ttu-id="59538-112">A tabela a seguir mostra os vetores de cor para as quatro barras antes e depois da transformação distorção.</span><span class="sxs-lookup"><span data-stu-id="59538-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="59538-113">Original</span><span class="sxs-lookup"><span data-stu-id="59538-113">Original</span></span>           | <span data-ttu-id="59538-114">Distorcido</span><span class="sxs-lookup"><span data-stu-id="59538-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="59538-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="59538-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="59538-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="59538-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="59538-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="59538-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="59538-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="59538-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="59538-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



