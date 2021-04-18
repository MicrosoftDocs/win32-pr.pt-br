---
description: Fazer uma chamada assíncrona para um método WMI ou um método de provedor permite que um script continue a ser executado enquanto os objetos retornam a um objeto SWbemSink e são manipulados por métodos como SWbemSink. OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Fazendo uma chamada assíncrona com o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810819"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="cc0fa-103">Fazendo uma chamada assíncrona com o VBScript</span><span class="sxs-lookup"><span data-stu-id="cc0fa-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="cc0fa-104">Fazer uma chamada assíncrona para um [*método WMI*](gloss-w.md) ou um [*método de provedor*](gloss-p.md) permite que um script continue a ser executado enquanto os objetos retornam a um objeto [**SWbemSink**](swbemsink.md) e são manipulados por métodos como [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="cc0fa-105">No entanto, as chamadas assíncronas não são recomendadas porque os dados podem não ser retornados no mesmo nível de segurança que a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="cc0fa-106">Ao usar chamadas de coletor assíncronas como [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para obter dados retornados, você pode definir o valor do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="cc0fa-107">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**</span><span class="sxs-lookup"><span data-stu-id="cc0fa-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="cc0fa-108">Definir esse valor de registro garante a autenticação dos objetos de dados retornados ao coletor.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="cc0fa-109">Se **UnsecAppAccessControlDefault** for definido como um (1), o WMI executará a verificação de acesso do retorno de dados.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="cc0fa-110">Verificações de acesso Verifique se os dados vêm da fonte correta.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="cc0fa-111">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="cc0fa-112">Métodos assíncronos com nomes que terminam em "Async \_ " sempre retornam imediatamente após serem chamados para que um programa possa continuar em execução.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="cc0fa-113">Por exemplo, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) é síncrono e bloqueia a execução até que todos os objetos sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="cc0fa-114">O método [**cQueryAsyncSWbemServices.Exe**](swbemservices-execqueryasync.md) é a versão assíncrona não bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="cc0fa-115">Uma maneira mais segura de fazer a chamada para **SWbemServices.Exe** o desbloqueio cQuery é fazendo a chamada [*semisynchronously*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="cc0fa-116">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md) e [fazendo uma chamada de Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="cc0fa-117">O parâmetro *iFlags* para chamadas assíncronas sempre assume como padrão zero (0).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="cc0fa-118">Os métodos assíncronos não fornecem uma coleção [**SWbemObjectSet**](swbemobjectset.md) para a sub-rotina Sink.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="cc0fa-119">Em vez disso, a sub-rotina de evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) em seu script ou aplicativo recebe cada objeto conforme ele é fornecido.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="cc0fa-120">Quando a chamada assíncrona original é concluída, ela chama o evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) do coletor de objetos e executa o código que você coloca ali para processar o resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="cc0fa-121">Uma página de Active Server (ASP) como um host de script não oferece suporte a uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="cc0fa-122">O procedimento a seguir descreve como fazer uma chamada assíncrona usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="cc0fa-123">**Para fazer uma chamada assíncrona usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="cc0fa-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="cc0fa-124">Conecte-se ao WMI e obtenha um objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="cc0fa-125">Crie o coletor de objetos usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ou (somente para o Windows Script Host 2,0) a marca de objeto com um atributo de eventos definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="cc0fa-126">– ou –</span><span class="sxs-lookup"><span data-stu-id="cc0fa-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="cc0fa-127">Crie uma sub-rotina para cada evento que um evento assíncrono pode disparar.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="cc0fa-128">Esses eventos são definidos como métodos em [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="cc0fa-129">Por exemplo, o WMI faz um retorno de chamada para [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) conforme cada instância retorna.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="cc0fa-130">Quando você cria a sub-rotina, coloca o código na sub-rotina para lidar com cada evento quando ele é recebido.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="cc0fa-131">Examine o parâmetro *iHresult* retornado pelo evento [**OnCompleted**](swbemsink-oncompleted.md) para determinar se a chamada assíncrona foi bem-sucedida ou se ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="cc0fa-132">Se for bem-sucedido, o valor passado no parâmetro *iHresult* será igual a zero (0).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="cc0fa-133">Qualquer outro valor pode indicar um erro e você deve verificar os valores no objeto de erro que é retornado no parâmetro *objErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="cc0fa-134">Faça uma chamada assíncrona e passe o nome do seu coletor no parâmetro *objWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="cc0fa-135">Faça uma chamada que impeça que o script termine antes que todos os eventos sejam recebidos.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="cc0fa-136">Se o script puder ser executado com uma interface de tela, uma maneira simples de fazer isso é usar um comando do WSH (Windows Script Host) `Echo` , que é mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="cc0fa-137">Ao executar esse script, você poderá ver a primeira instância retornar antes da mensagem **aguardando instâncias** ou poderá vê-la após.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="cc0fa-138">Essa é a natureza do processamento assíncrono.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="cc0fa-139">Se você fechar a caixa de mensagem **aguardando instâncias em** breve, talvez não veja todas as instâncias.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="cc0fa-140">Se você tiver resultados de várias chamadas assíncronas diferentes retornando ao mesmo coletor, armazene todos os dados de distinção necessários no parâmetro de contexto *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="cc0fa-141">Quando terminar com o coletor, cancele sua chamada assíncrona com o método [**Cancel**](swbemsink-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="cc0fa-142">O método [**Cancel**](swbemsink-cancel.md) INSTRUI o WSH a cancelar todas as chamadas assíncronas associadas a um determinado objeto de coletor.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="cc0fa-143">Portanto, talvez você queira usar coletores separados para operações assíncronas que devem ser independentes.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="cc0fa-144">Libere o objeto do coletor atribuindo o objeto de coletor a `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="cc0fa-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="cc0fa-145">O exemplo de código a seguir mostra uma consulta assíncrona para todas as instâncias do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) no computador local.</span><span class="sxs-lookup"><span data-stu-id="cc0fa-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="cc0fa-146">Para obter uma versão semisynchronous do mesmo método, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cc0fa-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="cc0fa-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc0fa-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc0fa-148">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="cc0fa-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="cc0fa-149">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="cc0fa-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
