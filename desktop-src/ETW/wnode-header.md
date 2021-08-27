---
description: A estrutura DE \_ HEADER WNODE é um membro da estrutura EVENT \_ TRACE \_ PROPERTIES.
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER estrutura (Wmistr.h)
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
ms.openlocfilehash: 93cecb900b0c62084a3b5ea4e4a7789575c20c27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480682"
---
# <a name="wnode_header-structure"></a>Estrutura de \_ HEADER WNODE

A **estrutura DE \_ HEADER WNODE** é um membro da estrutura EVENT TRACE [**\_ \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

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

Tamanho total da memória alocada, em bytes, para as propriedades da sessão de rastreamento de eventos. O tamanho da memória deve incluir a sala para a estrutura [**EVENT \_ TRACE \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) mais a cadeia de caracteres de nome de sessão e a cadeia de caracteres de nome de arquivo de log que seguem a estrutura na memória.

</dd> <dt>

**Providerid**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Na saída, o alça para a sessão de rastreamento de eventos.

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

**Timestamp**
</dt> <dd>

Hora em que as informações nessa estrutura foram atualizadas, em intervalos de 100 nanossegundos desde a meia-noite de 1º de janeiro de 1601.

</dd> <dt>

**Guid**
</dt> <dd>

O GUID que você define para a sessão.

Para uma sessão do NT Kernel Logger, de definido esse membro **como SystemTraceControlGuid**.

Se esse membro for definido como **SystemTraceControlGuid** ou **GlobalLoggerGuid,** o logger será um logger do sistema.

Para uma sessão de logger privado, de definir esse membro como o GUID do provedor que você vai habilitar para a sessão.

Se você iniciar uma sessão que não seja um logger de kernel ou sessão de logger privado, não será necessário especificar um GUID de sessão. Se você não especificar um GUID, o ETW criará um para você. Você precisará especificar um GUID de sessão somente se quiser alterar as permissões padrão associadas a uma sessão específica. Para obter detalhes, consulte a função EventAccessControl.

Não é possível iniciar mais de uma sessão com o mesmo GUID de sessão.

**Antes do Windows Vista:** Você pode iniciar mais de uma sessão com o mesmo GUID de sessão.

</dd> <dt>

**ClientContext**
</dt> <dd>

Resolução do relógio a ser usada ao registrar o carimbo de data/hora para cada evento. O padrão é QPC (Contador de desempenho de consulta).

**Antes do Windows Vista:** O padrão é a hora do sistema.

**Antes da Windows 10, versão 1703:** Não mais do que dois tipos de relógio distintos podem ser usados simultaneamente por qualquer logger do sistema.

**Começando com Windows 10, versão 1703:** A restrição de tipo de relógio foi removida. Agora, todos os três tipos de relógio podem ser usados simultaneamente por ativos do sistema.

Você pode especificar um dos valores a seguir.




| Valor | Significado | 
|-------|---------|
| <dl><dt>1</dt></dl> | QPC (contador de desempenho de consulta). O contador QPC fornece um carimbo de data/hora de alta resolução que não é afetado por ajustes no relógio do sistema. O carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API QueryPerformanceCounter. Para obter mais informações sobre as características desse carimbo de data/hora, consulte <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Adquirindo carimbos de data/hora de alta resolução.</a><br /> Você deverá usar essa resolução se tiver altas taxas de eventos ou se o consumidor mesclar eventos de buffers diferentes. Nesses casos, a precisão e a estabilidade do carimbo de data/hora QPC permitem uma melhor precisão na ordenação dos eventos de buffers diferentes. No entanto, o carimbo de data/hora QPC não refletirá as atualizações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de data/hora QPC no rastreamento continuarão a refletir o tempo como se nenhuma atualização tivesse ocorrido.<br /> Para determinar a resolução, use <strong>o membro PerfFreq</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.<br /> Para converter o carimbo de data/hora de um evento em unidades de 100 ns, use a seguinte fórmula de conversão: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart<br /> Observe que, em computadores mais antigos, o carimbo de data/hora pode não ser preciso porque o contador às vezes ignora o encaminhamento devido a erros de hardware.<br /> | 
| <dl><dt>2</dt></dl> | Hora do sistema. A hora do sistema fornece um carimbo de data/hora que acompanha as alterações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de data/hora do sistema no rastreamento também avançarão para corresponder à nova configuração do relógio do sistema. <br /><ul><li>Em sistemas anteriores Windows 10, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimeAsFileTime.</li><li>No Windows 10 ou posterior, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimePreciseAsFileTime.</li></ul>Antes Windows 10, a resolução desse carimbo de data/hora era a resolução de um tique do relógio do sistema, conforme indicado pelo membro TimerResolution do TRACE_LOGFILE_HEADER. Começando com Windows 10, a resolução desse carimbo de data/hora é a resolução do contador de desempenho, conforme indicado pelo membro PerfFreq do TRACE_LOGFILE_HEADER.<br /> Para converter o carimbo de data/hora de um evento em unidades de 100 ns, use a seguinte fórmula de conversão: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart<br /> Observe que quando os eventos são capturados em um sistema que executa um sistema operacional antes do Windows 10, se o volume de eventos for alto, a resolução do tempo do sistema poderá não ser suficiente para determinar a sequência de eventos. Nesse caso, um conjunto de eventos terá o mesmo carimbo de data/hora, mas a ordem na qual o ETW entrega os eventos pode não estar correta. Começando com Windows 10, o carimbo de data/hora é capturado com precisão adicional, embora algumas instabilidades ainda possam ocorrer em casos em que o relógio do sistema foi ajustado enquanto o rastreamento estava sendo capturado.<br /> | 
| <dl><dt>3</dt></dl> | Contador de ciclo de CPU. O contador de CPU fornece o carimbo de data/hora de resolução mais alta e é o menos intensivo de recursos a ser recuperado. No entanto, o contador de CPU não é confiável e não deve ser usado em produção. Por exemplo, em alguns computadores, os temporizadores alterarão a frequência devido a alterações térmicas e de energia, além de parar em alguns estados.<br /> Para determinar a resolução, use o <strong>membro CpuSpeedInMHz</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.<br /> Se o hardware não dá suporte a esse tipo de relógio, o ETW usa a hora do sistema.<br /><strong>Windows Server 2003, Windows XP com SP1 e Windows XP:</strong> Esse valor não tem suporte, ele foi introduzido no Windows Server 2003 com SP1 e Windows XP com SP2.<br /> | 




 

**Windows 2000:** Não há suporte para o membro **ClientContext.**

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Deve conter GUID **\_ \_ TRACED \_ do SINALIZADOR WNODE** para indicar que a estrutura contém informações de rastreamento de eventos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Certifique-se de inicializar a memória dessa estrutura como zero antes de definir os membros.

Para converter um timestamp ETW em um FILETIME, use o seguinte procedimento:

<dl> 1. Para cada sessão ou arquivo de log que está sendo processado (ou seja, para cada LOGFILE DE RASTREAMENTO DE EVENTOS), verifique o \_ campo logFile.ProcessTraceMode para determinar se o sinalizador \_ PROCESS TRACE MODE RAW \_ \_ \_ \_ TIMESTAMP está definido. Por padrão, esse sinalizador não está definido. Se esse sinalizador não estiver definido, o runtime do ETW converterá automaticamente o timestamp de cada REGISTRO DE EVENTO em um FILETIME antes de enviar o REGISTRO DE EVENTOS para \_ a função EventRecordCallback, portanto, nenhum processamento adicional será \_ necessário. As etapas a seguir só deverão ser usadas se o rastreamento estiver sendo processado com o sinalizador PROCESS \_ TRACE \_ MODE RAW \_ \_ TIMESTAMP definido.  
2. Para cada sessão ou arquivo de log que está sendo processado (ou seja, para cada LOGFILE DE RASTREAMENTO DE EVENTOS), verifique o \_ campo logFile.LogfileHeader.ReservedFlags para determinar a escala de carimbo de data/hora para o arquivo \_ de log. Com base no valor de ReservedFlags, siga uma destas etapas para determinar o valor a ser usado para timeStampScale nas etapas restantes: <dl> a. Se ReservedFlags == 1 (QPC): double timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;  
b. Se ReservedFlags == 2 (Tempo do sistema): double timeStampScale = 1,0;  
Observe que as etapas restantes são desnecessárias para eventos que usam o tempo do sistema, pois os eventos já fornecem seus carimbos de data/hora em unidades FILETIME. As etapas restantes funcionarão, mas serão desnecessárias e apresentarão um pequeno erro de arredondamento.  
c. Se ReservedFlags == 3 (contador de ciclo de CPU): double timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                         |
| Cabeçalho<br/>                   | <dl> <dt>Wmistr.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**PROPRIEDADES \_ DE RASTREAMENTO DE \_ EVENTO**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**INTEIRO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
