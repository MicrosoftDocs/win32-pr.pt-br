---
description: Usando APIs de log para controles dos pais
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Usando APIs de log para controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 571a24f8bdbf687f8c1975cfc29057035ac56747edc0459682512531194c55a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869058"
---
# <a name="using-logging-apis-for-parental-controls"></a>Usando APIs de log para controles dos pais

### <a name="activity-reporting-logging"></a>Relatório de atividades (registro em log)

O arquivo de cabeçalho WpcEvent. h contém definições dos campos para cada tipo de evento de atividade predefinido e o tipo personalizado. Este código de exemplo mostra as etapas para registrar um evento de convite de conversa de mensagens instantâneas usando a API de publicação do ETW:


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



### <a name="custom-logging"></a>Registro em log personalizado

Para que um aplicativo estenda os eventos registrados fora do conjunto de eventos predefinidos ou um tipo personalizado, será necessário definir um provedor para isso no manifesto do aplicativo. O canal padrão WPC pode ser importado e os eventos definidos pelo aplicativo podem ser registrados.

### <a name="logging-rights"></a>Direitos de registro em log

O canal de log WPC é controlado pela ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) para fornecer acesso completo apenas para administradores. Contas que não são de administrador podem gravar no canal, mas não têm acesso de leitura ou exclusão. O acesso ao canal é usando a API do ETW.

### <a name="parental-controls-logging-provider-details"></a>Detalhes do provedor de log de controles dos pais

o provedor WPC é denominado Microsoft.com/Windows/ParentalControls com GUID {01090065-B467-4503-9B28-533766761087}. o canal de log local padrão é Microsoft.com/Windows/ParentalControls/LocalEvents.

os arquivos de Log são armazenados na \\ pasta de Logs do Windows System32 \\ Wpc \\ .

### <a name="notification-of-impending-time-limits-logout"></a>Notificação de logoff de limites de tempo iminente

O sistema de controles dos pais acionará um evento de aviso em 15 minutos e novamente em 1 minuto antes do logoff de um usuário controlado com base nas restrições de tempo. os aplicativos podem assinar esses eventos, especialmente quando estão sendo executados no modo de tela inteira do DirectX, em que as notificações padrão de Windows não são exibidas. É fornecido um código de exemplo que mostra como assinar os eventos, registrar uma função de retorno de chamada e receber os eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos recursos de extensibilidade dos controles dos pais](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**\_descritor de dados de evento \_**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
