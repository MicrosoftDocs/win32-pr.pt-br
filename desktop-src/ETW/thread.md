---
description: Classe de thread-essa classe é a classe pai para eventos de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Classe Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105524"
---
# <a name="thread-class"></a>Classe Thread

Essa classe é a classe pai para eventos de thread.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **thread** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de thread em uma sessão de log de kernel NT, especifique o sinalizador de **thread do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de thread chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento de thread real ao consumir eventos.



| Tipo de evento                                                      | Descrição                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)<br/>   | Finalizar evento de thread. A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.                                                                                                        |
| **Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)<br/> | Iniciar evento de thread. A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.                                                                                                      |
| Valor do tipo de evento, 3                                             | Iniciar evento de thread de coleta de dados. Enumera os threads que estão sendo executados no momento em que a sessão do kernel é iniciada. A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento. |
| Valor do tipo de evento, 4                                             | Evento de thread de coleta de dados final. Enumera os threads que estão sendo executados no momento em que a sessão do kernel termina. A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.     |



 

Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai. Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado. É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ v1**](thread-v1.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 
