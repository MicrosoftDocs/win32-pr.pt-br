---
description: Uma transformação de dimensionamento multiplica um ou mais dos quatro componentes de cor por um número. As entradas de matriz de cores que representam o dimensionamento são dadas na tabela a seguir.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Cores de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172400"
---
# <a name="scaling-colors"></a><span data-ttu-id="f13e1-104">Cores de escala</span><span class="sxs-lookup"><span data-stu-id="f13e1-104">Scaling Colors</span></span>

<span data-ttu-id="f13e1-105">Uma transformação de dimensionamento multiplica um ou mais dos quatro componentes de cor por um número.</span><span class="sxs-lookup"><span data-stu-id="f13e1-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="f13e1-106">As entradas de matriz de cores que representam o dimensionamento são dadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f13e1-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="f13e1-107">Componentes que serão escalados</span><span class="sxs-lookup"><span data-stu-id="f13e1-107">Component to be scaled</span></span> | <span data-ttu-id="f13e1-108">Entrada da matriz</span><span class="sxs-lookup"><span data-stu-id="f13e1-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f13e1-109">Vermelho</span><span class="sxs-lookup"><span data-stu-id="f13e1-109">Red</span></span>                    | <span data-ttu-id="f13e1-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="f13e1-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="f13e1-111">Verde</span><span class="sxs-lookup"><span data-stu-id="f13e1-111">Green</span></span>                  | <span data-ttu-id="f13e1-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="f13e1-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="f13e1-113">Azul</span><span class="sxs-lookup"><span data-stu-id="f13e1-113">Blue</span></span>                   | <span data-ttu-id="f13e1-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="f13e1-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="f13e1-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="f13e1-115">Alpha</span></span>                  | <span data-ttu-id="f13e1-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="f13e1-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="f13e1-117">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="f13e1-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="f13e1-118">Depois o código escala o componente azul de cada pixel na imagem por um fator de 2.</span><span class="sxs-lookup"><span data-stu-id="f13e1-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="f13e1-119">A imagem original é desenhada ao lado da imagem transformada.</span><span class="sxs-lookup"><span data-stu-id="f13e1-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="f13e1-120">A ilustração a seguir mostra a imagem original à esquerda e a imagem em escala à direita.</span><span class="sxs-lookup"><span data-stu-id="f13e1-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Mostra quatro barras coloridas e as mesmas barras com cores diferentes.](images/colortrans3.png)

<span data-ttu-id="f13e1-122">A tabela a seguir mostra os vetores de cor para as quatro barras antes e depois do dimensionamento azul.</span><span class="sxs-lookup"><span data-stu-id="f13e1-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="f13e1-123">Veja que o componente azul na quarta barra de cores foi de 0,8 para 0,6.</span><span class="sxs-lookup"><span data-stu-id="f13e1-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="f13e1-124">Isso ocorre porque o GDI+ retém apenas a parte fracionária do resultado.</span><span class="sxs-lookup"><span data-stu-id="f13e1-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="f13e1-125">Por exemplo, (2)(0,8) = 1,6, e a parte fracionária de 1,6 é 0,6.</span><span class="sxs-lookup"><span data-stu-id="f13e1-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="f13e1-126">Reter apenas a parte fracionária garante que o resultado esteja sempre no intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f13e1-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="f13e1-127">Original</span><span class="sxs-lookup"><span data-stu-id="f13e1-127">Original</span></span>           | <span data-ttu-id="f13e1-128">Em escala</span><span class="sxs-lookup"><span data-stu-id="f13e1-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="f13e1-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="f13e1-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="f13e1-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="f13e1-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="f13e1-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="f13e1-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="f13e1-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="f13e1-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="f13e1-137">O exemplo a seguir constrói um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir do arquivo ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="f13e1-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="f13e1-138">Depois, o código escala os componentes vermelho, verde e azul de cada pixel na imagem.</span><span class="sxs-lookup"><span data-stu-id="f13e1-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="f13e1-139">Os componentes vermelhos são reduzidos em 25 por cento, os componentes verdes são reduzidos em 35 por cento e os componentes azuis são reduzidos em 50 por cento.</span><span class="sxs-lookup"><span data-stu-id="f13e1-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="f13e1-140">A ilustração a seguir mostra a imagem original à esquerda e a imagem em escala à direita.</span><span class="sxs-lookup"><span data-stu-id="f13e1-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![ilustração mostrando quatro barras coloridas, então essas barras com cores diferentes](images/colortrans4.png)

<span data-ttu-id="f13e1-142">A tabela a seguir mostra os vetores de cor para as quatro barras antes e depois do dimensionamento vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="f13e1-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="f13e1-143">Original</span><span class="sxs-lookup"><span data-stu-id="f13e1-143">Original</span></span>           | <span data-ttu-id="f13e1-144">Em escala</span><span class="sxs-lookup"><span data-stu-id="f13e1-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="f13e1-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="f13e1-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="f13e1-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="f13e1-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="f13e1-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="f13e1-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="f13e1-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="f13e1-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



