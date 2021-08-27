---
description: Esta seção descreve os novos recursos que foram adicionados ao Rastreamento de Eventos para Windows em cada versão.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Novidades no rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da1c6f1b54ae8bc4b91bd511bface8569bcf43b2893329b1b0462b46c001724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102016"
---
# <a name="whats-new-in-event-tracing"></a>Novidades no rastreamento de eventos

Esta seção descreve os novos recursos que foram adicionados ao Rastreamento de Eventos para Windows em cada versão.

## <a name="windows-10-version-1709"></a>Windows 10, versão 1709

O ETW agora pode, opcionalmente, rastrear binários para todos os provedores habilitados para a sessão. O acompanhamento aplica-se retroativamente a provedores que foram habilitados para a sessão antes da chamada, bem como para todos os provedores futuros habilitados para a sessão. Agora você também pode consultar o número máximo configurado atualmente de madeirões do sistema permitidos pelo sistema operacional. Para obter mais informações, consulte os valores **TraceProviderBinaryTracking** e **TraceMaxLoggersQuery** da [**enumeração TRACE \_ INFO \_ CLASS,**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) bem como Recuperando dados adicionais de rastreamento de [eventos.](retrieving-additional-event-tracing-data.md)

O ETW agora pode filtrar eventos com base no nome do evento. Você também pode determinar quais eventos capturam suas pilhas. Para obter mais informações, consulte os valores EVENT NAME EVENT NAME , EVENT FILTER TYPE **\_ \_ \_ STACKWALK \_ NAME** e EVENT FILTER TYPE **\_ \_ \_ STACKWALK \_ LEVEL \_ KW** da estrutura [**EVENT FILTER \_ \_ DESCRIPTOR,**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) bem como as estruturas [**associadas EVENT \_ FILTER \_ EVENT \_ NAME**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) e [**EVENT FILTER LEVEL \_ \_ \_ KW.**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) **\_ \_ \_ \_**

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) se baseia no ETW e fornece uma maneira simplificada de instrumentar o código para desenvolvedores nativos, do .NET e do WinRT. TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.

[As características do](provider-traits.md) provedor foram adicionadas como um método para anexar mais dados a um registro de provedor individual. Eles podem ser usados para provedores baseados em manifesto ou TraceLogging. Atualmente, isso inclui suporte para adicionar um Nome do Provedor e/ou um Grupo de Provedores a um registro de provedor individual. Os Grupos de Provedores são um novo recurso para permitir que vários provedores ETW sejam controlados em agregação pelo grupo ao que pertencem.

O estado de captura periódico é uma maneira de permitir que as notificações de estado de captura sejam enviadas rotineiramente aos provedores. Quando isso estiver habilitado, as notificações serão enviadas somente para registros de provedor que foram habilitados anteriormente para a sessão atual. Cada provedor pode definir sua própria resposta (se alguma) para uma notificação. Para obter detalhes de implementação, consulte [**TRACE PERIODIC CAPTURE STATE \_ \_ \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Os recursos a seguir foram adicionados ao Rastreamento de Eventos Windows 8.1 e Windows Server 2012 R2.

Funções que suportam o uso de filtros de carga de evento, escopo e passo a passo usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e as [**estruturas ENABLE \_ TRACE \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar condições específicas em uma sessão do logger. Para obter mais informações, consulte:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Além disso, confira a documentação revisada extensivamente para a função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e as [**estruturas ENABLE \_ TRACE \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) que são usadas por esses recursos.

Uma estrutura que define um predicado de filtro de conteúdo de evento que descreve como filtrar em um único campo em uma sessão de rastreamento usada pela nova [**função TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) e uma nova estrutura usada pela ID de evento e filtros de passo a passo de pilha. Para obter mais informações, consulte:

-   [**\_ID DO EVENTO DE \_ FILTRO DE \_ EVENTO**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**PREDICADO \_ DE FILTRO DE \_ CONTEÚDO**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funções que recuperam informações sobre eventos presentes no manifesto do provedor. Para obter mais informações, consulte:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Uma estrutura que define uma matriz de eventos em um manifesto do provedor usado pela nova [**função TdhEnumerateManifestProviderEvents.**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) Para obter mais informações, consulte:

-   [**INFORMAÇÕES \_ DE EVENTO DO \_ PROVEDOR**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Os recursos a seguir foram adicionados ao Rastreamento de Eventos Windows 8 e Windows Server 2012.

Funções que executam operações em um objeto de registro, fornecem análise de conteúdo do evento, fornecem navegação do provedor de rastreamento, consultam configurações de sessão de rastreamento de eventos e processam um arquivo de rastreamento relogged. Para obter mais informações, consulte:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfaces que fornecem informações ao relogger sobre o processo de rastreamento e quando eventos são registrados em log, acesso a dados para um evento específico e acesso a recursos de relogger que permitem a manipulação de arquivos ETL (Log de Rastreamento de Eventos). Para obter mais informações, consulte:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumerações adicionais usadas pelas novas funções e interfaces. Para obter mais informações, consulte:

-   [**CLASSE EVENT \_ INFO \_**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**CLASSE TRACE \_ QUERY \_ INFO \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Os seguintes recursos foram adicionados nesta versão:

-   A capacidade de os provedores definirem filtros no manifesto. No Windows Vista, os controladores podem passar dados de filtro para o provedor. No entanto, o layout dos dados de filtro não foi definido no manifesto, portanto, o provedor teria que usar outros meios para fornecer a definição de filtro aos controladores. Com esta versão, os provedores podem definir a definição de filtro no manifesto (consulte o atributo **filters** do [**tipo complexo ProviderType).**](../wes/eventmanifestschema-providertype-complextype.md) Os controladores podem usar a [**função TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) para determinar a definição do filtro. Provedores que usam filtros devem usar a [**função EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para gravar o evento.
-   A capacidade de usar um único buffer para coletar eventos gerados em vários processadores. O uso de um único buffer elimina que os eventos apareçam fora de ordem em computadores com vários processadores. Para obter detalhes, consulte o modo [**de log EVENT TRACE NO PER PROCESSOR \_ \_ \_ \_ \_ BUFFERING.**](logging-mode-constants.md) Por padrão, o ETW usa buffers por processador.
-   A capacidade de capturar um rastreamento de pilha para eventos. Para habilitar o rastreamento de pilha para eventos de kernel, consulte [**a função TraceSetInformation.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) Para habilitar o rastreamento de pilha para eventos de usuário, consulte o **sinalizador EVENT ENABLE PROPERTY STACK TRACE \_ \_ \_ \_ para** o membro **EnableProperty** [**de ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   A capacidade de especificar o MODO DE **\_ BUFFER \_ \_ DE** RASTREAMENTO DE EVENTOS ou o modo de log **\_ \_ \_ \_ NEWFILE DO** MODO DE ARQUIVO DE RASTREAMENTO DE EVENTO com o modo de registro em log DO MODO DE AGENTE PRIVADO DO RASTREAMENTO DE EVENTOS (consulte [Constantes](logging-mode-constants.md)do modo de registro em log ). **\_ \_ \_ \_**
-   A capacidade de habilitar um provedor de forma síncrona. Por padrão, os provedores são habilitados de forma assíncrona. Para habilitar um provedor de forma síncrona, de definido o parâmetro *Timeout* de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   A capacidade do controlador de solicitar que o provedor registre seu estado. Para obter detalhes, consulte o **sinalizador EVENT CONTROL CODE CAPTURE \_ \_ \_ \_ STATE** para o *parâmetro ControlCode* de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   A capacidade dos consumidores de formatar dados de evento usando a [**função TdhFormatProperty.**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   A capacidade de decodificar eventos manifestos em computadores que não contêm o provedor. Para obter detalhes, consulte a [**função TdhLoadManifest.**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)

As seguintes funções foram adicionadas nesta versão:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

As seguintes estruturas foram adicionadas nesta versão:

-   [**\_ID DE \_ EVENTO CLÁSSICO**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**\_HABILITAR \_ PARÂMETROS DE RASTREAMENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**\_TRACE32 de \_ pilha de item estendido de \_ evento \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**\_TRACE64 de \_ pilha de item estendido de \_ evento \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_cabeçalho do filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_informações de filtro do provedor \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

As seguintes enumerações foram adicionadas nesta versão:

-   [**\_classe de informações de rastreamento \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

As seguintes classes MOF foram adicionadas nesta versão:

-   [**StackWalk**](stackwalk.md)
-   [**\_Evento StackWalk**](stackwalk-event.md)

 

 
