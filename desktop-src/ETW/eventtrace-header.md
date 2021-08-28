---
description: A classe de tipo de evento para o evento de header do arquivo de log. Essa classe contém informações sobre a sessão de rastreamento de eventos.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: a5d0515b9d7d720409e0a72aec7aad5dc54561637563976a35d03b3e0dec79f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829986"
---
# <a name="eventtrace_header-class"></a>Classe EventTrace \_ Header

A classe de tipo de evento para o evento de header do arquivo de log. Essa classe contém informações sobre a sessão de rastreamento de eventos.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>Membros

A **classe EventTrace \_ Header** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe EventTrace \_ Header** tem essas propriedades.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (17)
</dt> </dl>

Hora em que o sistema foi iniciado, em intervalos de 100 nanossegundos desde a meia-noite de 1º de janeiro de 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Tamanho dos buffers da sessão de rastreamento de eventos, em quilobytes.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (21)
</dt> </dl>

Número total de buffers perdidos.

</dd> <dt>

**BuffersEscrito**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

Número total de buffers gravados pela sessão de rastreamento de eventos.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13)
</dt> </dl>

Velocidade da CPU, em megahertz.

**Windows 2000:** Sem suporte.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Hora em que a sessão de rastreamento de eventos parou, em intervalos de 100 nanossegundos desde a meia-noite de 1º de janeiro de 1601. Esse valor pode ser 0 se você estiver consumindo eventos em tempo real ou de um arquivo de log para o qual o provide ainda está registrando eventos.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12)
</dt> </dl>

Número de eventos perdidos durante a sessão de rastreamento de eventos.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8), **Format("x")**
</dt> </dl>

Modo de registro em log atual para a sessão de rastreamento de eventos. Para ver uma lista de valores, consulte Constantes de modo de registro em log.

</dd> <dt>

**Logfilename**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (15), **Ponteiro**
</dt> </dl>

Nome do arquivo de log de rastreamento de eventos que contém os eventos.

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14), **Ponteiro**
</dt> </dl>

Nome da sessão de rastreamento de eventos.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Tamanho máximo do arquivo de log, em megabytes.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Número de processadores no sistema.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (18)
</dt> </dl>

Frequência do contador de desempenho de alta resolução, se houver um.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Tamanho de um tipo de dados de ponteiro, em bytes.

</dd> <dt>

**Providerversion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Número de build do sistema operacional.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (20)
</dt> </dl>

Reservado.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10)
</dt> </dl>

Reservado.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (19)
</dt> </dl>

Hora em que a sessão de rastreamento de eventos foi iniciada, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6)
</dt> </dl>

Resolução do temporizador de hardware, em unidades de 100 nanossegundos.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (16), **extensão ("noprint")**, **Max** (176)
</dt> </dl>

Uma estrutura de [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) que contém o fuso horário para os membros **boottime**, **EndTime** e **StartTime** .

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Número de versão do sistema operacional. Começando com os bytes de ordem inferior, os dois primeiros bytes contêm a versão principal, os dois próximos bytes contêm uma versão secundária, os dois próximos bytes contêm service pack versão principal e os dois últimos bytes contêm service pack versão secundária.

</dd> </dl>

## <a name="remarks"></a>Comentários

Normalmente, você deseja salvar os valores para as propriedades a seguir para uso posterior ao processar eventos do arquivo de log.

-   **TimerResolution**— use com os membros de **kerneltime** e **usertime** da estrutura do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para determinar o custo da CPU para um conjunto de instruções. Para obter detalhes, consulte a seção comentários [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **Ponteiroize**– para propriedades que contêm o qualificador de **ponteiro** , use esse valor para determinar o tamanho do ponteiro. Observe que esse valor pode não ser preciso. Por exemplo, em um computador de 64 bits, um aplicativo de 32 bits registrará ponteiros de 4 bytes; no entanto, a sessão definirá **ponteiros** para 8.
-   **LOGFILEMODE**— use para determinar se esta sessão é uma sessão de agente de log particular. Há algumas propriedades que não contêm dados para sessões de agente particular. Por exemplo, os membros **kerneltime** e **usertime** da estrutura [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**cabeçalho do arquivo de log de rastreamento \_ \_**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
