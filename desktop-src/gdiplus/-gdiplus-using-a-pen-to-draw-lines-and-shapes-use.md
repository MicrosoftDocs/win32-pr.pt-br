---
description: 'A classe Graphics fornece uma variedade de métodos de desenho, incluindo aqueles mostrados na lista a seguir:'
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Usando uma caneta para desenhar linhas e formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090323"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="d650c-103">Usando uma caneta para desenhar linhas e formas</span><span class="sxs-lookup"><span data-stu-id="d650c-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="d650c-104">A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece uma variedade de métodos de desenho, incluindo aqueles mostrados na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="d650c-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="d650c-105">[Métodos DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="d650c-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="d650c-106">[Métodos DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="d650c-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="d650c-107">[Métodos DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="d650c-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="d650c-108">[Métodos DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="d650c-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="d650c-109">**Gráficos::D rawPath**</span><span class="sxs-lookup"><span data-stu-id="d650c-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="d650c-110">[Métodos DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="d650c-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="d650c-111">[Métodos DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="d650c-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="d650c-112">Um dos argumentos que você passa para esse método de desenho é o endereço de um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="d650c-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="d650c-113">Os tópicos a seguir abordam o uso de canetas com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="d650c-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="d650c-114">Uso de uma caneta para desenhar linhas e retângulos</span><span class="sxs-lookup"><span data-stu-id="d650c-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="d650c-115">Definindo a largura e o alinhamento da caneta</span><span class="sxs-lookup"><span data-stu-id="d650c-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="d650c-116">Desenhando uma linha com limites de linha</span><span class="sxs-lookup"><span data-stu-id="d650c-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="d650c-117">Unindo linhas</span><span class="sxs-lookup"><span data-stu-id="d650c-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="d650c-118">Desenhando uma linha tracejada personalizada</span><span class="sxs-lookup"><span data-stu-id="d650c-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="d650c-119">Desenhando uma linha preenchida com uma textura</span><span class="sxs-lookup"><span data-stu-id="d650c-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



