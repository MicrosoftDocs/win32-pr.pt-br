---
description: As constantes a seguir representam os modos de log possíveis para uma sessão de rastreamento de eventos.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Constantes do modo de log
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967469"
---
# <a name="logging-mode-constants"></a>Constantes do modo de log

As constantes a seguir representam os modos de log possíveis para uma sessão de rastreamento de eventos.

As constantes são usadas nos membros **LOGFILEMODE** de [**log de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) e estruturas de cabeçalho do arquivo de [**\_ log \_ de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) . Essas constantes são definidas no arquivo de cabeçalho *Evntrace. h* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>O mesmo que <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> sem o tamanho de arquivo máximo especificado.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Grava eventos em um arquivo de log sequencialmente; para quando o arquivo atinge seu tamanho máximo. Não use com <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> ou <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Grava eventos em um arquivo de log. Depois que o arquivo atingir o tamanho máximo, os eventos mais antigos serão substituídos pelos eventos de entrada. Observe que o conteúdo do arquivo de log circular pode parecer fora de ordem em computadores com vários processadores.<br/> Não use com <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Anexa eventos a um arquivo de log sequencial existente. Se o arquivo não existir, ele será criado. Use somente se você especificar a <a href="wnode-header.md"><strong>hora do sistema</strong></a> para a resolução do relógio, caso contrário, <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>ProcessTrace</strong></a> retornará eventos com carimbos de data/hora incorretos. Ao usar <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, os valores de <strong>BufferSize</strong>, <strong>NumberOfProcessors</strong>e <strong>clocktype</strong> devem ser fornecidos explicitamente e devem ser os mesmos no agente de log e no arquivo que está sendo anexado.<br/> Não use com <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Alterna automaticamente para um novo arquivo de log quando o arquivo atinge o tamanho máximo. O membro <strong>MaximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> deve ser definido. O nome de arquivo especificado deve ser uma cadeia de caracteres formatada (por exemplo, a cadeia de caracteres contém um% d, como c:\test%d.ETL). Cada vez que um novo arquivo é criado, um contador é incrementado e seu valor é usado, a cadeia de caracteres formatada é atualizada e a cadeia de caracteres resultante é usada como o nome do arquivo.<br/> Esta opção não é permitida para sessões de rastreamento de eventos particulares e não deve ser usada para sessões de agente de log NT.<br/> Não use com <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> ou <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Reserva <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a> bytes de espaço em disco para o arquivo de log com antecedência. O arquivo ocupa todo o espaço durante o registro em log para arquivos de log circulares e sequenciais. Quando você interrompe a sessão, o arquivo de log é reduzido para o tamanho necessário. Você deve definir <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a>.<br/> Você não pode usar o modo para sessões de rastreamento de eventos particulares.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>Não é possível interromper a sessão de registro em log. Esse modo só tem suporte do autologger. essa opção tem suporte no Windows Vista e posterior.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0X00000080)</td>
<td>Restringe quem pode registrar eventos na sessão para aqueles com <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> permissão. Essa opção tem suporte no Windows Vista e versões posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Entrega os eventos aos consumidores em tempo real. Os eventos são entregues quando os buffers são liberados, não no momento em que o provedor grava o evento. Você não deve habilitar o modo em tempo real se não houver consumidores para consumir os eventos, pois as chamadas para eventos de log eventualmente falharão quando os buffers ficarem cheios. Antes do Windows Vista, se os eventos não estivessem sendo consumidos, os eventos foram descartados. Não especifique mais de um consumidor em tempo real em um processo no Windows XP orWindows Server 2003. Em vez disso, faça com que um thread consuma eventos e distribua os eventos para outras pessoas.<br/> <strong>Antes do Windows Vista:</strong> Você não deve usar o modo em tempo real porque a taxa de eventos com suporte é muito menor do que a leitura do arquivo de log (os eventos podem ser descartados). Além disso, a ordem do evento não é garantida em computadores com vários processadores. O modo em tempo real é mais adequado para eventos de baixo tráfego e tipo de notificação.<br/> <br/> Você pode combinar esse modo com outros modos de arquivo de log; no entanto, não use esse modo com EVENT_TRACE_PRIVATE_LOGGER_MODE. Observe que, se você combinar esse modo com outros modos de arquivo de log, os buffers serão liberados uma vez a cada segundo, resultando em buffers parcialmente preenchidos sendo gravados no arquivo de log. Por exemplo, se você usar buffers de 64K e sua taxa de registro em log for 1 evento a cada segundo, o serviço gravará 64K/segundo em seu arquivo de log.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Esse modo é usado para atrasar a abertura do arquivo de log até que ocorra um evento. <br/>
<blockquote>
<strong>Observação</strong>:<br />
No Windows Vista ou posterior, esse modo não é aplicável não deve ser usado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Esse modo grava eventos em um buffer de memória circular. Eventos gravados além do tamanho total do buffer removem os eventos mais antigos ainda restantes no buffer. O tamanho desse buffer de memória é o produto de <strong>MinimumBuffers</strong> e <strong>BufferSize</strong> (consulte <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). Como consequência dessa fórmula, qualquer buffer que usa <strong>EVENT_TRACE_BUFFERING_MODE</strong> ignorará o valor <strong>MaximumBuffers</strong> .<br/> Os eventos não são gravados em um arquivo de log ou entregues em tempo real e o ETW não libera os buffers. Para obter um instantâneo do buffer, chame a função <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>FlushTrace</strong></a> .<br/> Esse modo é particularmente útil para depurar drivers de dispositivo em conjunto com a capacidade de exibir o conteúdo de buffers na memória com a extensão do depurador de kernel <a href="/windows-hardware/drivers/devtest/trace-session">WMITrace</a> .<br/> Não use com <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Cria uma sessão de rastreamento de eventos no modo de usuário que é executada no mesmo processo que seu provedor de rastreamento de eventos. A memória para buffers vem da memória do processo. Processos que não exigem dados do kernel podem eliminar a sobrecarga associada a transições do modo kernel usando uma sessão de rastreamento de eventos particular.<br/> Se o provedor for registrado por vários processos, o ETW acrescentará o identificador do processo ao nome do arquivo de log para criar um nome de arquivo de log exclusivo. Por exemplo, se o controlador especificar os nomes de arquivo de log como c:\mylogs\myprivatelog.ETL, o ETW criará o arquivo de log como c:\mylogs\ myprivatelog.etl_nnnn, em que nnnn é o identificador do processo. O identificador do processo não é acrescentado ao primeiro processo que registra o provedor, ele é anexado apenas aos processos subsequentes que registram o provedor.<br/> As sessões de rastreamento de eventos particulares têm as seguintes limitações:<br/>
<ul>
<li>Uma sessão privada pode registrar eventos somente para os threads do processo em que ele está sendo executado.</li>
<li>Pode haver até oito sessões privadas por processo.</li>
<li>As sessões privadas não podem ser usadas com a entrega em tempo real.</li>
<li>Os eventos gerados por uma sessão privada não incluem tempo de execução para instruções de modo kernel versus modo de usuário, ou detalhes no nível de thread do tempo de CPU usado.</li>
</ul>
Filtros de ID de processo e filtros de nome de executável agora podem ser passados para APIs de controle de sessão quando os agentes particulares do sistema são iniciados. Para obter os melhores resultados em cenários de processo cruzado, os mesmos filtros devem ser passados para cada operação de controle durante a sessão, incluindo chamadas Enable/diasble do provedor. Observe que os filtros têm o mesmo formato que os consumidos por <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>. <br/> Você pode usar esse modo em conjunto com o modo de <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> .<br/> <strong>Antes do Windows 10, versão 1703:</strong> Somente o LocalSystem, o administrador e os usuários no grupo de administradores que são executados em um processo com privilégios elevados podem criar uma sessão privada. Se você incluir o sinalizador <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> , qualquer usuário poderá criar uma sessão privada em processo. Além disso, nas versões anteriores do Windows, só pode haver uma sessão privada por processo (a menos que o modo de EVENT_TRACE_PRIVATE_IN_PROC também seja especificado; nesse caso, você pode criar até três sessões privadas em processo). <br/> <strong>Antes do Windows Vista:</strong> Os usuários no grupo usuários do log de desempenho também podem criar uma sessão privada.<br/> <br/> Não use com EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>Antes do Windows 7 e do Windows Server 2008 R2:</strong> Não use com EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Essa opção adiciona um cabeçalho ao arquivo de log.<br/>
<blockquote>
<strong>Observação</strong>:<br />
No Windows Vista ou posterior, esse modo não é aplicável não deve ser usado.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Use quilobytes como a unidade de medida para especificar o tamanho de um arquivo. A unidade de medida padrão é megabytes. Esse modo se aplica ao valor de registro <strong>MaxFileSize</strong> para uma sessão do <a href="configuring-and-starting-an-autologger-session.md">autologger</a> e o membro <strong>MaximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Essa opção tem suporte no Windows Vista e versões posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Usa números de sequência que são exclusivos entre sessões de rastreamento de eventos. Esse modo se aplica somente aos eventos registrados usando a função <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Para obter mais informações, consulte <strong>TraceMessage</strong> para obter detalhes de uso.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> e <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> são mutuamente exclusivos.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Usa números de sequência exclusivos somente para uma sessão de rastreamento de eventos individual. Esse modo se aplica somente aos eventos registrados usando a função <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Para obter mais informações, consulte <strong>TraceMessage</strong> para obter detalhes de uso.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> e <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> são mutuamente exclusivos.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000)</td>
<td>Registra o evento sem incluir <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>.
<blockquote>
<strong>Observação</strong>:<br />
Esse modo não deve ser usado. Ele é reservado para uso interno.
</blockquote>
<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Use em conjunto com o modo de <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> para iniciar uma sessão privada. Esse modo impõe que apenas o processo que registrou o GUID do provedor possa iniciar a sessão do agente com esse GUID.<br/> Você pode criar até três sessões privadas em processo por processo.<br/> Essa opção tem suporte no Windows Vista e versões posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Essa opção é usada para sinalizar o rastreamento de heap e seção crítica. Essa opção tem suporte no Windows Vista e versões posteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Essa opção interrompe o registro em log no desligamento híbrido. Se nenhum <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ou <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> for especificado, o ETW escolherá um padrão com base no fato de o chamador ser proveniente da sessão 0 ou não. Essa opção tem suporte no Windows 8 e no Windows Server 2012. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Essa opção continua registrando em log o desligamento híbrido. Se nenhum <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ou <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> for especificado, o ETW escolherá um padrão com base no fato de o chamador ser proveniente da sessão 0 ou não. Essa opção tem suporte no Windows 8 e no Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Usa memória paginável. Essa configuração é recomendada para que os eventos não usem a memória não paginável. Os buffers não paginados usam memória não paginável para o espaço do buffer. Como os buffers não paginados nunca são paginados, uma sessão de registro em log é bem executada. O uso de buffers paginável é menos intensivo de recursos.<br/> Provedores de modo kernel e agentes do sistema não podem registrar eventos em sessões que especificam esse modo de log.<br/> Esse modo será ignorado se <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> estiver definido.<br/> Você não pode usar esse modo com o agente de log de kernel do NT.<br/> <strong>Windows 2000:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Esta opção receberá eventos de SystemTraceProvider. Se o parâmetro <strong>LOGFILEMODE</strong> de <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>StartTrace</strong></a><em>Properties</em> incluir esse sinalizador, o agente de log será um agente de log do sistema. Essa opção tem suporte no Windows 8 e no Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Indica que uma sessão de registro em log não deve ser afetada por falhas de <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> em outras sessões. Sem esse sinalizador, se um evento não puder ser publicado em uma das sessões para as quais um provedor está habilitado, o evento não será publicado em nenhuma das sessões. Quando esse sinalizador é definido, uma falha ao gravar um evento em uma sessão não fará com que a função <strong>EventWrite</strong> retorne um código de erro em outras sessões. <br/> Não use com <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Essa opção tem suporte em Windows 8.1, Windows Server 2012 R2 e posterior.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Grava eventos que foram registrados em processadores diferentes em um buffer comum. O uso desse modo pode eliminar o problema dos eventos que aparecem fora de ordem quando os eventos estão sendo publicados em processadores diferentes usando a hora do sistema. Esse modo também pode eliminar o problema com logs circulares que aparecem para descartar eventos em vários computadores de processador.<br/> Se você não usar esse modo e usar a hora do sistema, os eventos poderão aparecer fora de ordem em vários computadores de processador. Isso ocorre porque os buffers ETW são associados a um processador em vez de um thread. Como resultado, se um thread for alternado de uma CPU para outra, o buffer associado à última CPU poderá ser liberado para o disco antes do associado à CPU anterior.<br/> Se você espera um alto volume de eventos (por exemplo, mais de 1.000 eventos por segundo), não deve usar esse modo.<br/> Observe que o número do processador não está incluído no evento.<br/> Essa opção tem suporte no Windows 7, Windows Server 2008 R2 e posterior.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Essa opção adiciona buffers ETW a despejos de triagem. Essa opção tem suporte no Windows 8 e no Windows Server 2012. <br/></td>
</tr>
</tbody>
</table>
