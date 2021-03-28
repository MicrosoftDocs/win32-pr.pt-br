---
description: Ao preencher uma forma, você deve passar o endereço de um objeto de pincel para um dos métodos Fill da classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Desenho com pincéis opacos e semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091471"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="51129-103">Desenho com pincéis opacos e semitransparentes</span><span class="sxs-lookup"><span data-stu-id="51129-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="51129-104">Ao preencher uma forma, você deve passar o endereço de um objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) para um dos métodos Fill da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="51129-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="51129-105">O parâmetro One do construtor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) é um objeto [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="51129-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="51129-106">Para preencher uma forma opaca, defina o componente alfa da cor como 255.</span><span class="sxs-lookup"><span data-stu-id="51129-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="51129-107">Para preencher uma forma semitransparente, defina o componente alfa para qualquer valor de 1 a 254.</span><span class="sxs-lookup"><span data-stu-id="51129-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="51129-108">Ao preencher uma forma semitransparente, a cor da forma é combinada com as cores da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="51129-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="51129-109">O componente alfa Especifica como as cores de forma e de plano de fundo são misturadas; os valores Alfa próximos 0 colocam mais peso nas cores do plano de fundo, e os valores Alfa próximos a 255 colocam mais importância na cor da forma.</span><span class="sxs-lookup"><span data-stu-id="51129-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="51129-110">O exemplo a seguir desenha uma imagem e, em seguida, preenche as três reticências que se sobrepõem à imagem.</span><span class="sxs-lookup"><span data-stu-id="51129-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="51129-111">A primeira elipse usa um componente alfa de 255, portanto, é opaca.</span><span class="sxs-lookup"><span data-stu-id="51129-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="51129-112">As segunda e terceira elipses usam um componente alfa de 128, para que sejam semitransparentes; É possível ver a imagem da tela de fundo pelas elipses.</span><span class="sxs-lookup"><span data-stu-id="51129-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="51129-113">A chamada para [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) faz com que a combinação da terceira elipse seja feita em conjunto com a correção gama.</span><span class="sxs-lookup"><span data-stu-id="51129-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="51129-114">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="51129-114">The following illustration shows the output of the preceding code.</span></span>

![ilustração mostrando uma imagem sobreposta por três elipses: uma opaca, uma levemente transparente, uma muito transparente](images/compqualellipse.png)

 

 



