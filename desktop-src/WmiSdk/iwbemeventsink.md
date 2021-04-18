---
description: Inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interface IWbemEventSink (Wbemprov. h)
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
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764457"
---
# <a name="iwbemeventsink-interface"></a>Interface IWbemEventSink

A interface **IWbemEventSink** inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas. Essa interface estende o [**IWbemObjectSink**](iwbemobjectsink.md), fornecendo novos métodos que lidam com segurança e desempenho. Para obter mais informações sobre como usar essa interface, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md) e [protegendo eventos WMI](securing-wmi-events.md).

## <a name="members"></a>Membros

A interface **IWbemEventSink** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWbemEventSink** tem esses métodos.



| Método                                                                | Descrição                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Chamado pelo consumidor para configurar consultas de eventos restritos.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Verifica o status do coletor de eventos.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Chamado pelo consumidor para definir parâmetros de envio em lote.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Usado para atualizar o descritor de segurança em um coletor de eventos.<br/>   |



 

## <a name="remarks"></a>Comentários

Ao implementar um coletor de assinatura de evento ([**IWbemObjectSink**](iwbemobjectsink.md) ou **IWbemEventSink**), não chame o WMI de dentro dos métodos no objeto Sink. Por exemplo, chamar [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar o coletor de dentro de uma implementação de [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) pode interferir no estado do WMI. Para cancelar uma assinatura de evento, defina um sinalizador e chame **IWbemServices:: CancelAsyncCall** de outro thread ou objeto. Para implementações que não estão relacionadas a um coletor de eventos, como recuperações de objeto, enum e consulta, você pode chamar de volta para o WMI.

As implementações do coletor devem processar a notificação de eventos dentro de 100 ms porque o thread WMI que entrega a notificação de eventos não pode realizar outro trabalho até que o objeto do coletor tenha concluído o processamento. Se a notificação exigir uma grande quantidade de processamento, o coletor poderá usar uma fila interna para que outro thread manipule o processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                            |
| parâmetro<br/>                   | <dl> <dt>Wbemprov. h (incluir Wbemidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




