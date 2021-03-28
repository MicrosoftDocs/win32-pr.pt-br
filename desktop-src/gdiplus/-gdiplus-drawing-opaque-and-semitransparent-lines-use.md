---
description: Ao desenhar uma linha, você deve passar o endereço de um objeto de caneta para o método DrawLine da classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Desenhar linhas opacas e semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558584"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="58367-103">Desenhar linhas opacas e semitransparentes</span><span class="sxs-lookup"><span data-stu-id="58367-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="58367-104">Ao desenhar uma linha, você deve passar o endereço de um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="58367-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="58367-105">Um dos parâmetros do construtor de **caneta** é um objeto de [**cor**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="58367-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="58367-106">Para desenhar uma linha opaca, defina o componente alfa da cor como 255.</span><span class="sxs-lookup"><span data-stu-id="58367-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="58367-107">Para desenhar uma linha semitransparente, defina o componente alfa para qualquer valor de 1 a 254.</span><span class="sxs-lookup"><span data-stu-id="58367-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="58367-108">Ao desenhar uma linha semitransparente em uma tela de fundo, a cor da linha é combinada com as cores da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="58367-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="58367-109">O componente alfa Especifica como as cores de linha e de segundo plano são misturadas; os valores Alfa próximos 0 colocam mais peso nas cores do plano de fundo, e os valores Alfa próximos a 255 colocam mais importância na cor da linha.</span><span class="sxs-lookup"><span data-stu-id="58367-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="58367-110">O exemplo a seguir desenha uma imagem e, em seguida, desenha três linhas que usam a imagem como um plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="58367-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="58367-111">A primeira linha usa um componente alfa de 255, portanto, é opaca.</span><span class="sxs-lookup"><span data-stu-id="58367-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="58367-112">As segunda e terceira linhas usam um componente alfa de 128, para que sejam semitransparentes. É possível ver a imagem da tela de fundo pelas linhas.</span><span class="sxs-lookup"><span data-stu-id="58367-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="58367-113">A chamada para [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) faz com que a combinação da terceira linha seja feita em conjunto com a correção gama.</span><span class="sxs-lookup"><span data-stu-id="58367-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="58367-114">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="58367-114">The following illustration shows the output of the preceding code.</span></span>

![ilustração mostrando uma imagem sobreposta por três linhas largas: uma opaca, uma levemente transparente e uma muito transparente](images/compqualline.png)

 

 



