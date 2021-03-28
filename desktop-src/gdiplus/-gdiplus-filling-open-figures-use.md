---
description: 'Você pode preencher um caminho passando o endereço de um objeto GraphicsPath para o método Graphics:: FillPath.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Preenchendo figuras abertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561645"
---
# <a name="filling-open-figures"></a><span data-ttu-id="c5af9-103">Preenchendo figuras abertas</span><span class="sxs-lookup"><span data-stu-id="c5af9-103">Filling Open Figures</span></span>

<span data-ttu-id="c5af9-104">Você pode preencher um caminho passando o endereço de um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) para o método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) .</span><span class="sxs-lookup"><span data-stu-id="c5af9-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="c5af9-105">O método **Graphics:: FillPath** preenche o caminho de acordo com o modo de preenchimento (alternativo ou de vento) definido atualmente para o caminho.</span><span class="sxs-lookup"><span data-stu-id="c5af9-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="c5af9-106">Se o caminho tiver figuras abertas, ele será preenchido como se essas figuras que foram fechadas.</span><span class="sxs-lookup"><span data-stu-id="c5af9-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="c5af9-107">O GDI+ Fecha uma figura desenhando uma linha reta de seu ponto de extremidade até o ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="c5af9-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="c5af9-108">O exemplo a seguir cria um caminho que tem uma figura aberta (um arco) e uma figura fechada (uma elipse).</span><span class="sxs-lookup"><span data-stu-id="c5af9-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="c5af9-109">O método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) preenche o caminho de acordo com o modo de preenchimento padrão, que é FillModeAlternate.</span><span class="sxs-lookup"><span data-stu-id="c5af9-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="c5af9-110">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="c5af9-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="c5af9-111">Observe que o caminho é preenchido (de acordo com FillModeAlternate) como se a figura aberta fosse fechada por uma linha reta de seu ponto final até seu ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="c5af9-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![ilustração mostrando uma elipse alta que sobrepõe a metade inferior de uma elipse larga; a União está preenchida, mas a interseção está vazia](images/fillopenpath.png)

 

 



