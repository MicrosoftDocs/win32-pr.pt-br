---
description: As dimensões de uma caneta geométrica são especificadas em unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Canetas geométricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988812"
---
# <a name="geometric-pens"></a><span data-ttu-id="5dbeb-103">Canetas geométricas</span><span class="sxs-lookup"><span data-stu-id="5dbeb-103">Geometric Pens</span></span>

<span data-ttu-id="5dbeb-104">As dimensões de uma caneta geométrica são especificadas em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="5dbeb-105">Portanto, as linhas desenhadas com uma caneta geométrica podem ser escaladas ou seja, elas podem parecer mais largas ou estreitas, dependendo da transformação do mundo atual.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="5dbeb-106">Para obter mais informações sobre a transformação do mundo, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="5dbeb-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="5dbeb-107">Além dos três atributos compartilhados com canetas superficiais (largura, estilo e cor), as canetas geométricas possuem os quatro atributos a seguir: padrão, hachura opcional, estilo final e estilo de junção.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="5dbeb-108">Para obter mais informações sobre esses atributos, consulte [atributos de caneta](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5dbeb-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="5dbeb-109">Para criar uma caneta geométrica, um aplicativo usa a função [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="5dbeb-110">Assim como nas canetas superficiais, a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleciona uma caneta geométrica no controlador de domínio do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



