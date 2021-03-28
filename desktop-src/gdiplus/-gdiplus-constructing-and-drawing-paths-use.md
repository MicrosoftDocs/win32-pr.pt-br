---
description: Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e assim por diante) que podem ser manipulados e desenhados como uma única unidade. Um caminho pode ser dividido em figuras que são abertas ou fechadas. Uma figura pode conter vários primitivos.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Construindo e desenhando demarcadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988889"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="4df6e-105">Construindo e desenhando demarcadores</span><span class="sxs-lookup"><span data-stu-id="4df6e-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="4df6e-106">Um caminho é uma sequência de primitivos gráficos (linhas, retângulos, curvas, texto e assim por diante) que podem ser manipulados e desenhados como uma única unidade.</span><span class="sxs-lookup"><span data-stu-id="4df6e-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="4df6e-107">Um caminho pode ser dividido em *figuras* que são abertas ou fechadas.</span><span class="sxs-lookup"><span data-stu-id="4df6e-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="4df6e-108">Uma figura pode conter vários primitivos.</span><span class="sxs-lookup"><span data-stu-id="4df6e-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="4df6e-109">Você pode desenhar um caminho chamando o método [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e pode preencher um caminho chamando o método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) da classe **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="4df6e-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="4df6e-110">Os tópicos a seguir abrangem caminhos com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="4df6e-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="4df6e-111">Criar figuras usando linhas, curvas e formas</span><span class="sxs-lookup"><span data-stu-id="4df6e-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="4df6e-112">Preenchendo figuras abertas</span><span class="sxs-lookup"><span data-stu-id="4df6e-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 



