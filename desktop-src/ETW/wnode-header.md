---
description: A \_ estrutura de cabeçalho WNODE é um membro da estrutura de propriedades de rastreamento de eventos \_ \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Estrutura de WNODE_HEADER (Wmistr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "104968762"
---
# <a name="wnode_header-structure"></a>\_Estrutura de cabeçalho WNODE

A estrutura de **\_ cabeçalho WNODE** é um membro da estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**BufferSize**
</dt> <dd>

Tamanho total da memória alocada, em bytes, para as propriedades da sessão de rastreamento de eventos. O tamanho da memória deve incluir o espaço para a estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , além da cadeia de caracteres do nome da sessão e da cadeia de caracteres do nome do arquivo de log que seguem a estrutura na memória.

</dd> <dt>

**ProviderId**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Na saída, o identificador para a sessão de rastreamento de eventos.

</dd> <dt>

**Versão**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**Vinculação**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**KernelHandle**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**Estampa**
</dt> <dd>

Hora em que as informações nesta estrutura foram atualizadas, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.

</dd> <dt>

**Volume**
</dt> <dd>

O GUID que você define para a sessão.

Para uma sessão do NT kernel Logger, defina esse membro como **SystemTraceControlGuid**.

Se esse membro for definido como **SystemTraceControlGuid** ou **GlobalLoggerGuid**, o agente será um agente de log do sistema.

Para uma sessão de agente de log particular, defina esse membro como o GUID do provedor que você vai habilitar para a sessão.

Se você iniciar uma sessão que não seja um agente de log de kernel ou uma sessão de agente particular, não será necessário especificar um GUID de sessão. Se você não especificar um GUID, o ETW criará um para você. Você precisará especificar um GUID de sessão somente se quiser alterar as permissões padrão associadas a uma sessão específica. Para obter detalhes, consulte a função EventAccessControl.

Não é possível iniciar mais de uma sessão com o mesmo GUID de sessão.

**Antes do Windows Vista:** Você pode iniciar mais de uma sessão com o mesmo GUID de sessão.

</dd> <dt>

**ClientContext**
</dt> <dd>

Resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento. O padrão é o contador de desempenho de consulta (QPC).

**Antes do Windows Vista:** O padrão é hora do sistema.

**Antes do Windows 10, versão 1703:** Não mais do que 2 tipos de relógio distintos podem ser usados simultaneamente por qualquer agente de log do sistema.

**A partir do Windows 10, versão 1703:** A restrição de tipo de relógio foi removida. Todos os três tipos de relógio agora podem ser usados simultaneamente por agentes de log do sistema.

Você pode especificar um dos valores a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>1</dt> </dl></td>
<td>Contador de desempenho de consulta (QPC). O contador QPC fornece um carimbo de data/hora de alta resolução que não é afetado pelos ajustes no relógio do sistema. O carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API QueryPerformanceCounter. Para obter mais informações sobre as características desse carimbo de data/hora, consulte <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">adquirindo carimbos de data/hora de alta resolução</a>.<br/> Você deve usar essa resolução se tiver taxas de eventos altas ou se o consumidor mesclar eventos de buffers diferentes. Nesses casos, a precisão e a estabilidade do carimbo de data/hora do QPC permitem maior precisão na ordenação dos eventos de diferentes buffers. No entanto, o carimbo de data/hora de QPC não refletirá as atualizações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de hora QPC no rastreamento continuarão a refletir o tempo como se nenhuma atualização tivesse ocorrido.<br/> Para determinar a resolução, use o membro <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.<br/> Para converter o carimbo de data/hora de um evento em unidades 100-NS, use a seguinte fórmula de conversão: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart * 10000000,0/logfileHeader. PerfFreq. QuadPart<br/> Observe que, em computadores mais antigos, o carimbo de data/hora pode não ser preciso, pois o contador às vezes pula para frente devido a erros de hardware.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Hora do sistema. A hora do sistema fornece um carimbo de data/hora que controla as alterações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de hora do sistema no rastreamento também serão encaminhados para corresponder à nova configuração do relógio do sistema. <br/>
<ul>
<li>Em sistemas anteriores ao Windows 10, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimeAsFileTime.</li>
<li>No Windows 10 ou posterior, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimePreciseAsFileTime.</li>
</ul>
Antes do Windows 10, a resolução desse carimbo de data/hora foi a resolução de um tique de relógio do sistema, conforme indicado pelo membro TimerResolution de TRACE_LOGFILE_HEADER. A partir do Windows 10, a resolução desse carimbo de data/hora é a resolução do contador de desempenho, conforme indicado pelo membro PerfFreq de TRACE_LOGFILE_HEADER.<br/> Para converter o carimbo de data/hora de um evento em unidades 100-NS, use a seguinte fórmula de conversão: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart<br/> Observe que quando os eventos são capturados em um sistema que executa um so anterior ao Windows 10, se o volume de eventos for alto, a resolução do tempo do sistema poderá não ser suficiente para determinar a sequência de eventos. Nesse caso, um conjunto de eventos terá o mesmo carimbo de data/hora, mas a ordem na qual o ETW entrega os eventos pode não estar correta. A partir do Windows 10, o carimbo de data/hora é capturado com precisão adicional, embora alguma instabilidade ainda possa ocorrer nos casos em que o relógio do sistema foi ajustado enquanto o rastreamento estava sendo capturado.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>Beta</dt> </dl></td>
<td>Contador de ciclo de CPU. O contador de CPU fornece o carimbo de data e hora de resolução mais alto e consome menos recursos para recuperar. No entanto, o contador de CPU não é confiável e não deve ser usado na produção. Por exemplo, em alguns computadores, os temporizadores mudarão a frequência devido a alterações térmicas e de energia, além de serem interrompidos em alguns Estados.<br/> Para determinar a resolução, use o membro <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.<br/> Se o hardware não oferecer suporte a esse tipo de relógio, o ETW usará a hora do sistema.<br/> <strong>Windows Server 2003, Windows XP com SP1 e Windows XP:</strong> Esse valor não tem suporte, foi introduzido no Windows Server 2003 com SP1 e no Windows XP com SP2.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** Não há suporte para o membro **ClientContext** .

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Deve conter **\_ \_ \_ GUID rastreado do sinalizador WNODE** para indicar que a estrutura contém informações de rastreamento de eventos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Certifique-se de inicializar a memória dessa estrutura para zero antes de definir os membros.

Para converter um carimbo de data/hora ETW em um FILETIME, use o seguinte procedimento:

<dl> 1. Para cada arquivo de sessão ou de log sendo processado (ou seja, para cada log de rastreamento de evento \_ \_ ), verifique o campo logfile. ProcessTraceMode para determinar se o \_ sinalizador de carimbo de \_ data/hora bruto do modo de rastreamento do processo \_ \_ está definido. Por padrão, esse sinalizador não é definido. Se esse sinalizador não for definido, o tempo de execução do ETW converterá automaticamente o carimbo de data/hora de cada registro de evento \_ em um FILETIME antes de enviar o registro de evento \_ para a função EventRecordCallback, portanto, nenhum processamento adicional será necessário. As etapas a seguir só devem ser usadas se o rastreamento estiver sendo processado com o \_ \_ sinalizador de \_ carimbo de \_ data/hora bruto do modo de rastreamento do processo.  
2. Para cada arquivo de sessão ou de log sendo processado (ou seja, para cada log de rastreamento de evento \_ \_ ), verifique o campo logfile. LogfileHeader. ReservedFlags para determinar a escala de carimbo de data/hora do arquivo de log. Com base no valor de ReservedFlags, siga uma destas etapas para determinar o valor a ser usado para timeStampScale nas etapas restantes: <dl> a. Se ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;  
b. Se ReservedFlags = = 2 (hora do sistema): timeStampScale duplo = 1,0;  
Observe que as etapas restantes são desnecessárias para eventos que usam a hora do sistema, pois os eventos já fornecem seus carimbos de data/hora em unidades FILETIME. As etapas restantes funcionarão, mas serão desnecessárias e apresentarão um pequeno erro de arredondamento.  
c. Se ReservedFlags = = 3 (contador de ciclo de CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                   |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                         |
| parâmetro<br/>                   | <dl> <dt>Wmistr. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**\_Propriedades de rastreamento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**\_inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
