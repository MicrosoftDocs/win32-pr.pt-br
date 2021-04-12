---
title: Fornecendo atualizações de status
description: Fornecendo atualizações de status
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Macro MCIWndSetActiveTimer
- Macro MCIWndSetInactiveTimer
- Macro MCIWndGetActiveTimer
- Macro MCIWndGetInactiveTimer
- Macro MCIWndSetTimers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363921"
---
# <a name="providing-status-updates"></a><span data-ttu-id="958d4-108">Fornecendo atualizações de status</span><span class="sxs-lookup"><span data-stu-id="958d4-108">Providing Status Updates</span></span>

<span data-ttu-id="958d4-109">O MCIWnd usa temporizadores para atualizar periodicamente as informações na barra de título da janela e na barra de rolagem e para enviar mensagens de notificação para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="958d4-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="958d4-110">Um temporizador controla o período de atualização da janela ativa do MCIWnd e um segundo temporizador controla o período de atualização para janelas do MCIWnd que estão inativas.</span><span class="sxs-lookup"><span data-stu-id="958d4-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="958d4-111">Seu aplicativo pode usar as macros do temporizador MCIWnd para recuperar as configurações do temporizador atual e ajustar os períodos de atualização.</span><span class="sxs-lookup"><span data-stu-id="958d4-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="958d4-112">Você pode definir o período de atualização usado pelo temporizador da janela ativa usando a macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="958d4-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="958d4-113">Essa macro define o período usado pelo MCIWnd para atualizar o TrackBar, para atualizar a posição de reprodução relatada na barra de título da janela e para notificar a janela pai de que a mídia foi alterada.</span><span class="sxs-lookup"><span data-stu-id="958d4-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="958d4-114">Você pode recuperar o período de atualização atual usado pelo temporizador da janela ativa usando a macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="958d4-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="958d4-115">O período de atualização padrão para o temporizador de janela ativa é de 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="958d4-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="958d4-116">Você pode definir o período de atualização usado pelo temporizador da janela inativa usando a macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="958d4-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="958d4-117">Essa macro define o período usado pelo MCIWnd para atualizar o TrackBar, para atualizar a posição de reprodução relatada na legenda da janela e para notificar a janela pai de que a mídia foi alterada.</span><span class="sxs-lookup"><span data-stu-id="958d4-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="958d4-118">Você pode recuperar o período de atualização atual usado pelo temporizador da janela inativa usando a macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="958d4-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="958d4-119">O período de atualização padrão para o temporizador de janela inativa é de 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="958d4-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="958d4-120">Seu aplicativo pode definir simultaneamente o período de atualização para ambos os temporizadores usando a macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="958d4-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="958d4-121">O armazenamento para o valor do período de atualização é limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="958d4-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="958d4-122">Se uma quantidade maior para o período de atualização for necessária, defina os temporizadores individualmente.</span><span class="sxs-lookup"><span data-stu-id="958d4-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




