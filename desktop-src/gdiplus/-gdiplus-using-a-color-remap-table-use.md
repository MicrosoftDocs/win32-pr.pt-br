---
description: Remapeamento é o processo de conversão de cores em uma imagem seguindo uma tabela de remapeamento de cores. A tabela de remapeamento de cores é uma matriz de estruturas ColorMap. Cada estrutura ColorMap na matriz tem um membro oldColor e um membro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso de uma tabela de remapeamento de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090324"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="4054d-105">Uso de uma tabela de remapeamento de cores</span><span class="sxs-lookup"><span data-stu-id="4054d-105">Using a Color Remap Table</span></span>

<span data-ttu-id="4054d-106">Remapeamento é o processo de conversão de cores em uma imagem seguindo uma tabela de remapeamento de cores.</span><span class="sxs-lookup"><span data-stu-id="4054d-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="4054d-107">A tabela de remapeamento de cores é uma matriz de estruturas [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="4054d-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="4054d-108">Cada estrutura **ColorMap** na matriz tem um membro **oldColor** e um membro **newColor** .</span><span class="sxs-lookup"><span data-stu-id="4054d-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="4054d-109">Quando GDI+ desenha uma imagem, cada pixel da imagem é comparado à matriz de cores antigas.</span><span class="sxs-lookup"><span data-stu-id="4054d-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="4054d-110">Se a cor do pixel corresponde a uma cor anterior, sua cor é alterada para a nova cor correspondente.</span><span class="sxs-lookup"><span data-stu-id="4054d-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="4054d-111">As cores são alteradas apenas para renderização — os valores de cor da própria imagem (armazenados em um objeto de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ou [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) não são alterados.</span><span class="sxs-lookup"><span data-stu-id="4054d-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="4054d-112">Para desenhar uma imagem remapeada, inicialize uma matriz de estruturas [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="4054d-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="4054d-113">Passe o endereço dessa matriz para o método [**ImageAttributes:: remapeatable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) de um objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e, em seguida, passe o endereço do objeto **ImageAttributes** para o método de [métodos DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4054d-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="4054d-114">O exemplo a seguir cria um objeto de [**imagem**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) do arquivo RemapInput.bmp.</span><span class="sxs-lookup"><span data-stu-id="4054d-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="4054d-115">O código cria uma tabela de remapeamento de cores que consiste em uma única estrutura [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="4054d-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="4054d-116">O membro **oldColor** da estrutura **ColorMap** é vermelho e o membro **newColor** é azul.</span><span class="sxs-lookup"><span data-stu-id="4054d-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="4054d-117">A imagem é desenhada uma vez sem remapeamento e uma vez com remapeamento.</span><span class="sxs-lookup"><span data-stu-id="4054d-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="4054d-118">O processo de remapeamento transforma todos os pixels vermelhos em azul.</span><span class="sxs-lookup"><span data-stu-id="4054d-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

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



<span data-ttu-id="4054d-119">A ilustração a seguir mostra a imagem original à esquerda e a imagem remapeada à direita.</span><span class="sxs-lookup"><span data-stu-id="4054d-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![ilustração mostrando duas versões de uma imagem multicoloridas; a região vermelha na primeira versão é azul na segunda versão](images/colortrans7.png)

 

 



