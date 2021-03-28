---
description: Você pode desenhar o início ou o final de uma linha em uma das várias formas chamadas line Caps. O Windows GDI+ dá suporte a várias arremates de linha, como round, quadrado, losango e ponta de seta.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Desenhando uma linha com limites de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988244"
---
# <a name="drawing-a-line-with-line-caps"></a><span data-ttu-id="493bd-104">Desenhando uma linha com limites de linha</span><span class="sxs-lookup"><span data-stu-id="493bd-104">Drawing a Line with Line Caps</span></span>

<span data-ttu-id="493bd-105">Você pode desenhar o início ou o final de uma linha em uma das várias formas chamadas line Caps.</span><span class="sxs-lookup"><span data-stu-id="493bd-105">You can draw the start or end of a line in one of several shapes called line caps.</span></span> <span data-ttu-id="493bd-106">O Windows GDI+ dá suporte a várias arremates de linha, como round, quadrado, losango e ponta de seta.</span><span class="sxs-lookup"><span data-stu-id="493bd-106">Windows GDI+ supports several line caps, such as round, square, diamond, and arrowhead.</span></span>

<span data-ttu-id="493bd-107">Você pode especificar limites de linha para o início de uma linha (Cap inicial), o fim de uma linha (extremidade final) ou os traços de uma linha tracejada (limite de traço).</span><span class="sxs-lookup"><span data-stu-id="493bd-107">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>

<span data-ttu-id="493bd-108">O exemplo a seguir desenha uma linha com uma ponta de seta em uma extremidade e um limite de arredondamento na outra extremidade:</span><span class="sxs-lookup"><span data-stu-id="493bd-108">The following example draws a line with an arrowhead at one end and a round cap at the other end:</span></span>


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



<span data-ttu-id="493bd-109">A ilustração a seguir mostra a linha resultante.</span><span class="sxs-lookup"><span data-stu-id="493bd-109">The following illustration shows the resulting line.</span></span>

![ilustração mostrando uma linha horizontal com uma seta na extremidade esquerda e um círculo na extremidade direita](images/pens4.png)

<span data-ttu-id="493bd-111">**LineCapArrowAnchor** e **LineCapRoundAnchor** são elementos da enumeração [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .</span><span class="sxs-lookup"><span data-stu-id="493bd-111">**LineCapArrowAnchor** and **LineCapRoundAnchor** are elements of the [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) enumeration.</span></span>

 

 



