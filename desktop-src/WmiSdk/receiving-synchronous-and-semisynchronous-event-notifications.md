---
description: Use SWbemServices.ExecQuery para solicitar todos os eventos existentes.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Recebendo notificações de eventos síncronas e Semisynchronous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781546"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="2f133-103">Recebendo notificações de eventos síncronas e Semisynchronous</span><span class="sxs-lookup"><span data-stu-id="2f133-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="2f133-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para solicitar todos os eventos existentes.</span><span class="sxs-lookup"><span data-stu-id="2f133-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="2f133-105">O exemplo de código a seguir mostra como consultar os eventos em um log.</span><span class="sxs-lookup"><span data-stu-id="2f133-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="2f133-106">Para obter mais informações, consulte [determinando o tipo de evento a receber](determining-the-type-of-event-to-receive.md), [recebendo notificações de eventos](receiving-event-notifications.md)e [WQL (SQL para WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="2f133-107">A chamada padrão para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usa a comunicação semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="2f133-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="2f133-108">O parâmetro *iFlags* tem os sinalizadores **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** definidos por padrão.</span><span class="sxs-lookup"><span data-stu-id="2f133-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="2f133-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2f133-110">O procedimento a seguir descreve como receber a notificação de eventos do semisynchronous usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="2f133-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="2f133-111">**Para receber a notificação de eventos do semisynchronous no VBScript**</span><span class="sxs-lookup"><span data-stu-id="2f133-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="2f133-112">Crie uma consulta para o tipo de evento que você deseja receber.</span><span class="sxs-lookup"><span data-stu-id="2f133-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="2f133-113">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="2f133-114">Se você solicitar um tipo de evento de instância como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indique na consulta um tipo de instância de destino, por exemplo, disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="2f133-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="2f133-115">Se necessário, especifique uma instância, por exemplo, o nome de um namespace ao solicitar instâncias de [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) futuras para um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="2f133-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="2f133-116">Especifique um intervalo de sondagem para Instrumentação de Gerenciamento do Windows (WMI) em uma consulta, como "dentro de 10", para sondar a cada 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="2f133-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="2f133-117">Para obter mais informações, consulte a [cláusula Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="2f133-118">Chame [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usando a consulta.</span><span class="sxs-lookup"><span data-stu-id="2f133-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="2f133-119">Faça um loop pela coleção que você receber.</span><span class="sxs-lookup"><span data-stu-id="2f133-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="2f133-120">O exemplo a seguir mostra como monitorar a inserção e a remoção de discos de uma unidade de disquete em um computador local.</span><span class="sxs-lookup"><span data-stu-id="2f133-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="2f133-121">O script solicita \_ instâncias [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) para a instância de disco rígido do [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de unidade de disquete e sonda a cada 10 segundos para novas instâncias.</span><span class="sxs-lookup"><span data-stu-id="2f133-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="2f133-122">Esse script é um exemplo de um consumidor de evento temporário e continua em execução até que seja interrompido no Gerenciador de tarefas ou o sistema seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="2f133-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="2f133-123">Para obter mais informações, consulte [recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="2f133-124">O procedimento a seguir descreve como receber a notificação de eventos do semisynchronous usando o C++.</span><span class="sxs-lookup"><span data-stu-id="2f133-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="2f133-125">**Para receber a notificação de eventos do semisynchronous em C++**</span><span class="sxs-lookup"><span data-stu-id="2f133-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="2f133-126">Configure o aplicativo com chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="2f133-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="2f133-127">Como o WMI é baseado em COM, chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) é uma etapa necessária para um aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="2f133-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="2f133-128">Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="2f133-129">Determine o tipo de eventos que você deseja receber.</span><span class="sxs-lookup"><span data-stu-id="2f133-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="2f133-130">O WMI dá suporte a eventos intrínsecos e extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="2f133-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="2f133-131">Um evento intrínseco é um evento predefinido pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="2f133-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="2f133-132">Um evento extrínsecos é um evento definido por um provedor de terceiros.</span><span class="sxs-lookup"><span data-stu-id="2f133-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="2f133-133">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="2f133-134">Registre-se para receber uma classe específica de eventos com uma chamada para o método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="2f133-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="2f133-135">Torne cada consulta muito específica.</span><span class="sxs-lookup"><span data-stu-id="2f133-135">Make each query very specific.</span></span> <span data-ttu-id="2f133-136">O objetivo do registro é registrar-se para receber apenas as notificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="2f133-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="2f133-137">Notificações que não são necessárias para processamento de desperdício e tempo de entrega.</span><span class="sxs-lookup"><span data-stu-id="2f133-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="2f133-138">Você pode criar um consumidor de eventos para receber vários eventos.</span><span class="sxs-lookup"><span data-stu-id="2f133-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="2f133-139">Por exemplo, um consumidor pode exigir notificação de eventos de modificação de instância para uma classe específica de eventos de violação de segurança e dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f133-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="2f133-140">Nesse caso, as tarefas que um consumidor realiza ao receber um evento de modificação de instância são diferentes para os dois eventos.</span><span class="sxs-lookup"><span data-stu-id="2f133-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="2f133-141">Portanto, o consumidor deve fazer uma chamada para [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) para registrar eventos de modificação de instância e outra chamada para **ExecNotificationQuery** para registrar eventos de violação de segurança.</span><span class="sxs-lookup"><span data-stu-id="2f133-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="2f133-142">Na chamada para [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), defina o parâmetro *LFlags* como **sinalizador WBEM \_ \_ retornar \_ imediatamente** e o **sinalizador WBEM \_ \_ \_ somente para frente**.</span><span class="sxs-lookup"><span data-stu-id="2f133-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="2f133-143">O **\_ sinalizador WBEM \_ retorna \_ imediatamente** sinaliza solicitações semisynchronous e o sinalizador **WBEM \_ \_ \_ somente encaminhar** solicita um enumerador somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="2f133-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="2f133-144">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2f133-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="2f133-145">A função **ExecNotificationQuery** retorna um ponteiro para uma interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="2f133-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="2f133-146">Sondar notificações de eventos registrados fazendo chamadas repetidas para o método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="2f133-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="2f133-147">Quando terminar, libere o enumerador que aponta para o objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="2f133-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="2f133-148">Você pode liberar o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associado ao registro.</span><span class="sxs-lookup"><span data-stu-id="2f133-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="2f133-149">Liberar o ponteiro de **IWbemServices** faz com que o WMI pare de entregar eventos a todos os consumidores temporários associados.</span><span class="sxs-lookup"><span data-stu-id="2f133-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
