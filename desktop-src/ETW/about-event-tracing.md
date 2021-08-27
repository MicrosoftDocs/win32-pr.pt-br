---
description: O ETW (Rastreamento de Eventos para Windows) é um recurso eficiente de rastreamento no nível do kernel que permite registrar eventos de kernel ou definidos pelo aplicativo em um arquivo de log.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Sobre o rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5004ada6d0d11d9c232a6fda1553ea24de5a59fb1d03e46728084f84f0e79de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086426"
---
# <a name="about-event-tracing"></a>Sobre o rastreamento de eventos

O ETW (Rastreamento de Eventos para Windows) é um recurso eficiente de rastreamento no nível do kernel que permite registrar eventos de kernel ou definidos pelo aplicativo em um arquivo de log. Você pode consumir os eventos em tempo real ou em um arquivo de log e usá-los para depurar um aplicativo ou determinar onde estão ocorrendo problemas de desempenho no aplicativo.

O ETW permite habilitar ou desabilitar o rastreamento de eventos dinamicamente, permitindo que você execute o rastreamento detalhado em um ambiente de produção sem exigir reinicializações de computador ou aplicativo.

A API de Rastreamento de Eventos é dividida em três componentes distintos:

-   [Controladores](#controllers), que iniciam e param uma sessão de rastreamento de eventos e habilitam provedores
-   [Provedores](#providers), que fornecem os eventos
-   [Consumidores](#consumers), que consomem os eventos

O diagrama a seguir mostra o modelo de rastreamento de eventos.

![modelo de rastreamento de eventos](images/etdiag2.png)

## <a name="controllers"></a>Controladores

Os controladores são aplicativos que definem o tamanho e o local do arquivo de log, iniciam e param sessões de rastreamento de eventos, habilitam provedores para que possam registrar eventos na sessão, gerenciar o tamanho do pool de [buffers](event-tracing-sessions.md)e obter estatísticas de execução para sessões. As estatísticas de sessão incluem o número de buffers usados, o número de buffers entregues e o número de eventos e buffers perdidos. 

Para obter mais informações, consulte [Controlando sessões de rastreamento de eventos](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Provedores

Provedores são aplicativos que contêm instrumentação de rastreamento de eventos. Depois que um provedor se registrar, um controlador poderá habilitar ou desabilitar o rastreamento de eventos no provedor. O provedor define sua interpretação de estar habilitado ou desabilitado. Em geral, um provedor habilitado gera eventos, enquanto um provedor desabilitado não gera. Isso permite adicionar o rastreamento de eventos ao seu aplicativo sem exigir que ele gere eventos o tempo todo. 

Embora o modelo ETW separe o controlador e o provedor em aplicativos separados, um aplicativo pode incluir ambos os componentes.

Para obter mais informações, consulte [Fornecendo eventos](providing-events.md).

### <a name="types-of-providers"></a>Tipos de provedores

Há quatro tipos principais de provedores: provedores MOF (clássico), provedores WPP, provedores baseados em manifesto e provedores TraceLogging. Você deverá usar um provedor baseado em manifesto ou um provedor TraceLogging se estiver escrevendo aplicativos para o Windows Vista ou posterior que não precisam dar suporte a sistemas herdado.

#### <a name="mof-classic-providers"></a>Provedores MOF (clássicos) :

-   Use as [funções RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [e TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar e gravar eventos.
-   Use classes MOF para definir eventos para que os consumidores saibam como consumi-los.
-   Pode ser habilitado por apenas uma sessão de rastreamento por vez.

#### <a name="wpp-providers"></a>Provedores WPP:

-   Use as [funções RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [e TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar e gravar eventos.
-   Os arquivos TMF associados (compilados em um .pdb de um binário) que contêm informações de decodificação inferidos da verificação de instrumentação WPP do pré-processador no código-fonte.
-   Pode ser habilitado por apenas uma sessão de rastreamento por vez.

#### <a name="manifest-based-providers"></a>Provedores baseados em manifesto:

-   Use [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para registrar e gravar eventos.
-   Use um manifesto para definir eventos para que os consumidores saibam como consumi-los.
-   Pode ser habilitado por até oito sessões de rastreamento simultaneamente.

#### <a name="tracelogging-providers"></a>[Provedores TraceLogging:](/windows/desktop/tracelogging/trace-logging-about)

-   Use [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) e [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para registrar e gravar eventos.
-   Use eventos autodescrevendo para que os próprios eventos contenham todas as informações necessárias para consumi-los.
-   Pode ser habilitado por até oito sessões de rastreamento simultaneamente.

Todos os provedores de eventos usam fundamentalmente a família de APIs de Rastreamento de Eventos ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para tecnologias herdada e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para as mais novas). Os provedores de eventos simplesmente diferem em quais tipos de campo eles armazenam em conteúdos de eventos e onde armazenam as informações de decodificação de eventos associadas.

## <a name="consumers"></a>Consumidores

Os consumidores são aplicativos que selecionam uma ou mais sessões de rastreamento de eventos como uma fonte de eventos. Um consumidor pode solicitar eventos de várias sessões de rastreamento de eventos simultaneamente; o sistema fornece os eventos em ordem cronológica. Os consumidores podem receber eventos armazenados em arquivos de log ou de sessões que entregam eventos em tempo real. Ao processar eventos, um consumidor pode especificar as horas de início e término e somente os eventos que ocorrem no período especificado serão entregues. 

Para obter mais informações, consulte [Consumindo eventos](consuming-events.md).

## <a name="missing-events"></a>Eventos ausentes

O Perfmon, o Diagnóstico do Sistema e outras ferramentas do sistema podem relatar eventos ausentes no Log de Eventos e indicar que as configurações do ETW (Rastreamento de Eventos para Windows) podem não ser ideais. Os eventos podem ser perdidos por vários motivos:

-   O tamanho total do evento é maior que 64K. Isso inclui o header ETW mais os dados ou o payload. Um usuário não tem controle sobre esses eventos ausentes, pois o tamanho do evento é configurado pelo aplicativo.

-   O tamanho do buffer ETW é menor que o tamanho total do evento. Um usuário não tem controle sobre esses eventos ausentes, pois o tamanho do evento é configurado pelo aplicativo registrando os eventos em log.

-   Para registro em log em tempo real, o consumidor em tempo real não está consumindo eventos rápido o suficiente ou não está presente completamente e, em seguida, o arquivo de backing está preenchendo. Isso poderá resultar se o serviço log de eventos for interrompido e iniciado quando os eventos estão sendo registrados. Um usuário não tem controle sobre esses eventos ausentes.

-   Ao registrar em log em um arquivo, o disco é muito lento para acompanhar a taxa de registro em log.

Por qualquer um desses motivos, informe esses problemas ao provedor do aplicativo ou serviço que está gerando os eventos. Esses problemas só podem ser corrigidos pelo desenvolvedor do aplicativo ou pelo serviço que registra os eventos em log. Se os eventos ausentes estão sendo relatados no Serviço de Log de Eventos, isso pode indicar um problema com a configuração do serviço de Log de Eventos. O usuário pode ter alguma capacidade limitada de aumentar o espaço máximo em disco a ser usado pelo Serviço de Log de Eventos, o que pode reduzir o número de eventos ausentes.

 

 
