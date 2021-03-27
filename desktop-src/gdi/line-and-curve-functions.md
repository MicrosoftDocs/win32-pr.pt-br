---
description: As funções a seguir são usadas com linhas e curvas.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Funções de linha e curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988799"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="cbd0b-103">Funções de linha e curva</span><span class="sxs-lookup"><span data-stu-id="cbd0b-103">Line and Curve Functions</span></span>

<span data-ttu-id="cbd0b-104">As funções a seguir são usadas com linhas e curvas.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="cbd0b-105">Função</span><span class="sxs-lookup"><span data-stu-id="cbd0b-105">Function</span></span>                                   | <span data-ttu-id="cbd0b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbd0b-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbd0b-107">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="cbd0b-108">Desenha um segmento de linha e um arco.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="cbd0b-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="cbd0b-110">Desenha um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="cbd0b-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="cbd0b-112">Desenha um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="cbd0b-113">**GetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="cbd0b-114">Recupera a direção do arco atual para o contexto do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="cbd0b-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="cbd0b-116">Determina quais pixels devem ser realçados para uma linha definida pelos pontos inicial e final especificados.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="cbd0b-117">**LineDDAProc**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="cbd0b-118">Uma função de retorno de chamada definida pelo aplicativo usada com a função LineDDA.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="cbd0b-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="cbd0b-120">Desenha uma linha da posição atual até, mas não incluindo, o ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="cbd0b-121">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="cbd0b-122">Atualiza a posição atual para o ponto especificado e, opcionalmente, retorna a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="cbd0b-123">**PolyBezierSegment**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="cbd0b-124">Desenha uma ou mais curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="cbd0b-125">**Polibézierto**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="cbd0b-126">Desenha uma ou mais curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="cbd0b-127">**Metaempate**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="cbd0b-128">Desenha um conjunto de segmentos de linha e curvas Bézier.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="cbd0b-129">**Múltipla**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="cbd0b-130">Desenha uma série de segmentos de linha conectando os pontos na matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="cbd0b-131">**Polilineto**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="cbd0b-132">Desenha uma ou mais linhas retas.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="cbd0b-133">**Polyline**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="cbd0b-134">Desenha várias séries de segmentos de linha conectados.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="cbd0b-135">**SetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="cbd0b-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="cbd0b-136">Define a direção do desenho a ser usada para as funções Arc e Rectangle.</span><span class="sxs-lookup"><span data-stu-id="cbd0b-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



