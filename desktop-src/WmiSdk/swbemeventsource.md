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
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789323"
---
# <a name="swbemeventsource-object"></a><span data-ttu-id="6b291-103">Objeto SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="6b291-103">SWbemEventSource object</span></span>

<span data-ttu-id="6b291-104">O objeto **SWbemEventSource** recupera eventos de uma consulta de evento em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="6b291-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="6b291-105">Você obterá um objeto **SWbemEventSource** se fizer uma chamada para **SWbemServices.ExecNotificationQuery** para fazer uma consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="6b291-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="6b291-106">Em seguida, você pode usar o método [**NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="6b291-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="6b291-107">Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b291-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="6b291-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6b291-108">Members</span></span>

<span data-ttu-id="6b291-109">O objeto **SWbemEventSource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6b291-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="6b291-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6b291-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b291-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6b291-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b291-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6b291-112">Methods</span></span>

<span data-ttu-id="6b291-113">O objeto **SWbemEventSource** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6b291-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="6b291-114">Método</span><span class="sxs-lookup"><span data-stu-id="6b291-114">Method</span></span>                                          | <span data-ttu-id="6b291-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b291-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b291-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="6b291-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="6b291-117">Usado para recuperar um evento em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="6b291-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6b291-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6b291-118">Properties</span></span>

<span data-ttu-id="6b291-119">O objeto **SWbemEventSource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6b291-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="6b291-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6b291-120">Property</span></span>                                                    | <span data-ttu-id="6b291-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="6b291-121">Access type</span></span>          | <span data-ttu-id="6b291-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b291-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="6b291-123">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="6b291-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="6b291-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b291-124">Read-only</span></span><br/> | <span data-ttu-id="6b291-125">Usado para ler ou alterar as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="6b291-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6b291-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b291-126">Examples</span></span>

<span data-ttu-id="6b291-127">Esse script usa os métodos da classe **SWbemEventSource** e da classe [**SWbemServices**](swbemservices.md) em conjunto com uma consulta WQL para eventos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b291-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="6b291-128">Para obter mais informações sobre notificação de eventos e consultas do WMI, consulte [monitorando eventos](monitoring-events.md), [executando um script com base em um evento](running-a-script-based-on-an-event.md)e [recebendo notificações de eventos assíncronos](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6b291-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6b291-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b291-129">Requirements</span></span>



| <span data-ttu-id="6b291-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b291-130">Requirement</span></span> | <span data-ttu-id="6b291-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6b291-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b291-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b291-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6b291-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b291-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b291-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b291-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6b291-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b291-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b291-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b291-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b291-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b291-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b291-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b291-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b291-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b291-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b291-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6b291-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b291-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b291-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b291-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="6b291-142">CLSID</span></span><br/>                    | <span data-ttu-id="6b291-143">\_SWBEMEVENTSOURCE CLSID</span><span class="sxs-lookup"><span data-stu-id="6b291-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="6b291-144">IID</span><span class="sxs-lookup"><span data-stu-id="6b291-144">IID</span></span><br/>                      | <span data-ttu-id="6b291-145">ISWbemEventSource de IID \_</span><span class="sxs-lookup"><span data-stu-id="6b291-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="6b291-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b291-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b291-147">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="6b291-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

