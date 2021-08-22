---
description: Os consumidores de rastreamento de eventos podem processar eventos de um ou mais provedores.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Consumindo eventos (rastreamento de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42761bed132c5416a99888e067a1192571a527f39506e8964d5ea0209135b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269356"
---
# <a name="consuming-events-event-tracing"></a>Consumindo eventos (rastreamento de eventos)

Os consumidores de rastreamento de eventos podem processar eventos de um ou mais provedores. Os consumidores podem processar eventos de um arquivo de log ou em tempo real. Você só poderá consumir eventos em tempo real se o controlador especificar o modo de registro em log em tempo real para a sessão. Por motivos de desempenho, o processamento em tempo real não é recomendado antes do Windows Vista.

Para especificar a sessão de rastreamento da qual você deseja processar eventos, use a [**estrutura EVENT \_ TRACE \_ LOGFILE.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) Você deve inicializar uma cópia dessa estrutura para cada arquivo de log ou sessão em tempo real que deseja processar.

Para consumir eventos de um arquivo de log, de definir o **membro LogFileName** como o nome do arquivo de log. Para consumir eventos da sessão em tempo real, de definir **o membro LoggerName** como o nome da sessão. Você também usa essa estrutura para especificar o retorno de chamada [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) e o retorno de chamada [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) [**ou EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) usado para processar os eventos.

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)— recebe e processa todos os eventos (incluindo o evento de header) de um ou mais arquivos de log e de uma sessão em tempo real. Você implementará esse retorno de chamada se usar as funções auxiliares de dados de rastreamento para analisar os dados do evento ou se quiser recuperar metadados sobre o evento.
-   [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)— recebe e processa todos os eventos (incluindo o evento de header) de um ou mais arquivos de log e de uma sessão em tempo real.
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)— recebe e processa informações resumidas sobre o buffer atual, como eventos perdidos. ETW chama o retorno de chamada depois de entregar todos os eventos no buffer para o consumidor. O consumidor também pode usar esse retorno de chamada para cancelar o processamento de eventos; no entanto, se você estiver consumindo eventos em tempo real, o ETW fornecerá eventos até que o controlador pare a sessão.

Depois de definir uma ou mais sessões de rastreamento, chame a [**função OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) para cada sessão de rastreamento que você deseja processar; você pode processar eventos de um ou mais arquivos de log, mas de apenas uma sessão em tempo real. Em seguida, você passa a lista de alças de sessão de rastreamento que **o OpenTrace** retorna para a [**função ProcessTrace.**](/windows/win32/api/evntrace/nf-evntrace-processtrace) A **função ProcessTrace** combina os eventos, classifica-os em ordem cronológica e, em seguida, os entrega aos retornos de chamada um de cada vez. Os eventos podem ser filtrados para incluir somente aqueles que se enquadram em um período de tempo específico usando os *parâmetros StartTime* e *EndTime.* A **função ProcessTrace** bloqueia o thread até que o consumidor processe todos os eventos nas sessões de rastreamento, [*bufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) retorna **FALSE** ou você chama [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**Antes do Windows Vista:** Você pode chamar [**CloseTrace somente**](/windows/win32/api/evntrace/nf-evntrace-closetrace) após o [**retorno do ProcessTrace.**](/windows/win32/api/evntrace/nf-evntrace-processtrace)

Para ver um exemplo que mostra como consumir eventos publicados usando um manifesto, MOF ou arquivos TMF, consulte Recuperando dados de evento usando [TDH](retrieving-event-data-using-tdh.md). Observe que, a partir do Windows Vista, você deve usar as funções de TDH (auxiliar de dados de rastreamento) para consumir eventos.

Para ver um exemplo que mostra como consumir eventos publicados usando MOF, consulte Recuperando dados [de evento usando MOF](retrieving-event-data-using-mof.md).

 

 
