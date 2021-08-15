---
description: Inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interface IWbemEventSink (Wbemprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 10c5fa56a96db3e46ce2c4c7941fd7a1d6fb27a1730dc3741890935782e4ace7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318092"
---
# <a name="iwbemeventsink-interface"></a>Interface IWbemEventSink

A interface **IWbemEventSink** inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas. Essa interface estende [**IWbemObjectSink,**](iwbemobjectsink.md)fornecendo novos métodos que lidam com segurança e desempenho. Para obter mais informações sobre como usar essa interface, consulte [Escrevendo um](writing-an-event-provider.md) provedor de eventos e proteger eventos [WMI](securing-wmi-events.md).

## <a name="members"></a>Membros

A interface **IWbemEventSink** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWbemEventSink** tem esses métodos.



| Método                                                                | Descrição                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Chamado pelo consumidor para configurar consultas de eventos restritos.<br/> |
| [**Isactive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Verifica o status do sink de eventos.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Chamado pelo consumidor para definir parâmetros de lote.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Usado para atualizar o descritor de segurança em um sink de evento.<br/>   |



 

## <a name="remarks"></a>Comentários

Ao implementar um sink de assinatura de evento [**(IWbemObjectSink**](iwbemobjectsink.md) ou **IWbemEventSink),** não chame o WMI de dentro dos métodos no objeto de sink. Por exemplo, chamar [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar o sink de dentro de uma implementação de [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) pode interferir no estado WMI. Para cancelar uma assinatura de evento, de definir um sinalizador e chamar **IWbemServices::CancelAsyncCall de** outro thread ou objeto. Para implementações que não estão relacionadas a um sink de evento, como recuperações de objeto, enum e consulta, você pode chamar novamente no WMI.

As implementações de sink devem processar a notificação de evento dentro de 100 MSEC porque o thread WMI que entrega a notificação de evento não pode fazer outro trabalho até que o objeto do sink tenha concluído o processamento. Se a notificação exigir uma grande quantidade de processamento, o sink poderá usar uma fila interna para outro thread para lidar com o processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Wbemprov.h (inclua Wbemidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




