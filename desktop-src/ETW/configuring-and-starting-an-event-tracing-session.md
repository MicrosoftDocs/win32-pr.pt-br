---
description: Para configurar uma sessão de rastreamento de eventos, use \_ a \_ estrutura Propriedades de rastreamento de eventos para especificar as propriedades da sessão.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configurando e iniciando uma sessão de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968250"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configurando e iniciando uma sessão de rastreamento de eventos

Para configurar uma sessão de rastreamento de eventos, use a estrutura [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar as propriedades da sessão. A memória que você aloca para a estrutura de **\_ \_ Propriedades de rastreamento de eventos** deve ser grande o suficiente para conter também os nomes de arquivos de log e de sessão que seguem a estrutura na memória.

Depois de especificar as propriedades da sessão, chame a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) para iniciar a sessão. Se a função for bem sucedido, o parâmetro *SessionHandle* conterá o identificador de sessão e a propriedade **LoggerNameOffset** conterá o deslocamento para o nome da sessão.

Para habilitar os provedores em que você deseja registrar eventos em sua sessão, chame a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar provedores clássicos e a função [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar provedores [baseados em manifesto](about-event-tracing.md) . Para habilitar os provedores em que você deseja que os eventos de log sejam filtrados em condições específicas em Windows 8.1, Windows Server 2012 R2 e posterior, chame a função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) .

Além disso, você também pode rastrear informações adicionais sobre um evento com uma chamada para a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . O **TraceSetInformation** coloca informações de rastreamento adicionais na seção de dados estendidos de um evento e pode incluir informações como as informações de versão de rastreamento ou quais provedores estão atualmente registrados no sistema. Para obter mais informações, consulte [recuperando dados adicionais de rastreamento de eventos](retrieving-additional-event-tracing-data.md).

Até oito sessões de rastreamento podem habilitar e receber eventos do mesmo provedor [baseado em manifesto](about-event-tracing.md) . No entanto, apenas uma sessão de rastreamento pode habilitar um provedor [clássico](about-event-tracing.md) . Se mais de uma sessão de rastreamento tentar habilitar um provedor clássico, a primeira sessão deixaria de receber eventos quando a segunda sessão habilitar o provedor. Por exemplo, se A sessão é um provedor habilitado 1 e, em seguida, A sessão B habilitou o provedor 1, somente a sessão B receberia eventos do provedor 1.

Você pode usar qualquer uma das três funções para habilitar um provedor, mas poderá perder a funcionalidade se usar o [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar um provedor baseado em manifesto porque não será possível fornecer um valor de MatchAllKeyword, especificar itens de dados estendidos para incluir no evento ou fornecer dados de filtro definidos pelo provedor. Para obter mais informações, consulte a seção comentários de cada função.

No Windows 8.1, o Windows Server 2012 R2 e posterior, o conteúdo do evento, o escopo e os filtros de exame de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar as condições específicas em uma sessão de agente. Para obter mais informações sobre filtros de carga de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e as estruturas [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **Enable \_ trace \_**, **\_ \_ descritor de filtro de evento** e conteúdo de filtro de carga.

Para determinar o nível e as palavras-chave usadas para habilitar um provedor baseado em manifesto, use um dos seguintes comandos:

-   Provedor de **consultas** **logman** *-nome*
-   *Nome do provedor de* **GP** de **wevtutil**

Os comandos listam apenas o nível e as palavras-chave, o provedor deve documentar os requisitos de dados de filtro para possíveis controladores.

Para enumerar os provedores baseados em manifesto, use **wevtutil** **EP**.

Para provedores clássicos, cabe ao provedor documentar e disponibilizar para controladores em potencial os níveis de severidade ou habilitar sinalizadores que ele suporta. Se o provedor quiser ser habilitado por qualquer controlador, o provedor deverá aceitar 0 para o nível de severidade e habilitar sinalizadores e interpretar 0 como uma solicitação para executar o registro em log padrão (o que for possível).

Você pode habilitar o provedor antes ou depois que o provedor se registrar. Depois de habilitar o provedor, o ETW chamará a função de retorno de chamada do provedor. Se o provedor não estiver registrado, o ETW chamará a função de retorno de chamada do provedor depois que ele se registrar.

Você também pode usar a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para desabilitar o provedor (parar de registrar eventos em log em sua sessão) ou para atualizar o nível de log ou habilitar os sinalizadores do provedor. Com a função [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) , você pode desabilitar o provedor ou atualizar o nível, as palavras-chave, os dados estendidos e os dados de filtro. Cada vez que você chama a função **EnableTrace** ou **ENABLETRACEEX** , o ETW chama a função de retorno de chamada do provedor. O provedor permanece habilitado para a sessão até que a sessão desabilite o provedor.

Para interromper a sessão de rastreamento após coletar eventos, chame a função [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e passe o controle de rastreamento de evento \_ \_ \_ parar como o código de controle. Para especificar a sessão a ser interrompida, você pode passar o identificador de sessão de rastreamento de eventos obtido de uma chamada anterior para a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) ou o nome de uma sessão iniciada anteriormente. Certifique-se de desabilitar todos os provedores antes de parar a sessão. Se você parar a sessão antes de desabilitar primeiro o provedor, o ETW desabilitará o provedor e tentará chamar a função de retorno de chamada de controle do provedor. Se o aplicativo que iniciou a sessão terminar sem desabilitar o provedor ou chamar a função **ControlTrace** , o provedor permanecerá habilitado.

Se [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) for bem-sucedido, as propriedades da sessão serão atualizadas para refletir os valores de propriedade final e as estatísticas de execução da sessão de rastreamento de eventos.

Para obter um exemplo que inicia uma sessão de rastreamento de eventos, consulte o seguinte:

-   [Exemplo que cria uma sessão e habilita um provedor baseado em manifesto](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) – inicia uma sessão de rastreamento, habilita um provedor baseado em manifesto, desabilita o provedor e, em seguida, interrompe a sessão.

Para obter detalhes sobre como iniciar uma sessão de rastreamento, consulte um dos seguintes:

-   [Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md)
-   [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md)
-   [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Habilitar \_ parâmetros de rastreamento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_descritor de filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_Propriedades de rastreamento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**predicado de filtro de carga \_ \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
