---
description: 'Um B&\# 233; zier spline é uma curva especificada por quatro pontos: dois pontos de extremidade (P1 e P2) e dois pontos de controle (C1 e C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Linhas de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091489"
---
# <a name="bezier-splines"></a><span data-ttu-id="38826-103">Linhas de Bézier</span><span class="sxs-lookup"><span data-stu-id="38826-103">Bezier Splines</span></span>

<span data-ttu-id="38826-104">Uma spline de Bézier é uma curva especificada por quatro pontos: dois pontos de extremidade (p1 e p2) e dois pontos de controle (c1 e c2).</span><span class="sxs-lookup"><span data-stu-id="38826-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="38826-105">A curva começa em p1 e termina em p2.</span><span class="sxs-lookup"><span data-stu-id="38826-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="38826-106">A curva não passa pelos pontos de controle, mas os pontos de controle atuam como ímãs, puxando a curva em determinadas direções e influenciando a forma como a curva dobra.</span><span class="sxs-lookup"><span data-stu-id="38826-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="38826-107">A ilustração a seguir mostra uma curva de Bézier junto com seus pontos de extremidade e de controle.</span><span class="sxs-lookup"><span data-stu-id="38826-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![ilustração mostrando um spline de Bézier com dois pontos de extremidade e dois pontos de controle](images/aboutgdip02-art11a.png)

<span data-ttu-id="38826-109">Observe que a curva começa em P1 e se move para o ponto de controle C1.</span><span class="sxs-lookup"><span data-stu-id="38826-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="38826-110">A linha tangente da curva em p1 é a linha desenhada de p1 a c1.</span><span class="sxs-lookup"><span data-stu-id="38826-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="38826-111">Observe também que a linha tangente no ponto de extremidade P2 é a linha desenhada de C2 para P2.</span><span class="sxs-lookup"><span data-stu-id="38826-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="38826-112">Para desenhar um spline Bézier, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="38826-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="38826-113">O objeto **Graphics** fornece o método [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e o objeto **Pen** armazena os atributos da curva, como largura e cor da linha.</span><span class="sxs-lookup"><span data-stu-id="38826-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="38826-114">O endereço do objeto **Pen** é passado como um dos argumentos para o método DrawBezier.</span><span class="sxs-lookup"><span data-stu-id="38826-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="38826-115">Os argumentos restantes passados para o método DrawBezier são os pontos de extremidade e de controle.</span><span class="sxs-lookup"><span data-stu-id="38826-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="38826-116">O exemplo a seguir desenha um spline Bézier com ponto inicial (0, 0), pontos de controle (40, 20) e (80, 150) e ponto final (100, 10).</span><span class="sxs-lookup"><span data-stu-id="38826-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="38826-117">A ilustração a seguir mostra a curva, os pontos de controle e duas linhas tangentes.</span><span class="sxs-lookup"><span data-stu-id="38826-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![ilustração mostrando um spline de Bézier com dois pontos de extremidade, dois pontos de controle e duas linhas tangentes](images/aboutgdip02-art12.png)

<span data-ttu-id="38826-119">As splines de Bézier foram desenvolvidos originalmente por Pierre Bézier para projetos da indústria automotiva.</span><span class="sxs-lookup"><span data-stu-id="38826-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="38826-120">Desde que eles tenham sido comprovadamente muito úteis em muitos tipos de design auxiliado por computador e também são usados para definir os contornos das fontes.</span><span class="sxs-lookup"><span data-stu-id="38826-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="38826-121">Splines de Bézier podem gerar uma grande variedade de formas, algumas das quais são mostradas na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="38826-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![ilustração mostrando três linhas de Bézier](images/aboutgdip02-art13.png)

 

 



