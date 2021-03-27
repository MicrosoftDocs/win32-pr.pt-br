---
description: Um aplicativo executa testes de clique em regiões para determinar as coordenadas da posição atual do cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiões de teste de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165074"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="963d8-103">Regiões de teste de clique</span><span class="sxs-lookup"><span data-stu-id="963d8-103">Hit Testing Regions</span></span>

<span data-ttu-id="963d8-104">Um aplicativo executa testes de clique em regiões para determinar as coordenadas da posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="963d8-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="963d8-105">Em seguida, ele passa essas coordenadas, bem como um identificador que identifica a região para a função [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .</span><span class="sxs-lookup"><span data-stu-id="963d8-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="963d8-106">As coordenadas do cursor podem ser recuperadas processando as várias mensagens do mouse, como o [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , o [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , o [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e o [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="963d8-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="963d8-107">O valor de retorno para PtInRegion indica se a posição do cursor está dentro da região especificada.</span><span class="sxs-lookup"><span data-stu-id="963d8-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
