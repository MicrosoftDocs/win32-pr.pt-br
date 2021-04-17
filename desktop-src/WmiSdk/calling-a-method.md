---
description: O WMI fornece métodos na API COM e na API de script para obter informações ou manipular objetos em um sistema empresarial.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Chamando um método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770615"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="07861-103">Chamando um método WMI</span><span class="sxs-lookup"><span data-stu-id="07861-103">Calling a WMI Method</span></span>

<span data-ttu-id="07861-104">O WMI fornece métodos na [API com](com-api-for-wmi.md) e na [API de script](scripting-api-for-wmi.md) para obter informações ou manipular objetos em um sistema empresarial.</span><span class="sxs-lookup"><span data-stu-id="07861-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="07861-105">Por exemplo, o método de script WMI [**SWbemServices.Execonsultas cQuery**](swbemservices-execquery.md) para dados.</span><span class="sxs-lookup"><span data-stu-id="07861-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="07861-106">Os provedores também têm métodos definidos nas classes que registram.</span><span class="sxs-lookup"><span data-stu-id="07861-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="07861-107">Os exemplos são os métodos do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) e [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) fornecidos pelo [provedor do Win32](/windows/desktop/CIMWin32Prov/win32-provider).</span><span class="sxs-lookup"><span data-stu-id="07861-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="07861-108">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="07861-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="07861-109">Métodos WMI em comparação com métodos de provedor</span><span class="sxs-lookup"><span data-stu-id="07861-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="07861-110">Modos de chamada de método no WMI</span><span class="sxs-lookup"><span data-stu-id="07861-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="07861-111">Modo síncrono</span><span class="sxs-lookup"><span data-stu-id="07861-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="07861-112">Modo assíncrono</span><span class="sxs-lookup"><span data-stu-id="07861-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="07861-113">Modo de Semisynchronous</span><span class="sxs-lookup"><span data-stu-id="07861-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="07861-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07861-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="07861-115">Métodos WMI em comparação com métodos de provedor</span><span class="sxs-lookup"><span data-stu-id="07861-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="07861-116">Usando as chamadas de [*método WMI*](gloss-w.md) combinadas com chamadas de [*método de provedor*](gloss-p.md) , você pode recuperar e manipular informações sobre sua empresa.</span><span class="sxs-lookup"><span data-stu-id="07861-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="07861-117">Para obter mais informações, consulte [chamando um método WMI](calling-a-wmi-method.md) e [chamando um método de provedor](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="07861-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="07861-118">Os métodos do objeto de script WMI [**SWbemObject**](swbemobject.md) têm um status especial, pois podem ser aplicados a qualquer classe de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="07861-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="07861-119">Para obter mais informações, consulte [scripts com SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="07861-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="07861-120">O exemplo de código a seguir chama o WMI e os métodos de provedor.</span><span class="sxs-lookup"><span data-stu-id="07861-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="07861-121">Os seguintes métodos WMI e de provedor estão localizados na [API de script para o WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="07861-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="07861-122">**objWMIService.ExecQuery** chama o método de script WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="07861-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="07861-123">**objService. StopService ()** chama o método de provedor [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="07861-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="07861-124">Você pode pesquisar o código que pode aparecer em "Return" na seção de códigos de retorno do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="07861-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="07861-125">Modos de Method-Calling no WMI</span><span class="sxs-lookup"><span data-stu-id="07861-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="07861-126">O modo de chamada semisynchronous geralmente fornece o melhor equilíbrio entre segurança e desempenho.</span><span class="sxs-lookup"><span data-stu-id="07861-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="07861-127">Para obter mais informações sobre cada um dos modos possíveis, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="07861-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="07861-128">Síncrono</span><span class="sxs-lookup"><span data-stu-id="07861-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="07861-129">Assíncronos</span><span class="sxs-lookup"><span data-stu-id="07861-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="07861-130">Semisynchronous</span><span class="sxs-lookup"><span data-stu-id="07861-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="07861-131">Modo síncrono</span><span class="sxs-lookup"><span data-stu-id="07861-131">Synchronous Mode</span></span>

<span data-ttu-id="07861-132">O modo síncrono ocorre quando o programa ou os scripts pausa até que a chamada de método retorne um objeto de coleção [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="07861-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="07861-133">O WMI cria essa coleção na memória antes de retornar o objeto de coleção para o programa ou script de chamada.</span><span class="sxs-lookup"><span data-stu-id="07861-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="07861-134">O modo síncrono pode ter um efeito adverso de desempenho de programa ou script no computador que executa o programa ou o script.</span><span class="sxs-lookup"><span data-stu-id="07861-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="07861-135">Por exemplo, a recuperação síncrona de milhares de eventos do log de eventos pode levar muito tempo e usar muita memória porque o WMI cria um objeto de cada evento e coloca esses objetos em uma coleção antes de passar a coleção para o método.</span><span class="sxs-lookup"><span data-stu-id="07861-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="07861-136">Você só deve chamar métodos que não retornam conjuntos de dados grandes no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="07861-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="07861-137">Os seguintes métodos [**SWbemServices**](swbemservices.md) podem ser chamados com segurança no modo síncrono:</span><span class="sxs-lookup"><span data-stu-id="07861-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="07861-138">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="07861-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="07861-139">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="07861-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="07861-140">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="07861-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="07861-141">Qualquer método [**SWbemServices**](swbemservices.md) sem a palavra, "Async" no nome pode ser chamado no modo síncrono, definindo o valor **WbemFlagReturnWhenComplete** no parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="07861-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="07861-142">Modo assíncrono</span><span class="sxs-lookup"><span data-stu-id="07861-142">Asynchronous Mode</span></span>

<span data-ttu-id="07861-143">O modo assíncrono ocorre quando o programa ou script continua a ser executado depois de chamar o método.</span><span class="sxs-lookup"><span data-stu-id="07861-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="07861-144">O WMI retorna todos os objetos do método para um objeto [**SWbemSink**](swbemsink.md) , pois cada objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="07861-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="07861-145">O programa ou script de chamada deve ter um objeto **SWbemSink** e um manipulador de eventos [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para processar os objetos retornados.</span><span class="sxs-lookup"><span data-stu-id="07861-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="07861-146">Para obter mais informações sobre como criar um manipulador de eventos para o modo assíncrono, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="07861-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="07861-147">Embora esse modo não tenha o desempenho e a penalidade de recursos do modo síncrono, o modo assíncrono pode criar sérios riscos de segurança porque os resultados armazenados no objeto [**SWbemSink**](swbemsink.md) podem não vir do script ou programa de chamada.</span><span class="sxs-lookup"><span data-stu-id="07861-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="07861-148">O WMI reduz o nível de autenticação no objeto **SWbemSink** até que o método tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="07861-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="07861-149">Para obter mais informações sobre como mitigar esses riscos de segurança, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="07861-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="07861-150">Os métodos anexados à palavra Async são métodos para o modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="07861-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="07861-151">Os métodos a seguir são chamadas assíncronas:</span><span class="sxs-lookup"><span data-stu-id="07861-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="07861-152">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="07861-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="07861-154">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="07861-155">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="07861-156">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="07861-157">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="07861-158">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="07861-159">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="07861-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="07861-160">Para obter mais informações sobre o modo assíncrono, consulte:</span><span class="sxs-lookup"><span data-stu-id="07861-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="07861-161">Fazendo uma chamada assíncrona com C++</span><span class="sxs-lookup"><span data-stu-id="07861-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="07861-162">Fazendo uma chamada assíncrona com o VBScript</span><span class="sxs-lookup"><span data-stu-id="07861-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="07861-163">Modo de Semisynchronous</span><span class="sxs-lookup"><span data-stu-id="07861-163">Semisynchronous Mode</span></span>

<span data-ttu-id="07861-164">O modo Semisynchronous é semelhante ao modo assíncrono no qual o programa ou script continua a ser executado depois de chamar o método.</span><span class="sxs-lookup"><span data-stu-id="07861-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="07861-165">No modo semisynchronous, o WMI recupera os objetos em segundo plano à medida que seu script ou programa continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="07861-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="07861-166">O WMI retorna cada objeto retornado ao método de chamada logo após a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="07861-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="07861-167">Como o WMI gerencia o objeto, o modo semisynchronous é mais seguro do que o modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="07861-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="07861-168">No entanto, se você usar o modo semisynchronous com mais de 1.000 instâncias, a recuperação da instância poderá monopolizar os recursos disponíveis, o que pode prejudicar o desempenho do programa ou do script e do computador usando o programa ou script.</span><span class="sxs-lookup"><span data-stu-id="07861-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="07861-169">Cada objeto ocupará os recursos necessários até que a memória seja liberada.</span><span class="sxs-lookup"><span data-stu-id="07861-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="07861-170">Para contornar essa condição, você pode chamar o método com o parâmetro *iFlags* definido com os sinalizadores **wbemFlagForwardOnly** e **WBEMFLAGRETURNIMMEDIATELY** para instruir o WMI a retornar um [**SWbemObjectSet**](swbemobjectset.md)somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="07861-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="07861-171">Um **SWbemObjectSet** somente de encaminhamento elimina o problema de desempenho causado por um grande conjunto de dados liberando a memória depois que o objeto é enumerado.</span><span class="sxs-lookup"><span data-stu-id="07861-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="07861-172">Qualquer método [**SWbemServices**](swbemservices.md) que não pode ser chamado no modo síncrono ou assíncrono é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="07861-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="07861-173">Os métodos a seguir são chamados no modo semisynchronous:</span><span class="sxs-lookup"><span data-stu-id="07861-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="07861-174">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="07861-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="07861-175">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="07861-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="07861-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="07861-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="07861-177">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="07861-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="07861-178">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="07861-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="07861-179">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="07861-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="07861-180">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="07861-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="07861-181">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="07861-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="07861-182">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="07861-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="07861-183">**SWbemServices. put**</span><span class="sxs-lookup"><span data-stu-id="07861-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="07861-184">Para obter mais informações sobre o modo semisynchronous, consulte [fazendo uma chamada semisynchronous com C++](making-a-semisynchronous-call-with-c--.md) e [fazendo uma chamada de Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="07861-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07861-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07861-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07861-186">Melhorando o desempenho da enumeração</span><span class="sxs-lookup"><span data-stu-id="07861-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="07861-187">Criando scripts com SWbemObject</span><span class="sxs-lookup"><span data-stu-id="07861-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="07861-188">**WbemFlagEnum**</span><span class="sxs-lookup"><span data-stu-id="07861-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
