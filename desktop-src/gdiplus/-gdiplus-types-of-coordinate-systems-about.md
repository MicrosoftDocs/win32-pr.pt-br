---
description: 'O Windows GDI+ usa três espaços de coordenadas: mundo, página e dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120621"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="3b094-103">Tipos de sistemas de coordenadas</span><span class="sxs-lookup"><span data-stu-id="3b094-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="3b094-104">O Windows GDI+ usa três espaços de coordenadas: mundo, página e dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b094-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="3b094-105">Quando você faz a chamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , os pontos que passa para o método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) – (0, 0) e (160, 80) — estão no espaço de coordenadas do mundo.</span><span class="sxs-lookup"><span data-stu-id="3b094-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="3b094-106">Antes que o GDI+ possa desenhar a linha na tela, as coordenadas passam por uma sequência de transformações.</span><span class="sxs-lookup"><span data-stu-id="3b094-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="3b094-107">Uma transformação converte coordenadas mundiais em coordenadas de página e outra transformação converte coordenadas de página em coordenadas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b094-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="3b094-108">Suponha que você queira trabalhar com um sistema de coordenadas cuja origem está no corpo da área de cliente em vez do canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="3b094-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="3b094-109">Digamos, por exemplo, que você queira que a origem esteja a 100 pixels da borda esquerda da área de cliente e a 50 pixels da parte superior da área de cliente.</span><span class="sxs-lookup"><span data-stu-id="3b094-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="3b094-110">A ilustração a seguir mostra esse sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="3b094-110">The following illustration shows such a coordinate system.</span></span>

![captura de tela de uma janela que contém eixos de coordenadas rotulados](images/aboutgdip05-art01.png)

<span data-ttu-id="3b094-112">Quando faz a chamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, você obtém a linha mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b094-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![captura de tela da janela anterior, mas com uma linha azul sendo estendida diagonalmente da origem](images/aboutgdip05-art02.png)

<span data-ttu-id="3b094-114">As coordenadas dos pontos de extremidade da sua linha nos três espaços de coordenadas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3b094-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="3b094-115">Space</span><span class="sxs-lookup"><span data-stu-id="3b094-115">Space</span></span>       |  <span data-ttu-id="3b094-116">Coordenadas do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3b094-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="3b094-117">World (Mundo)</span><span class="sxs-lookup"><span data-stu-id="3b094-117">World</span></span>  | <span data-ttu-id="3b094-118">(0, 0) a (160, 80)</span><span class="sxs-lookup"><span data-stu-id="3b094-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="3b094-119">?</span><span class="sxs-lookup"><span data-stu-id="3b094-119">Page</span></span>   | <span data-ttu-id="3b094-120">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="3b094-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="3b094-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3b094-121">Device</span></span> | <span data-ttu-id="3b094-122">(100, 50) a (260, 130)</span><span class="sxs-lookup"><span data-stu-id="3b094-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="3b094-123">Observe que o espaço de coordenadas de página tem sua origem no canto superior esquerdo da área de cliente; sempre será esse o caso.</span><span class="sxs-lookup"><span data-stu-id="3b094-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="3b094-124">Observe também que, como a unidade de medida é o pixel, as coordenadas do dispositivo são as mesmas que as coordenadas da página.</span><span class="sxs-lookup"><span data-stu-id="3b094-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="3b094-125">Se você definir a unidade de medida como algo diferente de pixels (por exemplo, polegadas), as coordenadas do dispositivo serão diferentes das coordenadas da página.</span><span class="sxs-lookup"><span data-stu-id="3b094-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="3b094-126">A transformação que mapeia coordenadas mundiais para coordenadas de página é chamada de *transformação mundial* e é mantida por um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="3b094-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="3b094-127">No exemplo anterior, a transformação do mundo é uma tradução 100 unidades na direção x e 50 unidades na direção y.</span><span class="sxs-lookup"><span data-stu-id="3b094-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="3b094-128">O exemplo a seguir define a transformação mundial de um objeto **Graphics** e, em seguida, usa esse objeto **Graphics** para desenhar a linha mostrada na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="3b094-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="3b094-129">A transformação que mapeia coordenadas de página para coordenadas de dispositivo é chamada de *transformação de página*.</span><span class="sxs-lookup"><span data-stu-id="3b094-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="3b094-130">A classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece quatro métodos para manipular e inspecionar a transformação página: [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**gráficos:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)e [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="3b094-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="3b094-131">A classe **Graphics** também fornece dois métodos, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) e [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), para examinar os pontos horizontais e verticais por polegada do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b094-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="3b094-132">Você pode usar o método [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar uma unidade de medida.</span><span class="sxs-lookup"><span data-stu-id="3b094-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="3b094-133">O exemplo a seguir desenha uma linha de (0, 0) para (2, 1) em que o ponto (2, 1) é de 2 polegadas à direita e 1 polegada para baixo a partir do ponto (0, 0).</span><span class="sxs-lookup"><span data-stu-id="3b094-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="3b094-134">Se você não especificar uma largura de caneta ao construir a caneta, o exemplo anterior desenhará uma linha com uma polegada de largura.</span><span class="sxs-lookup"><span data-stu-id="3b094-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="3b094-135">Você pode especificar a largura da caneta no segundo argumento para o construtor de [**caneta**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :</span><span class="sxs-lookup"><span data-stu-id="3b094-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="3b094-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="3b094-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="3b094-137">Se presumirmos que o dispositivo de vídeo tenha 96 pontos por polegada na direção horizontal e 96 pontos por polegada na direção vertical, os pontos de extremidade da linha no exemplo anterior têm as seguintes coordenadas nos três espaços de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="3b094-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="3b094-138">Space</span><span class="sxs-lookup"><span data-stu-id="3b094-138">Space</span></span>       | <span data-ttu-id="3b094-139">Coordenadas do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3b094-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="3b094-140">World (Mundo)</span><span class="sxs-lookup"><span data-stu-id="3b094-140">World</span></span>  | <span data-ttu-id="3b094-141">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3b094-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="3b094-142">?</span><span class="sxs-lookup"><span data-stu-id="3b094-142">Page</span></span>   | <span data-ttu-id="3b094-143">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3b094-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="3b094-144">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3b094-144">Device</span></span> | <span data-ttu-id="3b094-145">(0, 0) a (192, 96)</span><span class="sxs-lookup"><span data-stu-id="3b094-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="3b094-146">É possível combinar as transformações global e de página para obter uma variedade de resultados.</span><span class="sxs-lookup"><span data-stu-id="3b094-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="3b094-147">Por exemplo, suponha que você queira usar polegadas como a unidade de medida e queira que a origem se seu sistema de coordenadas esteja a 2 polegadas da borda esquerda da área de cliente e a 1/2 polegada da parte superior da área de cliente.</span><span class="sxs-lookup"><span data-stu-id="3b094-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="3b094-148">O exemplo a seguir define as transformações World e Page de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e, em seguida, desenha uma linha de (0, 0) para (2, 1).</span><span class="sxs-lookup"><span data-stu-id="3b094-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="3b094-149">A ilustração a seguir mostra a linha e o sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="3b094-149">The following illustration shows the line and coordinate system.</span></span>

![captura de tela da janela anterior, mas mais larga, com os eixos posicionados à esquerda e rotulados de forma diferente](images/aboutgdip05-art03.png)

<span data-ttu-id="3b094-151">Se presumirmos que o dispositivo de vídeo tenha 96 pontos por polegada na direção horizontal e 96 pontos por polegada na direção vertical, os pontos de extremidade da linha no exemplo anterior têm as seguintes coordenadas nos três espaços de coordenadas:</span><span class="sxs-lookup"><span data-stu-id="3b094-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="3b094-152">Space</span><span class="sxs-lookup"><span data-stu-id="3b094-152">Space</span></span>       | <span data-ttu-id="3b094-153">Coordenadas do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3b094-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="3b094-154">World (Mundo)</span><span class="sxs-lookup"><span data-stu-id="3b094-154">World</span></span>  | <span data-ttu-id="3b094-155">(0, 0) a (2, 1)</span><span class="sxs-lookup"><span data-stu-id="3b094-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="3b094-156">?</span><span class="sxs-lookup"><span data-stu-id="3b094-156">Page</span></span>   | <span data-ttu-id="3b094-157">(2, 0.5) a (4, 1.5)</span><span class="sxs-lookup"><span data-stu-id="3b094-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="3b094-158">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="3b094-158">Device</span></span> | <span data-ttu-id="3b094-159">(192, 48) a (384, 144)</span><span class="sxs-lookup"><span data-stu-id="3b094-159">(192, 48) to (384, 144)</span></span> |



 

 

 
