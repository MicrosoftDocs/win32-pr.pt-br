---
description: Process_V2 classe - essa classe é a classe pai para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8b5ac8c1e8dd09b8f3a1078abde39523487afbe901d1e3013eade82170e4af11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069936"
---
# <a name="process_v2-class"></a>Classe \_ Process V2

Essa classe é a classe pai para eventos de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A **classe** Process não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de processo em uma sessão de log do Kernel NT, especifique o sinalizador **EVENT \_ TRACE FLAG \_ \_ PROCESS** no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar o seguinte sinalizador:

-   **CONTADORES DE \_ PROCESSO DO SINALIZADOR DE RASTREAMENTO DE \_ \_ \_ EVENTOS**

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos de processo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento de processo real ao consumir eventos.



| Tipo de evento                                                      | Descrição                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(o valor do tipo de evento é 2)<br/>   | Evento de processo final. A [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) define os dados de evento para esse evento.                                                                                                          |
| **EVENTO \_ TRACE \_ TYPE \_ START**(o valor do tipo de evento é 1)<br/> | Iniciar evento de processo. A [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) define os dados de evento para esse evento.                                                                                                        |
| Valor do tipo de evento, 3                                             | Iniciar evento de processo de coleta de dados. Enumera os processos que estão sendo executados no momento em que a sessão do kernel é iniciada. A [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) define os dados de evento para esse evento. |
| Valor do tipo de evento, 4                                             | Evento de processo de coleta de dados final. Enumera os processos que estão sendo executados no momento em que a sessão do kernel termina. A [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) define os dados de evento para esse evento.     |
| Valor do tipo de evento, 32                                            | Evento de contadores de desempenho. A [**classe \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define os dados de evento para esse evento.                                                                                          |
| Valor do tipo de evento, 33                                            | Rundown dos contadores de desempenho no início da sessão. A [**classe \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) define os dados de evento para esse evento.                                                     |
| Valor do tipo de evento, 39                                            | Evento de processo defunção. A [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) define os dados de evento para esse evento.                                                                                                      |



 

Eventos de início de thread e processo podem ser registrados no contexto do processo ou thread pai. Como resultado, os **membros ProcessId** e **ThreadId** do [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado. É por isso que esses eventos contêm os identificadores de processo e thread nos dados do evento (além daqueles no header do evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemTrace do MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Processar**](process.md)
</dt> <dt>

[**Processar \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processo \_ V0**](process-v0.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> </dl>

 

 
