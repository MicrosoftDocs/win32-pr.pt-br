---
title: Eventos do Windows
description: Normalmente, os eventos são usados para solucionar problemas de software de aplicativo e de driver. Antes do Windows Vista, você usaria o ETW (rastreamento de eventos para Windows) ou o log de eventos para registrar eventos. O Windows Vista introduziu um novo modelo de eventos que unificava o ETW (rastreamento de eventos para Windows) e a API do log de eventos do Windows. O Windows 10 apresenta o TraceLogging, que se baseia no ETW e fornece uma maneira simplificada de instrumentar o código para desenvolvedores nativos, .NET e WinRT.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3d22580c38e45d06f5362e99626642eebdfe20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007497"
---
# <a name="windows-events"></a>Eventos do Windows

Normalmente, os eventos são usados para solucionar problemas de software de aplicativo e de driver.

-   Antes do Windows Vista, você usaria o ETW ( [rastreamento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) ) ou o [log de eventos](/windows/desktop/EventLog/event-logging) para registrar eventos.
-   O Windows Vista introduziu um novo modelo de eventos que unificava o ETW ( [rastreamento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) ) e a API do [log de eventos do Windows](/windows/desktop/WES/windows-event-log) .
-   O Windows 10 apresenta o [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) , que se baseia no ETW e fornece uma maneira simplificada de instrumentar o código para desenvolvedores nativos, .net e WinRT.

O novo modelo [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.

O modelo do Windows Vista usa um manifesto XML para definir os eventos que você deseja publicar. Os eventos podem ser publicados em um canal ou em uma sessão do ETW. Você pode publicar os eventos nos seguintes tipos de canais: admin, operacional, analítica e depuração. Se você usar apenas o ETW para habilitar o Publicador, não será necessário especificar canais em seu manifesto. Para obter detalhes completos sobre como escrever um manifesto, consulte [escrevendo um manifesto de instrumentação](/windows/desktop/WES/writing-an-instrumentation-manifest)e para obter informações sobre canais, consulte [definindo canais](/windows/desktop/WES/defining-channels).

Para registrar seu editor de eventos e publicar eventos, use a API do ETW. Para obter detalhes, consulte [fornecendo eventos](/windows/desktop/ETW/providing-events) e [desenvolvendo um provedor](/windows/desktop/WES/developing-a-provider). O editor de eventos gravará automaticamente os eventos nos canais especificados no manifesto, se eles estiverem habilitados.

Se você quiser controlar os eventos que um editor de eventos publica em um nível mais preciso de granularidade, use a API do ETW. Por exemplo, se o manifesto definir eventos de gravação e leitura, você poderá habilitar apenas os eventos de gravação. Um evento também pode especificar um valor de nível, como aviso ou erro, para que você possa limitar os eventos que são gravados naqueles que especificam o nível de erro. Para obter detalhes, consulte [controlando sessões de rastreamento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions). Os eventos são gravados no arquivo de log da sessão.

O consumo de eventos envolve a recuperação de eventos de um canal de eventos, um arquivo de log de eventos (arquivos. evtx ou. evt), um arquivo de rastreamento (arquivos. ETL) ou uma sessão ETW em tempo real. Para consumir eventos de um arquivo de rastreamento ETW ou de uma sessão ETW em tempo real, use as funções auxiliares de dados de rastreamento (TDH) no ETW para consumir os eventos. Você também pode usar TDH para ler os metadados do evento. Para obter detalhes, consulte [consumindo eventos](/windows/desktop/ETW/consuming-events). Para consumir eventos de um canal de eventos ou de um arquivo de log de eventos, use as funções de log de eventos do Windows para consultar ou assinar eventos. Para obter mais informações, consulte [consultando eventos](/windows/desktop/WES/querying-for-events) ou [assinando eventos](/windows/desktop/WES/subscribing-to-events).

Antes do Windows Vista, você deve usar o [rastreamento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) ou [log de eventos](/windows/desktop/EventLog/event-logging) para publicar e consumir eventos.

 

 