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
# <a name="swbemsink-object"></a><span data-ttu-id="38b85-103">Objeto SWbemSink</span><span class="sxs-lookup"><span data-stu-id="38b85-103">SWbemSink object</span></span>

<span data-ttu-id="38b85-104">O objeto **SWbemSink** é implementado por aplicativos cliente para receber os resultados de operações assíncronas e notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="38b85-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="38b85-105">Para fazer uma chamada assíncrona, você deve criar uma instância de um objeto **SWbemSink** e passá-lo como o parâmetro *ObjWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="38b85-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="38b85-106">Os eventos em sua implementação de **SWbemSink** são disparados quando o status ou os resultados são retornados ou quando a chamada é concluída.</span><span class="sxs-lookup"><span data-stu-id="38b85-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="38b85-107">A chamada VBScript **CreateObject** cria esse objeto.</span><span class="sxs-lookup"><span data-stu-id="38b85-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="38b85-108">Membros</span><span class="sxs-lookup"><span data-stu-id="38b85-108">Members</span></span>

<span data-ttu-id="38b85-109">O objeto **SWbemSink** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="38b85-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="38b85-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="38b85-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="38b85-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="38b85-111">Methods</span></span>

<span data-ttu-id="38b85-112">O objeto **SWbemSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="38b85-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="38b85-113">Método</span><span class="sxs-lookup"><span data-stu-id="38b85-113">Method</span></span>                             | <span data-ttu-id="38b85-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="38b85-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="38b85-115">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="38b85-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="38b85-116">Cancela todas as operações assíncronas associadas a este coletor.</span><span class="sxs-lookup"><span data-stu-id="38b85-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38b85-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="38b85-117">Remarks</span></span>

<span data-ttu-id="38b85-118">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="38b85-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="38b85-119">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="38b85-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="38b85-120">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="38b85-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="38b85-121">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="38b85-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="38b85-122">Eventos</span><span class="sxs-lookup"><span data-stu-id="38b85-122">Events</span></span>

<span data-ttu-id="38b85-123">Você pode implementar sub-rotinas a serem chamadas quando os eventos forem disparados.</span><span class="sxs-lookup"><span data-stu-id="38b85-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="38b85-124">Por exemplo, se você quiser processar cada objeto retornado por uma chamada de consulta assíncrona, como [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), crie uma sub-rotina usando o coletor especificado na chamada assíncrona, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="38b85-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="38b85-125">Use a tabela a seguir como uma referência para identificar eventos e descrições de gatilho.</span><span class="sxs-lookup"><span data-stu-id="38b85-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="38b85-126">Evento</span><span class="sxs-lookup"><span data-stu-id="38b85-126">Event</span></span>                                            | <span data-ttu-id="38b85-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="38b85-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="38b85-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="38b85-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="38b85-129">Disparado quando uma operação assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="38b85-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="38b85-130">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="38b85-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="38b85-131">Disparado quando uma operação Put assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="38b85-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="38b85-132">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="38b85-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="38b85-133">Disparado quando um objeto fornecido por uma chamada assíncrona está disponível.</span><span class="sxs-lookup"><span data-stu-id="38b85-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="38b85-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="38b85-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="38b85-135">Disparado para fornecer o status de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="38b85-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="38b85-136">**Recuperando de forma assíncrona as estatísticas do log de eventos**</span><span class="sxs-lookup"><span data-stu-id="38b85-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="38b85-137">O WMI dá suporte a scripts assíncronos e semisíncronos.</span><span class="sxs-lookup"><span data-stu-id="38b85-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="38b85-138">Ao recuperar eventos dos logs de eventos, os scripts assíncronos geralmente recuperam esses dados muito mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="38b85-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="38b85-139">Em um script assíncrono, uma consulta é emitida e o controle é retornado imediatamente para o script.</span><span class="sxs-lookup"><span data-stu-id="38b85-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="38b85-140">A consulta continua a ser processada em um thread separado, enquanto o script começa a agir imediatamente sobre as informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="38b85-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="38b85-141">Os scripts assíncronos são controlados por evento: cada vez que um registro de evento é recuperado, o evento OnObjectReady é acionado.</span><span class="sxs-lookup"><span data-stu-id="38b85-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="38b85-142">Quando a consulta for concluída, o evento OnCompleted será acionado e o script poderá continuar com base no fato de que todos os registros disponíveis foram retornados.</span><span class="sxs-lookup"><span data-stu-id="38b85-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="38b85-143">Em um script semisíncrono, por outro lado, uma consulta é emitida e o script, em seguida, enfileira uma grande quantidade de informações recuperadas antes de agir sobre ela.</span><span class="sxs-lookup"><span data-stu-id="38b85-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="38b85-144">Para muitos objetos, o processamento semi-síncrono é adequado; por exemplo, ao consultar uma unidade de disco para suas propriedades, pode haver apenas uma divisão de segundo entre a hora em que a consulta é emitida e a hora em que as informações são retornadas e aplicadas.</span><span class="sxs-lookup"><span data-stu-id="38b85-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="38b85-145">Isso é devido a uma grande parte do fato de que a quantidade de informações retornadas é relativamente pequena.</span><span class="sxs-lookup"><span data-stu-id="38b85-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="38b85-146">No entanto, ao consultar um log de eventos, o intervalo entre a hora em que a consulta é emitida e a hora em que um script semisíncrono pode terminar de retornar e agir nas informações pode levar horas.</span><span class="sxs-lookup"><span data-stu-id="38b85-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="38b85-147">Além disso, o script pode ficar sem memória e falhar por conta própria antes de concluir.</span><span class="sxs-lookup"><span data-stu-id="38b85-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="38b85-148">Para logs de eventos com um grande número de registros, a diferença no tempo de processamento pode ser considerável.</span><span class="sxs-lookup"><span data-stu-id="38b85-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="38b85-149">Em um computador de teste com base no Windows 2000 com 2.000 registros no log de eventos, uma consulta semisíncrona que recuperou todos os eventos e exibi-los em uma janela de comando levou 10 minutos e 45 segundos.</span><span class="sxs-lookup"><span data-stu-id="38b85-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="38b85-150">Uma consulta assíncrona que realizou a mesma operação levou um minuto a 54 segundos.</span><span class="sxs-lookup"><span data-stu-id="38b85-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="38b85-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38b85-151">Examples</span></span>

<span data-ttu-id="38b85-152">O VBScript a seguir consulta os logs de eventos de forma assíncrona para todos os registros.</span><span class="sxs-lookup"><span data-stu-id="38b85-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="38b85-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38b85-153">Requirements</span></span>



| <span data-ttu-id="38b85-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b85-154">Requirement</span></span> | <span data-ttu-id="38b85-155">Valor</span><span class="sxs-lookup"><span data-stu-id="38b85-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38b85-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38b85-156">Minimum supported client</span></span><br/> | <span data-ttu-id="38b85-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38b85-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38b85-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38b85-158">Minimum supported server</span></span><br/> | <span data-ttu-id="38b85-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38b85-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38b85-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38b85-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="38b85-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38b85-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="38b85-162">INSERI</span><span class="sxs-lookup"><span data-stu-id="38b85-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38b85-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38b85-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="38b85-164">DLL</span><span class="sxs-lookup"><span data-stu-id="38b85-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38b85-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38b85-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="38b85-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="38b85-166">CLSID</span></span><br/>                    | <span data-ttu-id="38b85-167">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="38b85-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="38b85-168">\_SWBEMSINKEVENTS CLSID</span><span class="sxs-lookup"><span data-stu-id="38b85-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="38b85-169">IID</span><span class="sxs-lookup"><span data-stu-id="38b85-169">IID</span></span><br/>                      | <span data-ttu-id="38b85-170">ISWbemSink de IID \_</span><span class="sxs-lookup"><span data-stu-id="38b85-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="38b85-171">ISWbemSinkEvents de IID \_</span><span class="sxs-lookup"><span data-stu-id="38b85-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="38b85-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="38b85-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b85-173">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="38b85-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




