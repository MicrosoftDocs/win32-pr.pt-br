---
description: A função SetRect cria um retângulo, a função CopyRect faz uma cópia de um determinado retângulo, e a função SetRectEmpty cria um retângulo vazio.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operações de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296577"
---
# <a name="rectangle-operations"></a><span data-ttu-id="46669-103">Operações de retângulo</span><span class="sxs-lookup"><span data-stu-id="46669-103">Rectangle Operations</span></span>

<span data-ttu-id="46669-104">A função [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) cria um retângulo, a função [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) faz uma cópia de um determinado retângulo, e a função [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) cria um retângulo vazio.</span><span class="sxs-lookup"><span data-stu-id="46669-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="46669-105">Um retângulo vazio é qualquer retângulo com largura zero, altura zero ou ambos.</span><span class="sxs-lookup"><span data-stu-id="46669-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="46669-106">A função [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se um determinado retângulo está vazio.</span><span class="sxs-lookup"><span data-stu-id="46669-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="46669-107">A função [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se dois retângulos são idênticos ou seja, se eles têm as mesmas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="46669-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="46669-108">A função [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta ou diminui a largura ou altura de um retângulo, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="46669-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="46669-109">Ele pode adicionar ou remover largura de ambas as extremidades do retângulo; Ele pode adicionar ou remover altura das partes superior e inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="46669-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="46669-110">A função [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) move um retângulo por um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="46669-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="46669-111">Ele move o retângulo adicionando o valor x, o valor y ou os valores x e y determinados às coordenadas de canto.</span><span class="sxs-lookup"><span data-stu-id="46669-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="46669-112">A função [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se um determinado ponto está dentro de um determinado retângulo.</span><span class="sxs-lookup"><span data-stu-id="46669-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="46669-113">O ponto estará no retângulo se ele estiver no lado esquerdo ou superior ou estiver completamente dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="46669-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="46669-114">O ponto não estará no retângulo se ele estiver no lado direito ou inferior.</span><span class="sxs-lookup"><span data-stu-id="46669-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="46669-115">A função [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) cria um novo retângulo que é a interseção de dois retângulos existentes, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="46669-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="46669-116">ilustração mostrando dois retângulos sobrepostos, com sombreamento mais escuro para indicar a interseção</span><span class="sxs-lookup"><span data-stu-id="46669-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="46669-117">A função [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) cria um novo retângulo que é a União de dois retângulos existentes, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="46669-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![ilustração de dois retângulos sobrepostos, com sombreamento mais escuro indicando áreas dentro da União, mas não dentro de um retângulo](images/csrec-02.png)

<span data-ttu-id="46669-119">Para obter informações sobre as funções que desenham reticências e polígonos, confira [formas preenchidas](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="46669-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



