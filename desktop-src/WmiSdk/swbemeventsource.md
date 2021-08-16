---
description: O objeto SWbemEventSource recupera eventos de uma consulta de evento em conjunto com SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Objeto SWbemEventSource (Wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e38dab258ebccacb24cf92b7445752102b297ab1207b99e40355c30fde99113d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992136"
---
# <a name="swbemeventsource-object"></a>Objeto SWbemEventSource

O objeto **SWbemEventSource** recupera eventos de uma consulta de evento em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Você obterá um objeto **SWbemEventSource** se fizer uma chamada para **SWbemServices.ExecNotificationQuery** para fazer uma consulta de evento. Em seguida, você pode usar o método [**NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos à medida que eles chegam. Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membros

O objeto **SWbemEventSource** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemEventSource** tem esses métodos.



| Método                                          | Descrição                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Usado para recuperar um evento em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemEventSource** tem essas propriedades.



| Propriedade                                                    | Tipo de acesso          | Descrição                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Segurança\_**](swbemeventsource-security-.md)<br/> | Somente leitura<br/> | Usado para ler ou alterar as configurações de segurança.<br/> |



 

## <a name="examples"></a>Exemplos

Esse script usa os métodos da classe **SWbemEventSource** e da classe [**SWbemServices**](swbemservices.md) em conjunto com uma consulta WQL para eventos de aplicativo. Para obter mais informações sobre notificação de eventos e consultas do WMI, consulte [monitorando eventos](monitoring-events.md), [executando um script com base em um evento](running-a-script-based-on-an-event.md)e [recebendo notificações de eventos assíncronos](receiving-asynchronous-event-notifications.md).


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMEVENTSOURCE CLSID<br/>                                                      |
| IID<br/>                      | ISWbemEventSource de IID \_<br/>                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

