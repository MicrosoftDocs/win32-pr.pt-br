---
description: Os registros de polilinha são uma série de pontos; as linhas desenhadas entre os pontos descrevem a estrutura de tópicos do caractere.
ms.assetid: 6f0de0bb-ad23-471f-9771-8f28614ee28d
title: Registros de polilinha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e9a9e87a730d06d15eae219f6f626f1d6d3848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165055"
---
# <a name="polyline-records"></a><span data-ttu-id="19895-103">Registros de polilinha</span><span class="sxs-lookup"><span data-stu-id="19895-103">Polyline Records</span></span>

<span data-ttu-id="19895-104">Os registros de [polilinha](/windows/desktop/api/Wingdi/nf-wingdi-polyline) são uma série de pontos; as linhas desenhadas entre os pontos descrevem a estrutura de tópicos do caractere.</span><span class="sxs-lookup"><span data-stu-id="19895-104">[Polyline](/windows/desktop/api/Wingdi/nf-wingdi-polyline) records are a series of points; lines drawn between the points describe the outline of the character.</span></span> <span data-ttu-id="19895-105">Um registro de polilinha começa com o último ponto no registro anterior (ou, para o primeiro registro na delimitação, o ponto de partida).</span><span class="sxs-lookup"><span data-stu-id="19895-105">A polyline record begins with the last point in the previous record (or, for the first record in the contour, the starting point).</span></span> <span data-ttu-id="19895-106">Cada ponto no registro está no contorno de glifo e pode ser conectado simplesmente usando linhas retas.</span><span class="sxs-lookup"><span data-stu-id="19895-106">Each point in the record is on the glyph outline and can be connected simply by using straight lines.</span></span>

 

 



