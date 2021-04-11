---
description: Os aplicativos podem adaptar melhor seu comportamento ao estado de energia atual do computador Registrando-se para eventos de energia.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrando para eventos de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169511"
---
# <a name="registering-for-power-events"></a><span data-ttu-id="2e002-103">Registrando para eventos de energia</span><span class="sxs-lookup"><span data-stu-id="2e002-103">Registering for Power Events</span></span>

<span data-ttu-id="2e002-104">Os aplicativos podem adaptar melhor seu comportamento ao estado de energia atual do computador Registrando-se para eventos de energia.</span><span class="sxs-lookup"><span data-stu-id="2e002-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="2e002-105">Um aplicativo deve se registrar para cada evento de alteração de energia que possa afetar seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="2e002-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="2e002-106">Um aplicativo ou serviço usa a função [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) para se registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="2e002-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="2e002-107">Quando a configuração de energia correspondente é alterada, o sistema envia notificações da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2e002-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="2e002-108">Um aplicativo recebe uma mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) com um *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) e um *lParam* que aponta para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="2e002-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="2e002-109">Um serviço recebe uma chamada para a função de retorno de chamada [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) que ele registrou chamando a função [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .</span><span class="sxs-lookup"><span data-stu-id="2e002-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="2e002-110">O parâmetro *lpEventData* enviado para a função de retorno de chamada *HandlerEx* aponta para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="2e002-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="2e002-111">Na estrutura [**de \_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , o membro **PowerSetting** contém o GUID que identifica a notificação e o membro de **dados** contém o novo valor da configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="2e002-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="2e002-112">Para obter uma lista de GUIDs de configuração de energia para notificações que são mais úteis para aplicativos, consulte [**GUIDs de configuração de energia**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="2e002-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
