---
description: Os provedores clássicos usam a função TraceEventInstance para rastrear eventos que fazem parte de uma única transação. Você também pode usar essa função para rastrear eventos pai/filho.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Gravando eventos relacionados em um provedor clássico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41443c0a05bd94e25ae4ca6a4549671c6aa0682b848660ca31683bb4bf8b75b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813808"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Gravando eventos relacionados em um provedor clássico

Os provedores [clássicos](about-event-tracing.md) usam a função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para rastrear eventos que fazem parte de uma única transação. Você também pode usar essa função para rastrear eventos pai/filho.

Antes de chamar a função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) , você deve primeiro chamar a função [**CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) para obter um identificador de transação. Essa função gera um identificador de transação exclusivo e o mapeia para um identificador de GUID de classe registrado. Os identificadores de GUIDs de classe registrados estão disponíveis nos membros **RegHandle** de estruturas de [**registro de \_ GUID \_ de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) , depois de chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . O identificador de transação é colocado no membro **InstanceId** de uma estrutura de [**\_ \_ informações da instância de evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) que você passa para a função **CreateTraceInstanceId** .

A estrutura de [**\_ \_ cabeçalho da instância de evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) que é passada para a função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) é semelhante à estrutura de cabeçalho de [**\_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (consulte [eventos de rastreamento](tracing-events.md)), exceto que ela contém informações adicionais relacionadas a instâncias e não contém um membro **GUID** .

As instâncias de evento podem ser usadas para estabelecer uma relação hierárquica entre eventos. A função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) aceita informações específicas da instância de duas instâncias de evento. O parâmetro *pInstInfo* aponta para a estrutura de [**\_ \_ informações da instância de evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) da instância do evento e o parâmetro *pParentInstInfo* aponta para a estrutura de **\_ \_ informações da instância de evento** de uma instância de evento pai. A definição de uma instância de evento "pai" é definida pelo aplicativo; o pai pode ser qualquer instância que já tenha sido gerada.

 

 
