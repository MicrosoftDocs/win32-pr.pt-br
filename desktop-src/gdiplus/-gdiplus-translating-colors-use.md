---
description: Uma conversão adiciona um valor a um ou mais dos componentes de quatro cores. As entradas de matriz de cores que representam as conversões são fornecidas na tabela a seguir.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Traduzindo cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555650"
---
# <a name="translating-colors"></a><span data-ttu-id="ca70b-104">Traduzindo cores</span><span class="sxs-lookup"><span data-stu-id="ca70b-104">Translating Colors</span></span>

<span data-ttu-id="ca70b-105">Uma conversão adiciona um valor a um ou mais dos componentes de quatro cores.</span><span class="sxs-lookup"><span data-stu-id="ca70b-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="ca70b-106">As entradas de matriz de cores que representam as conversões são fornecidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca70b-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="ca70b-107">Componente a ser convertido</span><span class="sxs-lookup"><span data-stu-id="ca70b-107">Component to be translated</span></span> | <span data-ttu-id="ca70b-108">Entrada da matriz</span><span class="sxs-lookup"><span data-stu-id="ca70b-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="ca70b-109">Vermelho</span><span class="sxs-lookup"><span data-stu-id="ca70b-109">Red</span></span>                        | <span data-ttu-id="ca70b-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ca70b-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="ca70b-111">Verde</span><span class="sxs-lookup"><span data-stu-id="ca70b-111">Green</span></span>                      | <span data-ttu-id="ca70b-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ca70b-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="ca70b-113">Azul</span><span class="sxs-lookup"><span data-stu-id="ca70b-113">Blue</span></span>                       | <span data-ttu-id="ca70b-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ca70b-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="ca70b-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="ca70b-115">Alpha</span></span>                      | <span data-ttu-id="ca70b-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ca70b-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="ca70b-117">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="ca70b-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="ca70b-118">Em seguida, o código adiciona 0,75 ao componente vermelho de cada pixel na imagem.</span><span class="sxs-lookup"><span data-stu-id="ca70b-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="ca70b-119">A imagem original é desenhada ao lado da imagem transformada.</span><span class="sxs-lookup"><span data-stu-id="ca70b-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="ca70b-120">A ilustração a seguir mostra a imagem original à esquerda e a imagem transformada à direita.</span><span class="sxs-lookup"><span data-stu-id="ca70b-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![ilustração mostrando quatro barras coloridas e, em seguida, as mesmas barras com cores diferentes](images/colortrans2.png)

<span data-ttu-id="ca70b-122">A tabela a seguir lista os vetores de cores para as quatro barras antes e depois da conversão em vermelho.</span><span class="sxs-lookup"><span data-stu-id="ca70b-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="ca70b-123">Observe que, como o valor máximo para um componente de cor é 1, o componente vermelho na segunda linha não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ca70b-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="ca70b-124">(Da mesma forma, o valor mínimo para um componente de cor é 0).</span><span class="sxs-lookup"><span data-stu-id="ca70b-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="ca70b-125">Original</span><span class="sxs-lookup"><span data-stu-id="ca70b-125">Original</span></span>           | <span data-ttu-id="ca70b-126">Traduzido</span><span class="sxs-lookup"><span data-stu-id="ca70b-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="ca70b-127">Preto (0, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="ca70b-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="ca70b-129">Vermelho (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="ca70b-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="ca70b-131">Verde (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="ca70b-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="ca70b-133">Azul (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="ca70b-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="ca70b-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



