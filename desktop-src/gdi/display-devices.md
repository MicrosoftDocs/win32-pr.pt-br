---
description: Antes de pintar, o sistema deve preparar o dispositivo de vídeo para operações de desenho.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Dispositivos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967677"
---
# <a name="display-devices"></a><span data-ttu-id="42d45-103">Dispositivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="42d45-103">Display Devices</span></span>

<span data-ttu-id="42d45-104">Antes de pintar, o sistema deve preparar o dispositivo de vídeo para operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="42d45-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="42d45-105">Um contexto de dispositivo de vídeo define um conjunto de objetos gráficos e seus atributos associados e os modos gráficos que afetam a saída.</span><span class="sxs-lookup"><span data-stu-id="42d45-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="42d45-106">O sistema prepara cada contexto de dispositivo de vídeo para saída para uma janela, definindo os objetos de desenho, as cores e os modos para a janela em vez do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="42d45-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="42d45-107">Quando o aplicativo fornece o contexto do dispositivo de exibição por meio de chamadas para funções GDI, a GDI usa as informações no contexto para gerar a saída na janela especificada sem intrusão em outras janelas ou outras partes da tela.</span><span class="sxs-lookup"><span data-stu-id="42d45-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="42d45-108">O sistema fornece cinco tipos de contextos de dispositivo de exibição.</span><span class="sxs-lookup"><span data-stu-id="42d45-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="42d45-109">Type</span><span class="sxs-lookup"><span data-stu-id="42d45-109">Type</span></span>                                           | <span data-ttu-id="42d45-110">Significado</span><span class="sxs-lookup"><span data-stu-id="42d45-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42d45-111">Common</span><span class="sxs-lookup"><span data-stu-id="42d45-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="42d45-112">Permite desenhar na área do cliente de uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="42d45-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="42d45-113">class</span><span class="sxs-lookup"><span data-stu-id="42d45-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="42d45-114">Permite desenhar na área do cliente de uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="42d45-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="42d45-115">parent</span><span class="sxs-lookup"><span data-stu-id="42d45-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="42d45-116">Permite desenhar em qualquer lugar na janela.</span><span class="sxs-lookup"><span data-stu-id="42d45-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="42d45-117">Embora o contexto do dispositivo pai também permita o desenho na janela pai, ele não se destina a ser usado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="42d45-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="42d45-118">pessoal</span><span class="sxs-lookup"><span data-stu-id="42d45-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="42d45-119">Permite desenhar na área do cliente de uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="42d45-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="42d45-120">Window</span><span class="sxs-lookup"><span data-stu-id="42d45-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="42d45-121">Permite desenhar em qualquer lugar na janela.</span><span class="sxs-lookup"><span data-stu-id="42d45-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="42d45-122">O sistema fornece um contexto de dispositivo comum, classe, pai ou privado para uma janela com base no tipo de contexto de dispositivo de exibição especificado no estilo de classe dessa janela.</span><span class="sxs-lookup"><span data-stu-id="42d45-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="42d45-123">O sistema fornece um contexto de dispositivo de janela somente quando o aplicativo solicita explicitamente um, por exemplo, chamando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) .</span><span class="sxs-lookup"><span data-stu-id="42d45-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="42d45-124">Em todos os casos, um aplicativo pode usar a função [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) para determinar qual janela um DC de exibição atualmente representa.</span><span class="sxs-lookup"><span data-stu-id="42d45-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="42d45-125">Esta seção fornece informações sobre os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="42d45-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="42d45-126">Exibir cache de contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="42d45-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="42d45-127">Exibir padrões de contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="42d45-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="42d45-128">Contextos de dispositivo de exibição comuns</span><span class="sxs-lookup"><span data-stu-id="42d45-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="42d45-129">Contextos de dispositivo de exibição particular</span><span class="sxs-lookup"><span data-stu-id="42d45-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="42d45-130">Os contextos do dispositivo de exibição pai</span><span class="sxs-lookup"><span data-stu-id="42d45-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="42d45-131">A classe exibe contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="42d45-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="42d45-132">Janela exibir contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="42d45-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="42d45-133">Os contextos do dispositivo de exibição pai</span><span class="sxs-lookup"><span data-stu-id="42d45-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



