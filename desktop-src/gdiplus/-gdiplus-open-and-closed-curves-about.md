---
description: 'A ilustração a seguir mostra duas curvas: uma aberta e outra fechada.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curvas abertas e fechadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552118"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="d9d18-103">Curvas abertas e fechadas</span><span class="sxs-lookup"><span data-stu-id="d9d18-103">Open and Closed Curves</span></span>

<span data-ttu-id="d9d18-104">A ilustração a seguir mostra duas curvas: uma aberta e outra fechada.</span><span class="sxs-lookup"><span data-stu-id="d9d18-104">The following illustration shows two curves: one open and one closed.</span></span>

![ilustração de uma curva aberta (uma linha curva) e uma curva fechada (a estrutura de uma forma)](images/aboutgdip02-art24.png)

<span data-ttu-id="d9d18-106">Curvas fechadas têm um interior e, portanto, podem ser preenchidas com um pincel.</span><span class="sxs-lookup"><span data-stu-id="d9d18-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="d9d18-107">A [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) no Windows GDI+ fornece os seguintes métodos para preencher figuras e curvas fechadas: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)e [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="d9d18-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="d9d18-108">Sempre que você chamar um desses métodos, deverá passar o endereço de um dos tipos de pincel específicos ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)ou [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) como um argumento.</span><span class="sxs-lookup"><span data-stu-id="d9d18-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="d9d18-109">O método [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) é um complemento para o método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) .</span><span class="sxs-lookup"><span data-stu-id="d9d18-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="d9d18-110">Assim como o método DrawArc desenha uma parte da estrutura de tópicos de uma elipse, o método FillPie preenche uma parte do interior de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="d9d18-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="d9d18-111">O exemplo a seguir desenha um arco e preenche a parte correspondente do interior da elipse.</span><span class="sxs-lookup"><span data-stu-id="d9d18-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="d9d18-112">A ilustração a seguir mostra o arco e a pizza preenchida.</span><span class="sxs-lookup"><span data-stu-id="d9d18-112">The following illustration shows the arc and the filled pie.</span></span>

![ilustração mostrando um segmento de uma elipse preenchida](images/aboutgdip02-art25.png)

<span data-ttu-id="d9d18-114">O método [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) é um complemento para o método [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="d9d18-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="d9d18-115">Ambos os métodos fecham automaticamente a curva conectando o ponto final ao ponto inicial.</span><span class="sxs-lookup"><span data-stu-id="d9d18-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="d9d18-116">O exemplo a seguir desenha uma curva que passa por (0, 0), (60, 20) e (40, 50).</span><span class="sxs-lookup"><span data-stu-id="d9d18-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="d9d18-117">Em seguida, a curva é fechada automaticamente conectando (40, 50) ao ponto inicial (0, 0), e o interior é preenchido com uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="d9d18-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="d9d18-118">Um caminho pode consistir em várias figuras (subcaminhos).</span><span class="sxs-lookup"><span data-stu-id="d9d18-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="d9d18-119">O método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) preenche o interior de cada figura.</span><span class="sxs-lookup"><span data-stu-id="d9d18-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="d9d18-120">Se uma figura não for fechada, o método **Graphics:: FillPath** preencherá a área que seria incluída se a figura fosse fechada.</span><span class="sxs-lookup"><span data-stu-id="d9d18-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="d9d18-121">O exemplo a seguir desenha e preenche um caminho que consiste em um arco, um spline Cardeal, uma cadeia de caracteres e uma pizza.</span><span class="sxs-lookup"><span data-stu-id="d9d18-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="d9d18-122">A ilustração a seguir mostra o caminho antes e depois que ele é preenchido com um pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="d9d18-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="d9d18-123">Observe que o texto na cadeia de caracteres é descrito, mas não preenchido, pelo método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) .</span><span class="sxs-lookup"><span data-stu-id="d9d18-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="d9d18-124">É o método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) que pinta os Interiors dos caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9d18-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![ilustração que duas vezes mostra texto e uma curva aberta e fechada; Eles estão vazios na primeira vez e são preenchidos da segunda vez](images/aboutgdip02-art26.png)

 

 



