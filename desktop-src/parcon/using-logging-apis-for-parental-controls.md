---
description: Usando APIs de log para controles dos pais
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Usando APIs de log para controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828614"
---
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="08101-103">Usando APIs de log para controles dos pais</span><span class="sxs-lookup"><span data-stu-id="08101-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="08101-104">Relatório de atividades (registro em log)</span><span class="sxs-lookup"><span data-stu-id="08101-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="08101-105">O arquivo de cabeçalho WpcEvent. h contém definições dos campos para cada tipo de evento de atividade predefinido e o tipo personalizado.</span><span class="sxs-lookup"><span data-stu-id="08101-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="08101-106">Este código de exemplo mostra as etapas para registrar um evento de convite de conversa de mensagens instantâneas usando a API de publicação do ETW:</span><span class="sxs-lookup"><span data-stu-id="08101-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a><span data-ttu-id="08101-107">Registro em log personalizado</span><span class="sxs-lookup"><span data-stu-id="08101-107">Custom Logging</span></span>

<span data-ttu-id="08101-108">Para que um aplicativo estenda os eventos registrados fora do conjunto de eventos predefinidos ou um tipo personalizado, será necessário definir um provedor para isso no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08101-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="08101-109">O canal padrão WPC pode ser importado e os eventos definidos pelo aplicativo podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="08101-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="08101-110">Direitos de registro em log</span><span class="sxs-lookup"><span data-stu-id="08101-110">Logging Rights</span></span>

<span data-ttu-id="08101-111">O canal de log WPC é controlado pela ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) para fornecer acesso completo apenas para administradores.</span><span class="sxs-lookup"><span data-stu-id="08101-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="08101-112">Contas que não são de administrador podem gravar no canal, mas não têm acesso de leitura ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="08101-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="08101-113">O acesso ao canal é usando a API do ETW.</span><span class="sxs-lookup"><span data-stu-id="08101-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="08101-114">Detalhes do provedor de log de controles dos pais</span><span class="sxs-lookup"><span data-stu-id="08101-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="08101-115">O provedor WPC é chamado de Microsoft.com/Windows/ParentalControls com GUID {01090065-B467-4503-9B28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="08101-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="08101-116">O canal de log local padrão é Microsoft.com/Windows/ParentalControls/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="08101-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="08101-117">Os arquivos de log são armazenados na \\ pasta Windows system32 \\ WPC \\ logs.</span><span class="sxs-lookup"><span data-stu-id="08101-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="08101-118">Notificação de logoff de limites de tempo iminente</span><span class="sxs-lookup"><span data-stu-id="08101-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="08101-119">O sistema de controles dos pais acionará um evento de aviso em 15 minutos e novamente em 1 minuto antes do logoff de um usuário controlado com base nas restrições de tempo.</span><span class="sxs-lookup"><span data-stu-id="08101-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="08101-120">Os aplicativos podem assinar esses eventos, especialmente quando estão sendo executados no modo de tela inteira do DirectX, em que as notificações padrão do Windows não são exibidas.</span><span class="sxs-lookup"><span data-stu-id="08101-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="08101-121">É fornecido um código de exemplo que mostra como assinar os eventos, registrar uma função de retorno de chamada e receber os eventos.</span><span class="sxs-lookup"><span data-stu-id="08101-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08101-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08101-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08101-123">Visão geral dos recursos de extensibilidade dos controles dos pais</span><span class="sxs-lookup"><span data-stu-id="08101-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="08101-124">**\_descritor de dados de evento \_**</span><span class="sxs-lookup"><span data-stu-id="08101-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="08101-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="08101-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="08101-126">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="08101-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
