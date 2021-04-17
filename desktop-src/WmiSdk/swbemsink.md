---
description: O objeto SWbemSink é implementado por aplicativos cliente para receber os resultados de operações assíncronas e notificações de eventos.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Objeto SWbemSink (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812094"
---
# <a name="swbemsink-object"></a>Objeto SWbemSink

O objeto **SWbemSink** é implementado por aplicativos cliente para receber os resultados de operações assíncronas e notificações de eventos. Para fazer uma chamada assíncrona, você deve criar uma instância de um objeto **SWbemSink** e passá-lo como o parâmetro *ObjWbemSink* . Os eventos em sua implementação de **SWbemSink** são disparados quando o status ou os resultados são retornados ou quando a chamada é concluída. A chamada VBScript **CreateObject** cria esse objeto.

## <a name="members"></a>Membros

O objeto **SWbemSink** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **SWbemSink** tem esses métodos.



| Método                             | Descrição                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Cancelar**](swbemsink-cancel.md) | Cancela todas as operações assíncronas associadas a este coletor.<br/> |



 

## <a name="remarks"></a>Comentários

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

### <a name="events"></a>Eventos

Você pode implementar sub-rotinas a serem chamadas quando os eventos forem disparados. Por exemplo, se você quiser processar cada objeto retornado por uma chamada de consulta assíncrona, como [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), crie uma sub-rotina usando o coletor especificado na chamada assíncrona, conforme mostrado no exemplo a seguir.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Use a tabela a seguir como uma referência para identificar eventos e descrições de gatilho.



| Evento                                            | Descrição                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Disparado quando uma operação assíncrona é concluída.                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | Disparado quando uma operação Put assíncrona é concluída.               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | Disparado quando um objeto fornecido por uma chamada assíncrona está disponível. |
| [**OnProgress**](swbemsink-onprogress.md)       | Disparado para fornecer o status de uma operação assíncrona.            |



 

**Recuperando de forma assíncrona as estatísticas do log de eventos**

O WMI dá suporte a scripts assíncronos e semisíncronos. Ao recuperar eventos dos logs de eventos, os scripts assíncronos geralmente recuperam esses dados muito mais rapidamente.

Em um script assíncrono, uma consulta é emitida e o controle é retornado imediatamente para o script. A consulta continua a ser processada em um thread separado, enquanto o script começa a agir imediatamente sobre as informações retornadas. Os scripts assíncronos são controlados por evento: cada vez que um registro de evento é recuperado, o evento OnObjectReady é acionado. Quando a consulta for concluída, o evento OnCompleted será acionado e o script poderá continuar com base no fato de que todos os registros disponíveis foram retornados.

Em um script semisíncrono, por outro lado, uma consulta é emitida e o script, em seguida, enfileira uma grande quantidade de informações recuperadas antes de agir sobre ela. Para muitos objetos, o processamento semi-síncrono é adequado; por exemplo, ao consultar uma unidade de disco para suas propriedades, pode haver apenas uma divisão de segundo entre a hora em que a consulta é emitida e a hora em que as informações são retornadas e aplicadas. Isso é devido a uma grande parte do fato de que a quantidade de informações retornadas é relativamente pequena.

No entanto, ao consultar um log de eventos, o intervalo entre a hora em que a consulta é emitida e a hora em que um script semisíncrono pode terminar de retornar e agir nas informações pode levar horas. Além disso, o script pode ficar sem memória e falhar por conta própria antes de concluir.

Para logs de eventos com um grande número de registros, a diferença no tempo de processamento pode ser considerável. Em um computador de teste com base no Windows 2000 com 2.000 registros no log de eventos, uma consulta semisíncrona que recuperou todos os eventos e exibi-los em uma janela de comando levou 10 minutos e 45 segundos. Uma consulta assíncrona que realizou a mesma operação levou um minuto a 54 segundos.

## <a name="examples"></a>Exemplos

O VBScript a seguir consulta os logs de eventos de forma assíncrona para todos os registros.


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/> \_SWBEMSINKEVENTS CLSID<br/>                           |
| IID<br/>                      | ISWbemSink de IID \_<br/> ISWbemSinkEvents de IID \_<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




