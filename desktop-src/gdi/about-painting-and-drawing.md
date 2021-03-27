---
description: Quase todos os aplicativos usam a tela para exibir os dados que manipulam.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Sobre pintura e desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988778"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="60082-103">Sobre pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="60082-103">About Painting and Drawing</span></span>

<span data-ttu-id="60082-104">Quase todos os aplicativos usam a tela para exibir os dados que manipulam.</span><span class="sxs-lookup"><span data-stu-id="60082-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="60082-105">Um aplicativo pinta imagens, desenha figuras e grava o texto para que o usuário possa exibir os dados conforme eles são criados, editados e impressos.</span><span class="sxs-lookup"><span data-stu-id="60082-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="60082-106">O Microsoft Windows fornece suporte avançado para pintura e desenho, mas, devido à natureza dos sistemas operacionais multitarefas, os aplicativos devem cooperar uns com os outros ao acessar a tela.</span><span class="sxs-lookup"><span data-stu-id="60082-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="60082-107">Para manter todos os aplicativos funcionando de forma tranqüila e cooperativa, o sistema gerencia toda a saída para a tela.</span><span class="sxs-lookup"><span data-stu-id="60082-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="60082-108">Os aplicativos usam o Windows como seu dispositivo de saída primário, em vez da própria tela.</span><span class="sxs-lookup"><span data-stu-id="60082-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="60082-109">O sistema fornece contextos de dispositivo que correspondem exclusivamente às janelas.</span><span class="sxs-lookup"><span data-stu-id="60082-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="60082-110">Os aplicativos usam contextos de dispositivo de exibição para direcionar sua saída para o Windows especificado.</span><span class="sxs-lookup"><span data-stu-id="60082-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="60082-111">O desenho em uma janela (direcionamento de saída para ela) impede que um aplicativo interfira na saída de outros aplicativos e permite que os aplicativos coexistam uns com os outros, ao mesmo tempo em que aproveitam ao máximo os recursos gráficos do sistema.</span><span class="sxs-lookup"><span data-stu-id="60082-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="60082-112">Quando desenhar em uma janela</span><span class="sxs-lookup"><span data-stu-id="60082-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="60082-113">A mensagem do WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="60082-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="60082-114">Desenho sem a mensagem de pintura do WM \_</span><span class="sxs-lookup"><span data-stu-id="60082-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="60082-115">Sistema de coordenadas da janela</span><span class="sxs-lookup"><span data-stu-id="60082-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="60082-116">Regiões da janela</span><span class="sxs-lookup"><span data-stu-id="60082-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="60082-117">Plano de fundo da janela</span><span class="sxs-lookup"><span data-stu-id="60082-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="60082-118">Janelas minimizadas</span><span class="sxs-lookup"><span data-stu-id="60082-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="60082-119">Janelas redimensionadas</span><span class="sxs-lookup"><span data-stu-id="60082-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="60082-120">Área não cliente</span><span class="sxs-lookup"><span data-stu-id="60082-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="60082-121">Região de atualização da janela filho</span><span class="sxs-lookup"><span data-stu-id="60082-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="60082-122">Dispositivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="60082-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="60082-123">Bloqueio de atualização de janela</span><span class="sxs-lookup"><span data-stu-id="60082-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="60082-124">Retângulo delimitador acumulado</span><span class="sxs-lookup"><span data-stu-id="60082-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



