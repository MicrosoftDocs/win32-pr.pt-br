---
description: Classe Process-essa classe é a classe pai para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Classe Process
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
ms.openlocfilehash: 25c21e5f301d88f3790900c70873d9485161f5041d28bb1a30f3bb85082a9bd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069896"
---
# <a name="process-class"></a>Classe Process

Essa classe é a classe pai para eventos de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **process** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de processo em uma sessão de log do kernel NT, especifique o sinalizador de **processo do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Você também pode especificar o seguinte sinalizador:

-   **\_contadores de \_ processo de sinalizador de rastreamento de eventos \_ \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de processo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento de processo real ao consumir eventos.



| Tipo de evento                                                      | Descrição                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)<br/>   | Encerrar o evento de processo. A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.                                                                                                          |
| **Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)<br/> | Iniciar o evento de processo. A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.                                                                                                        |
| Valor do tipo de evento, 3                                             | Iniciar evento de processo de coleta de dados. Enumera os processos que estão sendo executados no momento em que a sessão do kernel é iniciada. A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento. |
| Valor do tipo de evento, 4                                             | Evento de processo de coleta de dados final. Enumera os processos que estão sendo executados no momento em que a sessão do kernel termina. A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.     |



 

Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai. Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado. É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**TypeGroup1 de processo \_**](process-typegroup1.md)
</dt> <dt>

[**V0 de processo \_**](process-v0.md)
</dt> <dt>

[**Processo \_ v1**](process-v1.md)
</dt> <dt>

[**Processo \_ v2**](process-v2.md)
</dt> </dl>

 

 
