---
description: 'Você pode habilitar a correção gama para um pincel de gradiente passando TRUE para o método PathGradientBrush:: SetGammaCorrection desse pincel.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Aplicando a correção gama a um gradiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091490"
---
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="57922-103">Aplicando a correção gama a um gradiente</span><span class="sxs-lookup"><span data-stu-id="57922-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="57922-104">Você pode habilitar a correção gama para um pincel de gradiente passando **true** para o método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) desse pincel.</span><span class="sxs-lookup"><span data-stu-id="57922-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="57922-105">Você pode desabilitar a correção gama passando **false** para o método **PathGradientBrush:: SetGammaCorrection** .</span><span class="sxs-lookup"><span data-stu-id="57922-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="57922-106">A correção gama é desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="57922-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="57922-107">O exemplo a seguir cria um pincel de gradiente linear e usa esse pincel para preencher dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="57922-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="57922-108">O primeiro retângulo é preenchido sem a correção gama e o segundo retângulo é preenchido com a correção gama.</span><span class="sxs-lookup"><span data-stu-id="57922-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



<span data-ttu-id="57922-109">A ilustração a seguir mostra os dois retângulos preenchidos.</span><span class="sxs-lookup"><span data-stu-id="57922-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="57922-110">O retângulo superior, que não tem a correção gama, aparece escuro no meio.</span><span class="sxs-lookup"><span data-stu-id="57922-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="57922-111">O retângulo inferior, que tem a correção gama, parece ter mais intensidade uniforme.</span><span class="sxs-lookup"><span data-stu-id="57922-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![ilustração mostrando dois retângulos: o preenchimento colorido do primeiro varia em intensidade, o preenchimento da segunda varia menos](images/gammagradient1.png)

<span data-ttu-id="57922-113">O exemplo a seguir cria um pincel de gradiente de caminho com base em um caminho em formato de estrela.</span><span class="sxs-lookup"><span data-stu-id="57922-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="57922-114">O código usa o pincel de gradiente de caminho com a correção gama desabilitada (o padrão) para preencher o caminho.</span><span class="sxs-lookup"><span data-stu-id="57922-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="57922-115">Em seguida, o código passa **true** para o método [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) para habilitar a correção gama para o pincel de gradiente de caminho.</span><span class="sxs-lookup"><span data-stu-id="57922-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="57922-116">A chamada para [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) define a transformação mundial de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que a chamada subsequente para [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Preencha uma estrela que fica à direita da primeira estrela.</span><span class="sxs-lookup"><span data-stu-id="57922-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="57922-117">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="57922-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="57922-118">A estrela à direita tem correção de gama.</span><span class="sxs-lookup"><span data-stu-id="57922-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="57922-119">Observe que a estrela à esquerda, que não tem a correção gama, tem áreas que parecem escuras.</span><span class="sxs-lookup"><span data-stu-id="57922-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![ilustração de 2 5-pontos de início com preenchimento gradiente colorido; a primeira tem áreas escuras, a segunda não](images/gammagradient2.png)

 

 



