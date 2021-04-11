---
description: Para criar um caminho e selecioná-lo em um controlador de domínio, primeiro é necessário definir os pontos que o descrevem.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Criação de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165061"
---
# <a name="path-creation"></a><span data-ttu-id="cb4cf-103">Criação de caminho</span><span class="sxs-lookup"><span data-stu-id="cb4cf-103">Path Creation</span></span>

<span data-ttu-id="cb4cf-104">Para criar um caminho e selecioná-lo em um controlador de domínio, primeiro é necessário definir os pontos que o descrevem.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="cb4cf-105">Isso é feito chamando a função [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , especificando as funções de desenho apropriadas e, em seguida, chamando a função [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="cb4cf-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="cb4cf-106">Essa combinação de funções (**BeginPath**, funções de desenho e **EndPath**) constitui um *colchete de caminho*.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="cb4cf-107">A seguir está a lista de funções de desenho que podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="cb4cf-108">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="cb4cf-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="cb4cf-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="cb4cf-111">**Chord**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="cb4cf-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="cb4cf-113">**Ellipse**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="cb4cf-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="cb4cf-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="cb4cf-116">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="cb4cf-117">**Pizza**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="cb4cf-118">**PolyBezierSegment**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="cb4cf-119">**Polibézierto**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="cb4cf-120">**Metaempate**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="cb4cf-121">**Polígono**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="cb4cf-122">**Múltipla**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="cb4cf-123">**Polilineto**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="cb4cf-124">**Polipolygon**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="cb4cf-125">**Polyline**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="cb4cf-126">**Nele**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="cb4cf-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="cb4cf-128">**Texto**</span><span class="sxs-lookup"><span data-stu-id="cb4cf-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="cb4cf-129">Quando um aplicativo chama [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), o sistema seleciona o caminho associado no controlador de domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="cb4cf-130">(Se outro caminho tiver sido selecionado anteriormente no controlador de domínio, o sistema excluirá esse caminho sem salvá-lo.) Depois que o sistema seleciona o caminho no controlador de domínio, um aplicativo pode operar no caminho de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="cb4cf-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="cb4cf-131">Desenhe o contorno do caminho (usando a caneta atual).</span><span class="sxs-lookup"><span data-stu-id="cb4cf-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="cb4cf-132">Pinte o interior do caminho (usando o pincel atual).</span><span class="sxs-lookup"><span data-stu-id="cb4cf-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="cb4cf-133">Desenhe a estrutura de tópicos e preencha o interior do caminho.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="cb4cf-134">Modifique o caminho (convertendo curvas em segmentos de linha).</span><span class="sxs-lookup"><span data-stu-id="cb4cf-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="cb4cf-135">Converta o caminho em um caminho de clipe.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="cb4cf-136">Converta o caminho em uma região.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="cb4cf-137">Nivelar o caminho convertendo cada curva no caminho em uma série de segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="cb4cf-138">Recupere as coordenadas das linhas e das curvas que compõem um caminho.</span><span class="sxs-lookup"><span data-stu-id="cb4cf-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



