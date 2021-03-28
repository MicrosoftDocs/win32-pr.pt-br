---
description: Os consumidores de rastreamento de eventos podem processar eventos de um ou mais provedores.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Consumindo eventos (rastreamento de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968226"
---
# <a name="consuming-events-event-tracing"></a>Consumindo eventos (rastreamento de eventos)

Os consumidores de rastreamento de eventos podem processar eventos de um ou mais provedores. Os consumidores podem processar eventos de um arquivo de log ou em tempo real. Você só poderá consumir eventos em tempo real se o controlador especificar o modo de log em tempo real para a sessão. Por motivos de desempenho, o processamento em tempo real não é recomendado antes do Windows Vista.

Para especificar a sessão de rastreamento da qual você deseja processar eventos, use a estrutura de arquivo de [**\_ \_ log do rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) . Você deve inicializar uma cópia dessa estrutura para cada arquivo de log ou sessão em tempo real que você deseja processar.

Para consumir eventos de um arquivo de log, defina o membro **LogFileName** como o nome do arquivo de log. Para consumir eventos da sessão em tempo real, defina o membro **loggername** como o nome da sessão. Você também usa essa estrutura para especificar o retorno de chamada [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) e o retorno de chamada [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) ou [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) usado para processar os eventos.

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)– recebe e processa todos os eventos (incluindo o evento de cabeçalho) de um ou mais arquivos de log e uma sessão em tempo real. Você implementará esse retorno de chamada se usar as funções auxiliares de dados de rastreamento para analisar os dados de evento ou se quiser recuperar metadados sobre o evento.
-   [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)– recebe e processa todos os eventos (incluindo o evento de cabeçalho) de um ou mais arquivos de log e uma sessão em tempo real.
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)– recebe e processa informações de resumo sobre o buffer atual, como eventos perdidos. O ETW chama o retorno de chamada depois de fornecer todos os eventos no buffer para o consumidor. O consumidor também pode usar esse retorno de chamada para cancelar o processamento de eventos; no entanto, se você estiver consumindo eventos em tempo real, o ETW entregará eventos até que o controlador interrompa a sessão.

Depois de definir uma ou mais sessões de rastreamento, chame a função [**OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) para cada sessão de rastreamento que você deseja processar; Você pode processar eventos de um ou mais arquivos de log, mas apenas de uma sessão em tempo real. Em seguida, você passa a lista de identificadores de sessão de rastreamento que **OpenTrace** retorna para a função [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) . A função **ProcessTrace** combina os eventos, classifica-os em ordem cronológica e, em seguida, os entrega aos retornos de chamada um de cada vez. Os eventos podem ser filtrados para incluir somente aqueles que se enquadram em um período de tempo específico usando os parâmetros *StartTime* e *EndTime* . A função **ProcessTrace** bloqueia o thread até que seu consumidor processe todos os eventos nas sessões de rastreamento, o [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) retorna **false** ou você chama [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**Antes do Windows Vista:** Você pode chamar [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) somente após o retorno de [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) .

Para obter um exemplo que mostra como consumir eventos publicados usando um manifesto, MOF ou arquivos TMF, consulte [recuperando dados de evento usando TDH](retrieving-event-data-using-tdh.md). Observe que, a partir do Windows Vista, você deve usar as funções auxiliar de dados de rastreamento (TDH) para consumir eventos.

Para obter um exemplo que mostra como consumir eventos publicados usando o MOF, consulte [recuperando dados de evento usando o MOF](retrieving-event-data-using-mof.md).

 

 
