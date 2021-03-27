---
description: O ETW (rastreamento de eventos para Windows) é um recurso de rastreamento eficiente no nível de kernel que permite que você registre eventos de kernel ou definidos pelo aplicativo em um arquivo de log.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Sobre o rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921066"
---
# <a name="about-event-tracing"></a>Sobre o rastreamento de eventos

O ETW (rastreamento de eventos para Windows) é um recurso de rastreamento eficiente no nível de kernel que permite que você registre eventos de kernel ou definidos pelo aplicativo em um arquivo de log. Você pode consumir os eventos em tempo real ou de um arquivo de log e usá-los para depurar um aplicativo ou para determinar onde estão ocorrendo problemas de desempenho no aplicativo.

O ETW permite habilitar ou desabilitar o rastreamento de eventos dinamicamente, permitindo que você execute o rastreamento detalhado em um ambiente de produção sem exigir reinicializações do computador ou do aplicativo.

A API de rastreamento de eventos é dividida em três componentes distintos:

-   [Controladores](#controllers), que iniciam e paramm uma sessão de rastreamento de eventos e habilitam provedores
-   [Provedores](#providers), que fornecem os eventos
-   [Consumidores](#consumers), que consomem os eventos

O diagrama a seguir mostra o modelo de rastreamento de eventos.

![modelo de rastreamento de eventos](images/etdiag2.png)

## <a name="controllers"></a>Controladores

Controladores são aplicativos que definem o tamanho e o local do arquivo de log, iniciam e param [sessões de rastreamento de eventos](event-tracing-sessions.md), habilitam provedores para que possam registrar eventos na sessão, gerenciar o tamanho do pool de buffers e obter estatísticas de execução para sessões. As estatísticas de sessão incluem o número de buffers usados, o número de buffers entregues e o número de eventos e buffers perdidos. 

Para obter mais informações, consulte [controlando sessões de rastreamento de eventos](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Provedores

Provedores são aplicativos que contêm a instrumentação de rastreamento de eventos. Depois que um provedor se registra, um controlador pode habilitar ou desabilitar o rastreamento de eventos no provedor. O provedor define sua interpretação de ser habilitada ou desabilitada. Geralmente, um provedor habilitado gera eventos, enquanto um provedor desabilitado não faz isso. Isso permite que você adicione o rastreamento de eventos ao seu aplicativo sem exigir que ele gere eventos o tempo todo. 

Embora o modelo ETW separe o controlador e o provedor em aplicativos separados, um aplicativo pode incluir ambos os componentes.

Para obter mais informações, consulte [fornecendo eventos](providing-events.md).

### <a name="types-of-providers"></a>Tipos de provedores

Há quatro tipos principais de provedores: provedores MOF (clássicos), provedores de WPP, provedores baseados em manifesto e provedores de TraceLogging. Você deve usar um provedor baseado em manifesto ou um provedor TraceLogging se estiver escrevendo aplicativos para o Windows Vista ou posterior que não precisam oferecer suporte a sistemas herdados.

#### <a name="mof-classic-providers"></a>Provedores MOF (clássicos):

-   Use as funções [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) e [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar e gravar eventos.
-   Use classes MOF para definir eventos para que os consumidores saibam como consumi-los.
-   Pode ser habilitado por apenas uma sessão de rastreamento por vez.

#### <a name="wpp-providers"></a>Provedores de WPP:

-   Use as funções [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) e [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar e gravar eventos.
-   Ter arquivos TMF associados (compilados em um. pdb binário) contendo informações de decodificação inferidas da verificação do pré-processador da instrumentação de WPP no código-fonte.
-   Pode ser habilitado por apenas uma sessão de rastreamento por vez.

#### <a name="manifest-based-providers"></a>Provedores baseados em manifesto:

-   Use [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para registrar e gravar eventos.
-   Use um manifesto para definir eventos para que os consumidores saibam como consumi-los.
-   Pode ser habilitado por até oito sessões de rastreamento simultaneamente.

#### <a name="tracelogging-providers"></a>Provedores de [TraceLogging](/windows/desktop/tracelogging/trace-logging-about) :

-   Use [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) e [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para registrar e gravar eventos.
-   Use eventos autodescritivos para que os próprios eventos contenham todas as informações necessárias para consumi-los.
-   Pode ser habilitado por até oito sessões de rastreamento simultaneamente.

Todos os provedores de eventos usam fundamentalmente a família de APIs de rastreamento de eventos ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para tecnologias herdadas e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para as mais recentes). Os provedores de eventos são simplesmente diferentes em quais tipos de campos eles armazenam em cargas de eventos e onde armazenam as informações de decodificação de eventos associadas.

## <a name="consumers"></a>Consumidores

Os consumidores são aplicativos que selecionam uma ou mais sessões de rastreamento de eventos como uma fonte de eventos. Um consumidor pode solicitar eventos de várias sessões de rastreamento de eventos simultaneamente; o sistema entrega os eventos em ordem cronológica. Os consumidores podem receber eventos armazenados em arquivos de log ou de sessões que entregam eventos em tempo real. Durante o processamento de eventos, um consumidor pode especificar horários de início e término, e somente os eventos que ocorrem no período de tempo especificado serão entregues. 

Para obter mais informações, consulte [consumindo eventos](consuming-events.md).

## <a name="missing-events"></a>Eventos ausentes

O PerfMon, o diagnóstico do sistema e outras ferramentas do sistema podem relatar eventos ausentes no log de eventos e indicar que as configurações do ETW (rastreamento de eventos para Windows) podem não ser ideais. Os eventos podem ser perdidos por vários motivos:

-   O tamanho total do evento é maior que 64K. Isso inclui o cabeçalho ETW mais os dados ou a carga. Um usuário não tem controle sobre esses eventos ausentes, pois o tamanho do evento é configurado pelo aplicativo.

-   O tamanho do buffer ETW é menor do que o tamanho total do evento. Um usuário não tem controle sobre esses eventos ausentes, pois o tamanho do evento é configurado pelo aplicativo que registra os eventos em log.

-   Para o registro em log em tempo real, o consumidor em tempo real não está consumindo eventos rápido o suficiente ou não está presente completamente e, em seguida, o arquivo de backup está se enchendo. Isso pode ocorrer se o serviço log de eventos for interrompido e iniciado quando os eventos estiverem sendo registrados. Um usuário não tem controle sobre esses eventos ausentes.

-   Ao fazer logon em um arquivo, o disco fica muito lento para acompanhar a taxa de registro em log.

Por qualquer um desses motivos, informe esses problemas ao provedor do aplicativo ou serviço que está gerando os eventos. Esses problemas só podem ser corrigidos pelo desenvolvedor do aplicativo ou pelo serviço que está registrando os eventos. Se os eventos ausentes estiverem sendo relatados no serviço log de eventos, isso poderá indicar um problema com a configuração do serviço log de eventos. O usuário pode ter alguma capacidade limitada para aumentar o espaço máximo em disco a ser usado pelo serviço de log de eventos, o que pode reduzir o número de eventos ausentes.

 

 
