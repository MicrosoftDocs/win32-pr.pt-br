---
description: A sessão de rastreamento de eventos do agente autologger registra eventos que ocorrem no início do processo de inicialização do sistema operacional.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurando e iniciando uma sessão do agente de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102035"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configurando e iniciando uma sessão do agente de log

A sessão de rastreamento de eventos do agente autologger registra eventos que ocorrem no início do processo de inicialização do sistema operacional. Aplicativos e drivers de dispositivo podem usar a sessão de agente de log autologger para capturar rastreamentos antes que o usuário faça logon. Observe que alguns drivers de dispositivo, como drivers de dispositivo de disco, não são carregados no momento em que a sessão do agente de log é iniciada.

O agente de log autologger difere do agente de log global das seguintes maneiras:

-   Você pode especificar uma ou mais sessões do autologger (o agente global era uma única sessão para a qual todos os eventos registraram).
-   O agente de log de eventos envia uma notificação de habilitação para os provedores quando a sessão é iniciada (o agente de log global não enviou uma notificação de habilitação aos provedores, portanto, os provedores precisavam contar com outros meios para saber se a sessão global de agente foi iniciada para iniciar eventos de log).
-   O agente de log autologger não dá suporte a logs de eventos de agente de kernel NT (consulte o membro **EnableFlags** das [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Para registrar eventos de agente do kernel NT, você deve usar o agente de log [global](configuring-and-starting-the-global-logger-session.md).

Para obter mais informações sobre a visualização de agente de log global, consulte [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md).

> [!Note]  
> O ETW dá suporte ao agente de log autologger no Windows Vista e posterior. Use o [agente de log global](configuring-and-starting-the-global-logger-session.md) em sistemas operacionais anteriores.

 

Você usa o registro para configurar a sessão do agente de log autologger. Adicione a seguinte chave do registro, se ainda não estiver presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Na chave **autologger** , crie uma chave para cada sessão do autologger que você deseja configurar, conforme mostrado no exemplo a seguir.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

Para cada sessão, crie uma chave para cada provedor que você deseja habilitar para a sessão. Use o GUID do provedor como a chave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

A tabela a seguir descreve os valores que você pode definir para cada sessão do autologger. Você deve ter privilégios de administrador para especificar esses valores de registro. O valor **inicial** e o **GUID** são os únicos valores necessários para iniciar a sessão do agente de log automática; todos os outros valores têm configurações padrão que serão usadas se o valor não estiver presente no registro. Normalmente, você deve usar os valores padrão. Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho de cada buffer, em quilobytes. Deve ser menor que um megabyte. O ETW usa o tamanho da memória física para calcular esse valor.<br/></td>
</tr>
<tr class="even">
<td><strong>Clocktype</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O temporizador a ser usado ao registrar em log o carimbo de data/hora para cada evento.
<ul>
<li>1 = valor do contador de desempenho (alta resolução)</li>
<li>2 = temporizador do sistema</li>
<li>3 = contador de ciclo de CPU</li>
</ul>
Para obter uma descrição de cada tipo de relógio, consulte o membro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> O valor padrão é 1 (valor do contador de desempenho) no Windows Vista e posterior. Antes do Windows Vista, o valor padrão é 2 (temporizador do sistema).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para desabilitar a persistência em tempo real, defina esse valor como 1. O padrão é 0 (habilitado) para sessões em tempo real.<br/> Se a persistência em tempo real estiver habilitada, os eventos em tempo real que não foram entregues no momento em que o computador foi desligado serão persistidos. Os eventos serão então entregues ao consumidor na próxima vez que o consumidor se conectar à sessão. <br/></td>
</tr>
<tr class="even">
<td><strong>Contador de filecounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Não defina nem modifique esse valor. Esse valor é o número de série usado para incrementar o nome do arquivo de log se <strong>FileMax</strong> for especificado. Se o valor não for válido, 1 será assumido.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>O caminho totalmente qualificado do arquivo de log. O caminho para esse arquivo deve existir. O arquivo de log é um arquivo de log sequencial. O caminho é limitado a 1024 caracteres.<br/> Se <strong>filename</strong> não for especificado, os eventos serão gravados em%SystemRoot%\System32\LogFiles\WMI \& lt; SessionName &gt; . etl. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de instâncias do arquivo de log que o ETW cria. Se o arquivo de log especificado em <strong>filename</strong> existir, o ETW acrescentará o valor <strong>filecounterer</strong> ao nome do arquivo. Por exemplo, se o nome do arquivo de log padrão for usado, o formulário será%SystemRoot%\System32\LogFiles\WMI \& lt; SessionName &gt; . etl. NNNN. <br/> Na primeira vez que o computador é iniciado, o nome do arquivo é &lt; SessionName &gt; . etl. 0001, a segunda vez que o nome do arquivo é &lt; SessionName &gt; . etl. 0002 e assim por diante. Se <strong>FileMax</strong> for 3, na quarta reinicialização do computador, o ETW redefinirá o contador como 1 e substituirá &lt; SessionName &gt; . etl. 0001, se existir.<br/> O número máximo de instâncias do arquivo de log com suporte é 16.<br/> Não use esse recurso com o modo de arquivo de log <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Com que frequência, em segundos, os buffers de rastreamento são liberados forçosamente. O tempo de liberação mínimo é de 1 segundo. Essa liberação forçada é além da liberação automática que ocorre quando um buffer está cheio e quando a sessão de rastreamento é interrompida. <br/> Para o caso de um agente em tempo real, um valor igual a zero (o valor padrão) significa que o tempo de liberação será definido como 1 segundo. Um agente de log em tempo real é quando <strong>LOGFILEMODE</strong> é definido como <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> O valor padrão é 0. Por padrão, os buffers são liberados somente quando estão cheios. <br/></td>
</tr>
<tr class="even">
<td><strong>Volume</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Uma cadeia de caracteres que contém um GUID que identifica exclusivamente a sessão. Esse valor é necessário.</td>
</tr>
<tr class="odd">
<td><strong>LogFilemode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifique um ou mais modos de log. Para obter os valores possíveis, consulte <a href="logging-mode-constants.md">constantes do modo de log</a>. O padrão é <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Em vez de gravar em um arquivo de log, você pode especificar <strong>EVENT_TRACE_BUFFERING_MODE</strong> ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> A especificação de <strong>EVENT_TRACE_BUFFERING_MODE</strong> evita o custo de liberação do conteúdo da sessão para o disco quando o sistema de arquivos fica disponível. <br/> Observe que o uso de <strong>EVENT_TRACE_BUFFERING_MODE</strong> fará com que o sistema ignore o valor <strong>MaximumBuffers</strong> , pois o tamanho do buffer é, em vez disso, o produto de <strong>MinimumBuffers</strong> e <strong>BufferSize</strong>.<br/> As sessões do autologger não dão suporte ao modo de log de <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .<br/> Se <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> for especificado, <strong>BufferSize</strong> deverá ser fornecido explicitamente e deverá ser o mesmo no agente de log e no arquivo que está sendo anexado.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O tamanho máximo do arquivo de log, em megabytes. A sessão é fechada quando o tamanho máximo é atingido, a menos que você esteja no modo de arquivo de log circular. Para especificar sem limite, defina valor como 0. O padrão é 100 MB, se não estiver definido. O comportamento que ocorre quando o tamanho máximo do arquivo é atingido depende do valor de <strong>LOGFILEMODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número máximo de buffers a serem alocados. Normalmente, esse valor é o número mínimo de buffers, mais vinte. O ETW usa o tamanho do buffer e o tamanho da memória física para calcular esse valor. Esse valor deve ser maior ou igual ao valor de <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O número mínimo de buffers a serem alocados na inicialização. O número mínimo de buffers que você pode especificar é de dois buffers por processador. Por exemplo, em um único computador de processador, o número mínimo de buffers é dois.<br/></td>
</tr>
<tr class="odd">
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para que a sessão do autologger seja iniciada na próxima vez que o computador for reiniciado, defina esse valor como 1; caso contrário, defina esse valor como 0.<br/></td>
</tr>
<tr class="even">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>O status de inicialização do agente de log autologger. Se o agente de log automática não for iniciado, o valor dessa chave será o código de erro Win32 apropriado. Se o agente de log autologger foi iniciado com êxito, o valor dessa chave será <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

A tabela a seguir descreve os valores que você pode definir para cada provedor que você deseja habilitar na sua sessão. Você deve ter privilégios de administrador para especificar esses valores de registro. Se você especificar um valor que o ETW não tem suporte, o ETW substituirá o valor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Enabled</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Determina se o provedor está habilitado. Para habilitar o provedor, defina esse valor como 1. Para desabilitar o provedor, defina esse valor como 0. O padrão é 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido pelo provedor que especifica a classe de eventos para os quais o provedor gera eventos. Para obter detalhes, consulte o parâmetro <em>EnableFlags</em> da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> . Especifique esse nome de valor se o provedor não oferecer suporte a <strong>MatchAnyKeyword</strong> ou <strong>MatchAllKeyword</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido pelo provedor que especifica o nível de detalhe incluído no evento. Por exemplo, você pode usar esse valor para indicar o nível de severidade dos eventos (informativo, aviso, erro) que o provedor gera. Para obter uma lista de níveis predefinidos, consulte o parâmetro <em>Level</em> da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>Habilitada</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Use esse valor para incluir um ou mais dos seguintes itens no arquivo de log:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = incluir nos dados estendidos o Sid (identificador de segurança) do usuário.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = incluir nos dados estendidos o identificador de sessão de terminal.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = incluir nos dados estendidos um rastreamento de pilha de chamadas para eventos escritos usando <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos os eventos que não têm uma palavra-chave diferente de zero especificada.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica que essa chamada para <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> deve habilitar um <a href="provider-traits.md">grupo de provedores</a> em vez de um provedor de eventos individual.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = incluir a chave de início do processo nos dados estendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = incluir a chave de evento nos dados estendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos os eventos que estão marcados como um evento InPrivate ou que vêm de um processo marcado como InPrivate.</li>
</ul>
Para obter mais informações sobre esses itens, consulte a <strong>habilitação</strong> da estrutura de <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Bitmask de palavras-chave que determinam a categoria de eventos que você deseja que o provedor escreva. O provedor gravará o evento se qualquer um dos bits de palavra-chave do evento corresponder a qualquer um dos bits definidos nessa máscara. Para especificar que o provedor grava todos os eventos, defina esse valor como zero. Para obter um exemplo, consulte a seção comentários da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Esse bitmask é opcional. Essa máscara restringe ainda mais a categoria de eventos que você deseja que o provedor escreva. Se a palavra-chave do evento atender à condição <em>MatchAnyKeyword</em> , o provedor gravará o evento somente se todos os bits nessa máscara existirem na palavra-chave do evento. Essa máscara não será usada se <em>MatchAnyKeyword</em> for zero. Para obter um exemplo, consulte a seção comentários da função <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
</tbody>
</table>



 

Depois que o registro tiver sido modificado, a sessão do agente de log automática será iniciada na próxima vez em que o computador for reiniciado. A sessão do autologger chama a função [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar os provedores.

As sessões do autologger aumentam o tempo de inicialização do sistema e devem ser usadas com moderação. Os serviços que desejam capturar informações durante o processo de inicialização devem considerar a adição da lógica do controlador a si só, em vez de usar a sessão do agente de log.

Para interromper uma sessão do agente de log, chame a função [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) . O nome da sessão que você passa para a função é o nome da chave do registro que você usou para definir a sessão no registro.

No Windows 8.1, o Windows Server 2012 R2 e posterior, o conteúdo do evento, o escopo e os filtros de exame de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar as condições específicas em uma sessão de agente. Para obter mais informações sobre filtros de carga de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e as estruturas [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **Enable \_ trace \_**, **\_ \_ descritor de filtro de evento** e conteúdo de filtro de carga.

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão de agente de log particular, consulte [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do agente do NT kernel, consulte [Configurando e iniciando a sessão do agente de log do NT](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Habilitar \_ parâmetros de rastreamento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
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
