---
description: Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função. Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linhas e curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967696"
---
# <a name="combined-lines-and-curves"></a><span data-ttu-id="07ebd-104">Linhas e curvas combinadas</span><span class="sxs-lookup"><span data-stu-id="07ebd-104">Combined Lines and Curves</span></span>

<span data-ttu-id="07ebd-105">Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função.</span><span class="sxs-lookup"><span data-stu-id="07ebd-105">In addition to drawing lines or curves, applications can draw combinations of line and curve output by calling a single function.</span></span> <span data-ttu-id="07ebd-106">Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .</span><span class="sxs-lookup"><span data-stu-id="07ebd-106">For example, an application can draw the outline of a pie chart by calling the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span>

<span data-ttu-id="07ebd-107">A função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) desenha um arco ao longo do perímetro de um círculo e desenha uma linha conectando o ponto inicial do arco ao centro do círculo.</span><span class="sxs-lookup"><span data-stu-id="07ebd-107">The [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function draws an arc along a circle's perimeter and draws a line connecting the starting point of the arc to the circle's center.</span></span> <span data-ttu-id="07ebd-108">Além de usar a função **AngleArc** , um aplicativo também pode combinar a saída de linha e de curva irregular usando a função do [**polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .</span><span class="sxs-lookup"><span data-stu-id="07ebd-108">In addition to using the **AngleArc** function, an application can also combine line and irregular curve output by using the [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) function.</span></span>

 

 



