---
description: Uma sessão de rastreamento de eventos particulares é uma sessão de rastreamento de eventos no modo de usuário que é executada no mesmo processo que seus provedores de rastreamento de eventos&\# 8212; a sessão privada e os provedores que ela habilita devem estar no mesmo processo.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurando e iniciando uma sessão de agente de log particular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461199"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configurando e iniciando uma sessão de agente de log particular

Uma sessão de rastreamento de eventos particulares é uma sessão de rastreamento de eventos no modo de usuário que é executada no mesmo processo que seus provedores de rastreamento de eventos – a sessão privada e os provedores que ela habilita devem estar no mesmo processo. O benefício de usar uma sessão privada é que a sessão privada não conta com o máximo de 64 sessões de rastreamento de eventos em execução simultaneamente.

Configurar e iniciar uma sessão privada é semelhante a iniciar uma sessão normal de rastreamento de eventos. A diferença é que o membro **Wnode. GUID** da estrutura de [**\_ \_ Propriedades do rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve conter o **GUID** do provedor, e não a sessão, e o provedor já deve ter registrado o GUID. Observe que, se você também definir o \_ rastreamento de eventos \_ privado \_ no \_ modo de log de proc, poderá usar um **GUID** diferente para a sessão e o provedor. Para obter detalhes sobre como iniciar uma sessão normal de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Observe que você não pode iniciar, parar ou liberar uma sessão de rastreamento particular de DllMain; Você deve fazer isso nas rotinas de inicialização e finalização da DLL.

De Windows 8.1 para o Windows 10, a versão 1607, a carga do evento, o escopo e os filtros de exame de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar as condições específicas em uma sessão de agente. Para obter mais informações sobre filtros de carga de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e as estruturas [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **Enable \_ trace \_**, **\_ \_ descritor de filtro de evento** e conteúdo de filtro de carga.

A partir do Windows 10, versão 1703, os usuários com privilégios baixos agora podem iniciar uma sessão de agente de log particular em processos iniciados. O provedor não precisa mais ser registrado antes de habilitar ou iniciar a sessão privada, o que significa que o provedor é "habilitado previamente", semelhante a como os provedores de sessão não privados são. Há um limite de oito agentes particulares do sistema em um processo individual. Para aumentar o desempenho em cenários de processo cruzado, é recomendável usar a filtragem para APIs de sessão (incluindo [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) ao iniciar um agente de log particular do sistema. Observe que os mesmos filtros devem ser passados para todas as APIs de sessão. Para obter mais informações sobre filtros, [**consulte \_ Propriedades de rastreamento de eventos \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão do agente do NT kernel, consulte [Configurando e iniciando a sessão do agente de log do NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão de agente global, consulte [Configurando e iniciando uma sessão global de agente](configuring-and-starting-the-global-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do agente de log autologger, consulte [Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Habilitar \_ parâmetros de rastreamento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_Propriedades de rastreamento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Propriedades de rastreamento de eventos \_ \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**\_descritor de filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**predicado de filtro de carga \_ \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
