---
description: Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recuperando um retângulo delimitador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661583"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="4ce22-103">Recuperando um retângulo delimitador</span><span class="sxs-lookup"><span data-stu-id="4ce22-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="4ce22-104">Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) .</span><span class="sxs-lookup"><span data-stu-id="4ce22-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="4ce22-105">Se a região for retangular, **GetRgnBox** retornará as dimensões da região.</span><span class="sxs-lookup"><span data-stu-id="4ce22-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="4ce22-106">Se a região for elíptica, a função retornará as dimensões do menor retângulo que pode ser desenhada ao redor da elipse.</span><span class="sxs-lookup"><span data-stu-id="4ce22-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="4ce22-107">Os lados longos do retângulo têm o mesmo comprimento que o eixo principal da elipse, e os lados curtos do retângulo têm o mesmo comprimento que o eixo secundário da elipse.</span><span class="sxs-lookup"><span data-stu-id="4ce22-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="4ce22-108">Se a região for Polygon, **GetRgnBox** retornará as dimensões do menor retângulo que pode ser desenhado em todo o polígono.</span><span class="sxs-lookup"><span data-stu-id="4ce22-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 



