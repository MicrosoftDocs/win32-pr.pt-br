---
description: Esta seção descreve os novos recursos que foram adicionados ao rastreamento de eventos para Windows em cada versão.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: O que há de novo no rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647532"
---
# <a name="whats-new-in-event-tracing"></a>O que há de novo no rastreamento de eventos

Esta seção descreve os novos recursos que foram adicionados ao rastreamento de eventos para Windows em cada versão.

## <a name="windows-10-version-1709"></a>Windows 10, versão 1709

O ETW agora pode, opcionalmente, rastrear binários para todos os provedores habilitados para a sessão. O rastreamento aplica-se retroativamente para provedores que foram habilitados para a sessão antes da chamada, bem como para todos os provedores futuros que estão habilitados para a sessão. Agora, você também pode consultar o número máximo configurado atualmente de agentes de log do sistema permitidos pelo sistema operacional. Para obter mais informações, consulte os valores **TraceProviderBinaryTracking** e **TraceMaxLoggersQuery** da enumeração de [**\_ \_ classes Trace info**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , bem como [recuperando dados adicionais de rastreamento de eventos](retrieving-additional-event-tracing-data.md).

O ETW agora pode filtrar eventos com base no nome do evento. Você também pode determinar quais eventos podem ser capturados por suas pilhas. Para obter mais informações, consulte **o \_ \_ nome do \_ evento \_ do tipo** de filtro de evento, o tipo de filtro de **evento \_ \_ \_ STACKWALK \_ nome** e o **tipo de filtro de evento \_ \_ \_ STACKWALK \_ nível \_ kW** valores da estrutura do [**\_ \_ descritor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) , bem como as estruturas [**\_ \_ \_ kW**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) de [**\_ \_ \_ nome do evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) e filtro de eventos associados.

## <a name="windows-10"></a>Windows 10

O [TraceLogging](../tracelogging/trace-logging-portal.md) se baseia no ETW e fornece uma maneira simplificada de instrumentar o código para desenvolvedores nativos, .net e WinRT. O TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.

As [características do provedor](provider-traits.md) foram adicionadas como um método de anexar mais dados a um registro de provedor individual. Eles podem ser usados para provedores baseados em manifesto ou TraceLogging. Atualmente, isso inclui suporte para adicionar um nome de provedor e/ou um grupo de provedores a um registro de provedor individual. Os grupos de provedores são um novo recurso para permitir que vários provedores de ETW sejam controlados em agregação pelo grupo ao qual pertencem.

O estado de captura periódica é uma maneira de permitir que notificações de estado de captura sejam enviadas rotineiramente aos provedores. Quando isso estiver habilitado, as notificações serão enviadas somente aos registros do provedor que foram habilitados anteriormente para a sessão atual. Cada provedor pode definir sua própria resposta (se houver) para uma notificação. Para obter detalhes de implementação, consulte [**rastrear \_ \_ informações de \_ estado \_ de captura periódica**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Os recursos a seguir foram adicionados ao rastreamento de eventos no Windows 8.1 e no Windows Server 2012 R2.

Funções que dão suporte ao uso de carga de evento, escopo e filtros de movimentação de pilha usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e as estruturas de [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) e [**\_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para filtrar em condições específicas em uma sessão de agente. Para obter mais informações, consulte:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Além disso, consulte a documentação amplamente revisada para a função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e as estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) que são usadas por esses recursos.

Uma estrutura que define um predicado de filtro de carga de evento que descreve como filtrar em um único campo em uma sessão de rastreamento usada pela nova função [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) e uma nova estrutura usada pelos filtros de ID de evento e de movimentação de pilha. Para obter mais informações, consulte:

-   [**\_ID do \_ evento de filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**predicado de filtro de carga \_ \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funções que recuperam informações sobre eventos presentes no manifesto do provedor. Para obter mais informações, consulte:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Uma estrutura que define uma matriz de eventos em um manifesto de provedor usado pela nova função [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) . Para obter mais informações, consulte:

-   [**\_informações de evento do provedor \_**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Os recursos a seguir foram adicionados ao rastreamento de eventos no Windows 8 e no Windows Server 2012.

Funções que executam operações em um objeto de registro, fornecem análise de carga de evento, fornecem navegação de provedor de rastreamento, configurações de sessão de rastreamento de eventos de consulta e processam um arquivo de rastreamento reregistrado. Para obter mais informações, consulte:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfaces que fornecem informações para o relogger no processo de rastreamento e quando os eventos são registrados, acesso a dados para um evento específico e acesso a recursos de relogger que permitem a manipulação de arquivos ETL (log de rastreamento de eventos). Para obter mais informações, consulte:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumerações adicionais usadas pelas novas funções e interfaces. Para obter mais informações, consulte:

-   [**\_classe de informações de evento \_**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_classe de \_ informações de consulta de rastreamento \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Os seguintes recursos foram adicionados nesta versão:

-   A capacidade dos provedores de definir filtros no manifesto. No Windows Vista, os controladores podem passar dados de filtro para o provedor. No entanto, o layout dos dados de filtro não foi definido no manifesto, portanto, o provedor teria que usar outros meios para fornecer a definição de filtro aos controladores. Com esta versão, os provedores podem definir a definição do filtro no manifesto (consulte o atributo **Filters** do tipo complexo [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) ). Os controladores podem usar a função [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) para determinar a definição do filtro. Provedores que usam filtros devem usar a função [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para gravar o evento.
-   A capacidade de usar um único buffer para coletar eventos gerados em vários processadores. O uso de um único buffer elimina a exibição de eventos fora de ordem em computadores com vários processadores. Para obter detalhes, consulte o modo de log do [**rastreamento de eventos \_ \_ não \_ por \_ processador em \_ buffer**](logging-mode-constants.md) . Por padrão, o ETW usa buffers por processador.
-   A capacidade de capturar um rastreamento de pilha para eventos. Para habilitar o rastreamento de pilha para eventos de kernel, consulte a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . Para habilitar o rastreamento de pilha para eventos de usuário, consulte o sinalizador de **\_ rastreamento de \_ \_ pilha \_ de propriedade habilitar evento** para o membro **preaptoproperty** de [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   A capacidade de especificar o modo de **buffer de rastreamento de eventos \_ \_ \_** ou o modo de log do modo de arquivo de rastreamento de eventos no modo de registro [](logging-mode-constants.md)em log do **\_ \_ \_ \_ modo de agente particular do rastreamento de eventos** (consulte constantes do modo de log). **\_ \_ \_ \_**
-   A capacidade de habilitar um provedor de forma síncrona. Por padrão, os provedores são habilitados de forma assíncrona. Para habilitar um provedor de forma síncrona, defina o parâmetro *Timeout* de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   A capacidade do controlador de solicitar que o provedor Registre seu estado. Para obter detalhes, consulte o sinalizador estado de captura de código de  controle de **evento \_ \_ \_ \_** para o parâmetro ControlCode de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   A capacidade de os consumidores formatarem dados de eventos usando a função [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) .
-   A capacidade de decodificar eventos manifestados em computadores que não contêm o provedor. Para obter detalhes, consulte a função [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) .

As seguintes funções foram adicionadas nesta versão:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

As seguintes estruturas foram adicionadas nesta versão:

-   [**\_ID do evento clássico \_**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**Habilitar \_ parâmetros de rastreamento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**\_TRACE32 de \_ pilha de item estendido de \_ evento \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**\_TRACE64 de \_ pilha de item estendido de \_ evento \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_cabeçalho do filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_informações de filtro do provedor \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

As seguintes enumerações foram adicionadas nesta versão:

-   [**\_classe de informações de rastreamento \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

As seguintes classes MOF foram adicionadas nesta versão:

-   [**StackWalk**](stackwalk.md)
-   [**\_Evento StackWalk**](stackwalk-event.md)

 

 
