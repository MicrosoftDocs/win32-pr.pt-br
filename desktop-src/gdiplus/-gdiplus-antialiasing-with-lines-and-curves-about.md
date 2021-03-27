---
description: Ao usar o Windows GDI+ para desenhar uma linha, você fornece o ponto inicial e o ponto final da linha, mas não precisa fornecer informações sobre os pixels individuais na linha.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Suavização com linhas e curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661950"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="9315d-103">Suavização com linhas e curvas</span><span class="sxs-lookup"><span data-stu-id="9315d-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="9315d-104">Ao usar o Windows GDI+ para desenhar uma linha, você fornece o ponto inicial e o ponto final da linha, mas não precisa fornecer informações sobre os pixels individuais na linha.</span><span class="sxs-lookup"><span data-stu-id="9315d-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="9315d-105">O GDI+ funciona em conjunto com o software de driver de vídeo para determinar quais pixels serão ativados para mostrar a linha em um dispositivo de vídeo específico.</span><span class="sxs-lookup"><span data-stu-id="9315d-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="9315d-106">Considere uma linha vermelha reta que vai do ponto (4, 2) até o ponto (16, 10).</span><span class="sxs-lookup"><span data-stu-id="9315d-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="9315d-107">Suponha que o sistema de coordenadas tem sua origem no canto superior esquerdo e que a unidade de medida é o pixel.</span><span class="sxs-lookup"><span data-stu-id="9315d-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="9315d-108">Suponha também que o eixo X aponta para a direita e o eixo Y aponta para baixo.</span><span class="sxs-lookup"><span data-stu-id="9315d-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="9315d-109">A ilustração a seguir mostra uma exibição ampliada da linha vermelha desenhada em uma tela de fundo multicolorida.</span><span class="sxs-lookup"><span data-stu-id="9315d-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![ilustração mostrando pixels vermelhos sólidos em um plano de fundo multicolorido](images/aboutgdip02-art33.png)

<span data-ttu-id="9315d-111">Observe que os pixels vermelhos usados para renderizar a linha são opacos.</span><span class="sxs-lookup"><span data-stu-id="9315d-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="9315d-112">Não há pixels parcialmente transparentes envolvidos na exibição da linha.</span><span class="sxs-lookup"><span data-stu-id="9315d-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="9315d-113">Esse tipo de renderização de linha dá à linha uma aparência irregular e a linha parece um pouco como uma escada.</span><span class="sxs-lookup"><span data-stu-id="9315d-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="9315d-114">Essa técnica de representar uma linha com uma escada é chamada de serrilhado; a escada é um alias para a linha teórica.</span><span class="sxs-lookup"><span data-stu-id="9315d-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="9315d-115">Uma técnica mais sofisticada para renderizar uma linha envolve o uso de pixels parcialmente transparentes juntamente com pixels puros de vermelho.</span><span class="sxs-lookup"><span data-stu-id="9315d-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="9315d-116">Os pixels são definidos como vermelho puro ou com alguma mistura de vermelho e a cor do plano de fundo, dependendo de quão perto eles estão para a linha.</span><span class="sxs-lookup"><span data-stu-id="9315d-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="9315d-117">Esse tipo de renderização é chamado de suavização e resulta em uma linha que o olho humano percebe como mais suave.</span><span class="sxs-lookup"><span data-stu-id="9315d-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="9315d-118">A ilustração a seguir mostra como determinados pixels são mesclados com a tela de fundo para produzir uma linha suavizada.</span><span class="sxs-lookup"><span data-stu-id="9315d-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![ilustração mostrando pixels que são tons de vermelho no mesmo plano de fundo](images/aboutgdip02-art34.png)

<span data-ttu-id="9315d-120">A anti-aliasing (suavização) também pode ser aplicada a curvas.</span><span class="sxs-lookup"><span data-stu-id="9315d-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="9315d-121">A ilustração a seguir mostra uma exibição ampliada de uma elipse suavizada.</span><span class="sxs-lookup"><span data-stu-id="9315d-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![ilustração de uma elipse composta por diferentes tons de pixels azuis em um plano de fundo branco](images/aboutgdip02-art35.png)

<span data-ttu-id="9315d-123">A ilustração a seguir mostra a mesma elipse em seu tamanho real, uma vez sem suavização e outra com suavização.</span><span class="sxs-lookup"><span data-stu-id="9315d-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![captura de tela de duas elipses: a que está com a suavização aparece mais suave](images/aboutgdip02-art36.png)

<span data-ttu-id="9315d-125">Para desenhar linhas e curvas que usam anti-aliasing, crie um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passe *SmoothingModeAntiAlias* para o método [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="9315d-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="9315d-126">Em seguida, chame um dos métodos de desenho do mesmo objeto de **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="9315d-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="9315d-127">**SmoothingModeAntiAlias** é um elemento da enumeração [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="9315d-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



