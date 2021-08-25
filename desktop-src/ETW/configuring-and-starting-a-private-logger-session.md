---
description: Uma sessão de rastreamento de eventos privado é uma sessão de rastreamento de eventos no modo de usuário que é executado no mesmo processo que seus provedores de rastreamento de eventos&8212; a sessão privada e os provedores que ela habilita devem estar todos no \# mesmo processo.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurando e iniciando uma sessão de logger privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf15db05c03e5a412cf07ee6e020d2321380f2d48abba465669dc807729fe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901496"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configurando e iniciando uma sessão de logger privado

Uma sessão de rastreamento de eventos privado é uma sessão de rastreamento de eventos no modo de usuário que é executado no mesmo processo que seus provedores de rastreamento de eventos– a sessão privada e os provedores que ela habilita devem estar todos no mesmo processo. O benefício de usar uma sessão privada é que a sessão privada não conta com relação ao máximo de 64 sessões de rastreamento de eventos em execução simultaneamente.

Configurar e iniciar uma sessão privada é semelhante ao início de uma sessão normal de rastreamento de eventos. A diferença é que **o membro Wnode.Guid** da estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve conter o **GUID** do provedor, não a sessão, e o provedor já deve ter registrado o GUID. Observe que, se você também definir o modo de log EVENT TRACE PRIVATE IN PROC, poderá \_ usar um GUID \_ diferente para a sessão e o \_ \_ provedor.  Para obter detalhes sobre como iniciar uma sessão normal de rastreamento de eventos, consulte Configurando e [iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Observe que você não pode iniciar, parar ou liberar uma sessão de rastreamento privado de DllMain; você deve fazer isso nas rotinas de inicialização e finalização da DLL.

Do Windows 8.1 ao Windows 10, a versão 1607, o conteúdo do evento, o escopo e os filtros de passo a passo de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas [**estruturas ENABLE \_ TRACE \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar condições específicas em uma sessão do logger. Para obter mais informações sobre filtros de conteúdo de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e **AS estruturas ENABLE \_ TRACE \_ PARAMETERS,** **EVENT FILTER \_ \_ DESCRIPTOR** e [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

A partir Windows 10, versão 1703, os usuários de baixo privilégio agora podem iniciar uma sessão de logger privado nos processos que iniciaram. O provedor não precisa mais ser registrado antes de habilitar ou iniciar a sessão privada, o que significa que o provedor é "pré-habilitado" semelhante a como os provedores de sessão não privada são. Há um limite de 8 loggers privados de todo o sistema para um processo individual. Para aumentar o desempenho em cenários de processo cruzado, é recomendável usar a filtragem para APIs de sessão (incluindo [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) [**QueryTrace,**](/windows/win32/api/evntrace/nf-evntrace-querytrace) [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) ao iniciar um logger privado de todo o sistema. Observe que os mesmos filtros devem ser passados para todas as APIs de sessão. Para obter mais informações sobre filtros, consulte [**EVENT \_ TRACE PROPERTIES \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão do NT Kernel Logger, consulte Configurando e iniciando a [sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do Global Logger, consulte [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do AutoLogger, consulte Configurando e [iniciando uma sessão do AutoLogger.](configuring-and-starting-an-autologger-session.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão systemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão do AutoLogger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurando e iniciando a sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**\_HABILITAR \_ PARÂMETROS DE RASTREAMENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**PROPRIEDADES \_ DE RASTREAMENTO DE \_ EVENTO**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**PROPRIEDADES \_ DE RASTREAMENTO DE EVENTO \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**DESCRITOR \_ DE \_ FILTRO DE EVENTO**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PREDICADO \_ DE FILTRO DE \_ CONTEÚDO**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
