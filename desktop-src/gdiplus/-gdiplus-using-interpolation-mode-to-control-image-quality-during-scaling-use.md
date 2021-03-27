---
description: O modo de interpolação de um objeto gráfico influencia a maneira como o Windows GDI+ escala (amplia e reduz) imagens.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967395"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="7ae23-103">Usando o modo de interpolação para controlar a qualidade da imagem durante o dimensionamento</span><span class="sxs-lookup"><span data-stu-id="7ae23-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="7ae23-104">O modo de interpolação de um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influencia a maneira como o Windows GDI+ escala (amplia e reduz) imagens.</span><span class="sxs-lookup"><span data-stu-id="7ae23-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="7ae23-105">A enumeração [**interpolamode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) em Gdiplusenums. h define vários modos de interpolação, alguns dos quais são mostrados na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="7ae23-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="7ae23-106">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="7ae23-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="7ae23-107">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="7ae23-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="7ae23-108">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="7ae23-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="7ae23-109">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="7ae23-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="7ae23-110">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="7ae23-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="7ae23-111">Para alongar uma imagem, cada pixel da imagem original deve ser mapeado para um grupo de pixels da imagem maior.</span><span class="sxs-lookup"><span data-stu-id="7ae23-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="7ae23-112">Para encolher uma imagem, cada pixel da imagem original deve ser mapeado para pixels únicos da imagem menor.</span><span class="sxs-lookup"><span data-stu-id="7ae23-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="7ae23-113">A eficácia dos algoritmos que executam esses mapeamentos determina a qualidade de uma imagem dimensionada.</span><span class="sxs-lookup"><span data-stu-id="7ae23-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="7ae23-114">Algoritmos que produzem imagens dimensionadas de qualidade superior tendem a exigir mais tempo de processamento.</span><span class="sxs-lookup"><span data-stu-id="7ae23-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="7ae23-115">Na lista anterior, InterpolationModeNearestNeighbor é o modo de qualidade mais baixa e InterpolationModeHighQualityBicubic é o modo de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="7ae23-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="7ae23-116">Para definir o modo de interpolação, passe um dos membros da enumeração de [**interpolação**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) para o método **setinterpolamode** de um objeto de [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="7ae23-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="7ae23-117">O exemplo a seguir desenha uma imagem e reduz a imagem com três modos de interpolação diferentes:</span><span class="sxs-lookup"><span data-stu-id="7ae23-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="7ae23-118">A ilustração a seguir mostra a imagem original e as três imagens menores.</span><span class="sxs-lookup"><span data-stu-id="7ae23-118">The following illustration shows the original image and the three smaller images.</span></span>

![ilustração mostrando uma imagem original grande e as três imagens menores de qualidade variável](images/grapes1.png)

 

 



