---
description: Para receber notificações do provedor de registro do sistema, um aplicativo de gerenciamento deve ser registrado como um consumidor de evento temporário.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrando para eventos de registro do sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810855"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="a4525-103">Registrando para eventos de registro do sistema</span><span class="sxs-lookup"><span data-stu-id="a4525-103">Registering for System Registry Events</span></span>

<span data-ttu-id="a4525-104">Para receber notificações do provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , um aplicativo de gerenciamento deve ser registrado como um consumidor de evento temporário.</span><span class="sxs-lookup"><span data-stu-id="a4525-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="a4525-105">A maioria dos requisitos de registro para o provedor de registro do sistema é igual a qualquer outro registro de evento, exceto que você também deve executar o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4525-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="a4525-106">O provedor de registro fornece classes de evento para eventos no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4525-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="a4525-107">Para obter mais informações sobre o registro de eventos gerais, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="a4525-108">O procedimento a seguir descreve como registrar-se para eventos de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4525-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="a4525-109">**Para registrar-se para eventos de registro do sistema**</span><span class="sxs-lookup"><span data-stu-id="a4525-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="a4525-110">Chamar um método de consulta de notificação.</span><span class="sxs-lookup"><span data-stu-id="a4525-110">Call a notification query method.</span></span>

    <span data-ttu-id="a4525-111">Em script ou C++, use uma consulta de notificação como [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ou [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="a4525-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="a4525-112">Crie uma cadeia de caracteres de consulta para o parâmetro *bstrQuery* de **IWbemServices:: ExecNotificationQueryAsync** ou *strQuery* no script.</span><span class="sxs-lookup"><span data-stu-id="a4525-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="a4525-113">Determine o tipo de evento que você deseja receber e crie a consulta.</span><span class="sxs-lookup"><span data-stu-id="a4525-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="a4525-114">A tabela a seguir lista as classes de evento do registro que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="a4525-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="a4525-115">Classe de eventos</span><span class="sxs-lookup"><span data-stu-id="a4525-115">Event class</span></span>                                                      | <span data-ttu-id="a4525-116">Localização do hive</span><span class="sxs-lookup"><span data-stu-id="a4525-116">Hive location</span></span>        | <span data-ttu-id="a4525-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4525-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="a4525-118">**RegistryEvent**</span><span class="sxs-lookup"><span data-stu-id="a4525-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="a4525-119">N/D</span><span class="sxs-lookup"><span data-stu-id="a4525-119">N/A</span></span><br/>       | <span data-ttu-id="a4525-120">Classe base abstrata para alterações no registro.</span><span class="sxs-lookup"><span data-stu-id="a4525-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="a4525-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a4525-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="a4525-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="a4525-122">RootPath</span></span><br/>  | <span data-ttu-id="a4525-123">Monitora as alterações em uma hierarquia de chaves.</span><span class="sxs-lookup"><span data-stu-id="a4525-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="a4525-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a4525-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="a4525-125">KeyPath</span><span class="sxs-lookup"><span data-stu-id="a4525-125">KeyPath</span></span><br/>   | <span data-ttu-id="a4525-126">Monitora as alterações em uma única chave.</span><span class="sxs-lookup"><span data-stu-id="a4525-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="a4525-127">**RegistryValueChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a4525-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="a4525-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="a4525-128">ValueName</span></span><br/> | <span data-ttu-id="a4525-129">Monitora as alterações em um único valor.</span><span class="sxs-lookup"><span data-stu-id="a4525-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="a4525-130">Essas classes têm uma propriedade chamada **Hive** que identifica a hierarquia de chaves a ser monitorada para alteração, como **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="a4525-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="a4525-131">As alterações nas **seções hKey \_ classes \_ raiz** e **HKEY \_ Current \_ User** não são suportadas por [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ou classes derivadas dela, como [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span><span class="sxs-lookup"><span data-stu-id="a4525-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="a4525-132">Crie a cláusula WHERE para o registro do evento.</span><span class="sxs-lookup"><span data-stu-id="a4525-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="a4525-133">O provedor de registro do sistema tem regras específicas para cláusulas WHERE.</span><span class="sxs-lookup"><span data-stu-id="a4525-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="a4525-134">Para obter mais informações, consulte [criando uma cláusula WHERE apropriada para o provedor de registro](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="a4525-135">Para obter mais informações gerais sobre como criar uma cláusula WHERE, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="a4525-136">Determine se o consumidor está recebendo eventos.</span><span class="sxs-lookup"><span data-stu-id="a4525-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="a4525-137">O provedor de registro do sistema não garante que todos os eventos enviados sejam entregues.</span><span class="sxs-lookup"><span data-stu-id="a4525-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="a4525-138">Para obter mais informações, consulte [recebendo eventos do registro](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="a4525-139">O exemplo de código VBScript a seguir mostra como detectar uma alteração no registro no software da **\_ \_ máquina local hKey** \\  \\ **Microsoft** Hive ou Subtree.</span><span class="sxs-lookup"><span data-stu-id="a4525-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="a4525-140">Esse é um script de monitoramento que, para fins de demonstração, é executado em um processo chamado Wscript.exe até que seja encerrado no **Gerenciador de tarefas**, o WMI seja interrompido ou o sistema operacional seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="a4525-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="a4525-141">O script usa uma chamada [*semisynchronous*](gloss-s.md) para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="a4525-142">Para obter mais informações sobre chamadas semisynchronous, consulte [fazendo uma chamada semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



O exemplo de código VBScript a seguir mostra como monitorar a alteração nos valores de uma chave registrando-se para o tipo de evento do provedor de registro [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). O script chama um método assíncrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="a4525-145">Para obter mais informações sobre chamadas assíncronas e segurança, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="a4525-146">O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="a4525-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="a4525-147">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="a4525-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="a4525-148">Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="a4525-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

