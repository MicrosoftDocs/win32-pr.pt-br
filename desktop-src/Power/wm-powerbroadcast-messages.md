---
description: O sistema transmite uma mensagem para todos os aplicativos e drivers instaláveis sempre que ocorre um evento de gerenciamento de energia.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757747"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="149c8-103">\_Mensagens POWERBROADCAST do WM</span><span class="sxs-lookup"><span data-stu-id="149c8-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="149c8-104">O sistema transmite uma mensagem para todos os aplicativos e drivers instaláveis sempre que ocorre um evento de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="149c8-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="149c8-105">O sistema transmite esses eventos por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , definindo o parâmetro *wParam* como o evento de gerenciamento de energia apropriado.</span><span class="sxs-lookup"><span data-stu-id="149c8-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="149c8-106">Por exemplo, o evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica uma alteração no status de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="149c8-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="149c8-107">Você deve garantir que seu aplicativo responda corretamente à mensagem do **WM \_ POWERBROADCAST** .</span><span class="sxs-lookup"><span data-stu-id="149c8-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="149c8-108">O sistema transmite um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) imediatamente antes de suspender a operação.</span><span class="sxs-lookup"><span data-stu-id="149c8-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="149c8-109">Isso oferece aos aplicativos e drivers uma última chance de se preparar para o evento.</span><span class="sxs-lookup"><span data-stu-id="149c8-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="149c8-110">Em muitos casos, o sistema transmite essas mensagens sem solicitar permissão para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="149c8-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="149c8-111">Isso acontece, por exemplo, se um aplicativo força a suspensão com a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="149c8-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="149c8-112">O sistema transmite o evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) ou [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) quando a operação do sistema é restaurada.</span><span class="sxs-lookup"><span data-stu-id="149c8-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="149c8-113">Se um aplicativo recebeu um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de o computador ser suspenso, ele receberá o \_ evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="149c8-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="149c8-114">Caso contrário, ele receberá o \_ evento PBT APMRESUMECRITICAL.</span><span class="sxs-lookup"><span data-stu-id="149c8-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="149c8-115">O sistema envia um evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) para aplicativos que se registraram para o evento específico usando [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span><span class="sxs-lookup"><span data-stu-id="149c8-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="149c8-116">Para obter mais informações, consulte [registrando para eventos de energia](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="149c8-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="149c8-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="149c8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="149c8-118">Sobre o gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="149c8-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



