---
description: As funções a seguir fornecem suporte para vários monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Várias funções de monitores de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967646"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="e09bd-103">Várias funções de monitores de exibição</span><span class="sxs-lookup"><span data-stu-id="e09bd-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="e09bd-104">As funções a seguir fornecem suporte para vários monitores.</span><span class="sxs-lookup"><span data-stu-id="e09bd-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="e09bd-105">Função</span><span class="sxs-lookup"><span data-stu-id="e09bd-105">Function</span></span>                                           | <span data-ttu-id="e09bd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e09bd-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e09bd-107">**EnumDisplayMonitors**</span><span class="sxs-lookup"><span data-stu-id="e09bd-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="e09bd-108">Enumera os monitores de exibição que interseccionam uma região formada pela interseção de um retângulo de recorte especificado e a região visível de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e09bd-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="e09bd-109">**GetMonitorInfo**</span><span class="sxs-lookup"><span data-stu-id="e09bd-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="e09bd-110">Recupera informações sobre um monitor de exibição.</span><span class="sxs-lookup"><span data-stu-id="e09bd-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="e09bd-111">**MonitorEnumProc**</span><span class="sxs-lookup"><span data-stu-id="e09bd-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="e09bd-112">Uma função de retorno de chamada definida pelo aplicativo que é chamada pela função [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="e09bd-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="e09bd-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="e09bd-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="e09bd-114">Recupera um identificador para o monitor de exibição que contém um ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="e09bd-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="e09bd-115">**MonitorFromRect**</span><span class="sxs-lookup"><span data-stu-id="e09bd-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="e09bd-116">Recupera um identificador para o monitor de exibição que tem a maior área de interseção com um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="e09bd-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="e09bd-117">**MonitorFromWindow**</span><span class="sxs-lookup"><span data-stu-id="e09bd-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="e09bd-118">Recupera um identificador para o monitor de exibição que tem a maior área de interseção com o retângulo delimitador de uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="e09bd-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



