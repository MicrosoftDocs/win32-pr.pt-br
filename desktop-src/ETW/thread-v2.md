---
description: Thread_V2 classe - essa classe é a classe pai para eventos de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: d057f80d5cf29f6660ee3a2ebd651c468496529a56a11147225ebd504451184c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069386"
---
# <a name="thread_v2-class"></a>Classe Thread \_ V2

Essa classe é a classe pai para eventos de thread.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A **classe Thread \_ V2** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de thread em uma sessão de log do Kernel NT, especifique o sinalizador THREAD DO SINALIZADOR **\_ \_ DE \_** RASTREAMENTO DE EVENTOS no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar os seguintes sinalizadores:

-   **SINALIZADOR \_ DE RASTREAMENTO DE EVENTOS \_ \_ CSWITCH**
-   **DISPATCHER \_ DO SINALIZADOR DE RASTREAMENTO DE \_ \_ EVENTOS**

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos de thread chamando a [**função SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento de thread real ao consumir eventos.



| Tipo de evento                                                      | Descrição                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(o valor do tipo de evento é 2)<br/>   | Evento de thread final. A [**classe \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados de evento para esse evento.                                                                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ START**(o valor do tipo de evento é 1)<br/> | Iniciar evento de thread. A [**classe \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados de evento para esse evento.                                                                                                      |
| Valor do tipo de evento, 3                                             | Iniciar evento de thread de coleta de dados. Enumera threads que estão sendo executados no momento em que a sessão do kernel é iniciada. A [**classe \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados de evento para esse evento. |
| Valor do tipo de evento, 4                                             | Evento de thread de coleta de dados final. Enumera threads que estão sendo executados no momento em que a sessão do kernel termina. A [**classe \_ MOF Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados de evento para esse evento.     |
| Valor do tipo de evento, 36                                            | Evento de opção de contexto. A [**classe MOF CSwitch**](cswitch.md) define os dados de evento para esse evento.                                                                                                                                |
| Valor do tipo de evento, 50                                            | Evento de thread pronto. A [**classe ReadyThread**](readythread.md) MOF define os dados de evento para esse evento.                                                                                                                          |



 

Eventos de início de thread e processo podem ser registrados no contexto do processo ou thread pai. Como resultado, os **membros ProcessId** e **ThreadId** do [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado. É por isso que esses eventos contêm os identificadores de processo e thread nos dados do evento (além daqueles no header do evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemTrace do MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**CSwitch**](cswitch.md)
</dt> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 
