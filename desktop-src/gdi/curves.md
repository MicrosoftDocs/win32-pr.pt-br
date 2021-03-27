---
description: Uma curva regular é um conjunto de pixels realçados em uma exibição de varredura (ou pontos em uma página impressa) que definem o perímetro (ou parte do perímetro) de uma seção de cone.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827666"
---
# <a name="curves"></a><span data-ttu-id="a866f-103">Curvas</span><span class="sxs-lookup"><span data-stu-id="a866f-103">Curves</span></span>

<span data-ttu-id="a866f-104">Uma curva regular é um conjunto de pixels realçados em uma exibição de varredura (ou pontos em uma página impressa) que definem o perímetro (ou parte do perímetro) de uma seção de cone.</span><span class="sxs-lookup"><span data-stu-id="a866f-104">A regular curve is a set of highlighted pixels on a raster display (or dots on a printed page) that define the perimeter (or part of the perimeter) of a conic section.</span></span> <span data-ttu-id="a866f-105">Uma curva irregular é um conjunto de pixels que definem uma curva que não se ajusta ao perímetro de uma seção de cone.</span><span class="sxs-lookup"><span data-stu-id="a866f-105">An irregular curve is a set of pixels that define a curve that does not fit the perimeter of a conic section.</span></span> <span data-ttu-id="a866f-106">O ponto final é excluído de uma curva assim como é excluído de uma linha.</span><span class="sxs-lookup"><span data-stu-id="a866f-106">The ending point is excluded from a curve just as it is excluded from a line.</span></span>

<span data-ttu-id="a866f-107">Quando um aplicativo chama uma das funções de desenho de curva, o GDI quebra a curva em um número de segmentos de linha discretos extremamente pequenos.</span><span class="sxs-lookup"><span data-stu-id="a866f-107">When an application calls one of the curve-drawing functions, GDI breaks the curve into a number of extremely small, discrete line segments.</span></span> <span data-ttu-id="a866f-108">Depois de determinar os pontos de extremidade (ponto inicial e ponto final) para cada um desses segmentos de linha, o GDI determina quais pixels (ou pontos) definem cada linha aplicando seu DDA.</span><span class="sxs-lookup"><span data-stu-id="a866f-108">After determining the endpoints (starting point and ending point) for each of these line segments, GDI determines which pixels (or dots) define each line by applying its DDA.</span></span>

<span data-ttu-id="a866f-109">Um aplicativo pode desenhar uma elipse ou parte de uma elipse chamando a função [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) .</span><span class="sxs-lookup"><span data-stu-id="a866f-109">An application can draw an ellipse or part of an ellipse by calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function.</span></span> <span data-ttu-id="a866f-110">Essa função desenha a curva dentro do perímetro de um retângulo invisível chamado de um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="a866f-110">This function draws the curve within the perimeter of an invisible rectangle called a bounding rectangle.</span></span> <span data-ttu-id="a866f-111">O tamanho da elipse é especificado por dois radiais invisíveis que se estendem do centro do retângulo até os lados do retângulo.</span><span class="sxs-lookup"><span data-stu-id="a866f-111">The size of the ellipse is specified by two invisible radials extending from the center of the rectangle to the sides of the rectangle.</span></span> <span data-ttu-id="a866f-112">A ilustração a seguir mostra um arco (parte de uma elipse) desenhado usando a função **Arc** .</span><span class="sxs-lookup"><span data-stu-id="a866f-112">The following illustration shows an arc (part of an ellipse) drawn by using the **Arc** function.</span></span>

![diagrama mostrando um arco que representa três trimestres de um círculo completo](images/cslcv-03.png)

<span data-ttu-id="a866f-114">Ao chamar a função [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) , um aplicativo especifica as coordenadas do retângulo delimitador e radials.</span><span class="sxs-lookup"><span data-stu-id="a866f-114">When calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function, an application specifies the coordinates of the bounding rectangle and radials.</span></span> <span data-ttu-id="a866f-115">A ilustração anterior mostra o retângulo e as radials com linhas tracejadas enquanto o arco real foi desenhado usando uma linha sólida.</span><span class="sxs-lookup"><span data-stu-id="a866f-115">The preceding illustration shows the rectangle and radials with dashed lines while the actual arc was drawn using a solid line.</span></span>

<span data-ttu-id="a866f-116">Ao desenhar o arco de outro objeto, o aplicativo pode chamar as funções [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) e [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) para controlar a direção (no sentido horário ou anti-horário) na qual o objeto é desenhado.</span><span class="sxs-lookup"><span data-stu-id="a866f-116">When drawing the arc of another object, the application can call the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) and [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) functions to control the direction (clockwise or counterclockwise) in which the object is drawn.</span></span> <span data-ttu-id="a866f-117">A direção padrão para desenhar arcos e outros objetos é no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="a866f-117">The default direction for drawing arcs and other objects is counterclockwise.</span></span>

<span data-ttu-id="a866f-118">Além de desenhar elipses ou partes de elipses, os aplicativos podem desenhar curvas irregulares chamadas curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="a866f-118">In addition to drawing ellipses or parts of ellipses, applications can draw irregular curves called Bézier curves.</span></span> <span data-ttu-id="a866f-119">Uma *curva de Bézier* é uma curva irregular cuja curvatura é definida por quatro pontos de controle (P1, P2, P3 e P4).</span><span class="sxs-lookup"><span data-stu-id="a866f-119">A *Bézier curve* is an irregular curve whose curvature is defined by four control points (p1, p2, p3, and p4).</span></span> <span data-ttu-id="a866f-120">Os pontos de controle P1 e P4 definem os pontos inicial e final da curva, e os pontos de controle P2 e P3 definem a forma da curva por pontos de marcação em que a curva inverte a orientação, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a866f-120">The control points p1 and p4 define the starting and ending points of the curve, and the control points p2 and p3 define the shape of the curve by marking points where the curve reverses orientation, as shown in the following diagram.</span></span>

![ilustração mostrando duas curvas de Bézier, cada uma entre um ponto inicial e um final e cada uma com dois pontos de controle](images/cslcv-04.png)

<span data-ttu-id="a866f-122">Um aplicativo pode desenhar curvas irregulares chamando a função de [**telebezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) , fornecendo os pontos de controle apropriados.</span><span class="sxs-lookup"><span data-stu-id="a866f-122">An application can draw irregular curves by calling the [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) function, supplying the appropriate control points.</span></span>

 

 



