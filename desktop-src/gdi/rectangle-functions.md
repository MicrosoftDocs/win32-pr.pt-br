---
description: As funções a seguir são usadas com retângulos.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Funções de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165053"
---
# <a name="rectangle-functions"></a><span data-ttu-id="10ff6-103">Funções de retângulo</span><span class="sxs-lookup"><span data-stu-id="10ff6-103">Rectangle Functions</span></span>

<span data-ttu-id="10ff6-104">As funções a seguir são usadas com retângulos.</span><span class="sxs-lookup"><span data-stu-id="10ff6-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="10ff6-105">Função</span><span class="sxs-lookup"><span data-stu-id="10ff6-105">Function</span></span>                               | <span data-ttu-id="10ff6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="10ff6-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10ff6-107">**CopyRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="10ff6-108">Copia as coordenadas de um retângulo para outro.</span><span class="sxs-lookup"><span data-stu-id="10ff6-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="10ff6-109">**EqualRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="10ff6-110">Determina se os dois retângulos especificados são iguais, comparando as coordenadas dos cantos superior esquerdo e inferior direito.</span><span class="sxs-lookup"><span data-stu-id="10ff6-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="10ff6-111">**InflateRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="10ff6-112">Aumenta ou diminui a largura e a altura do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="10ff6-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="10ff6-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="10ff6-114">Calcula a interseção de dois retângulos de origem e coloca as coordenadas do retângulo de interseção no retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="10ff6-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="10ff6-115">**IsRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="10ff6-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="10ff6-116">Determina se o retângulo especificado está vazio.</span><span class="sxs-lookup"><span data-stu-id="10ff6-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="10ff6-117">**OffsetRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="10ff6-118">Move o retângulo especificado de acordo com os deslocamentos especificados.</span><span class="sxs-lookup"><span data-stu-id="10ff6-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="10ff6-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="10ff6-120">Determina se o ponto especificado está dentro do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="10ff6-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="10ff6-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="10ff6-122">Define as coordenadas do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="10ff6-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="10ff6-123">**SetRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="10ff6-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="10ff6-124">Cria um retângulo vazio no qual todas as coordenadas são definidas como zero.</span><span class="sxs-lookup"><span data-stu-id="10ff6-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="10ff6-125">**SubtractRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="10ff6-126">Determina as coordenadas de um retângulo formado por subtrair um retângulo de outro.</span><span class="sxs-lookup"><span data-stu-id="10ff6-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="10ff6-127">**UnionRect**</span><span class="sxs-lookup"><span data-stu-id="10ff6-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="10ff6-128">Cria a União de dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="10ff6-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



