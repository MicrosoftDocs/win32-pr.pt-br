---
description: Um método de provedor é um método que é implementado por um provedor de Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Chamando um método de provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763935"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="03b54-103">Chamando um método de provedor</span><span class="sxs-lookup"><span data-stu-id="03b54-103">Calling a Provider Method</span></span>

<span data-ttu-id="03b54-104">Um método de provedor é um método que é implementado por um provedor de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="03b54-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="03b54-105">O método é encontrado em uma classe definida por um provedor para representar dados de software ou hardware.</span><span class="sxs-lookup"><span data-stu-id="03b54-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="03b54-106">Por exemplo, a classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) tem métodos para iniciar, parar, retomar, pausar e alterar serviços.</span><span class="sxs-lookup"><span data-stu-id="03b54-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="03b54-107">Os métodos de provedor não devem ser confundidos com os seguintes tipos de métodos:</span><span class="sxs-lookup"><span data-stu-id="03b54-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="03b54-108">Métodos em [classes de sistema WMI](wmi-system-classes.md), [**como o método**](--systemsecurity-getsd.md) Obtido em [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="03b54-109">Métodos em objetos na [API de script para WMI](scripting-api-for-wmi.md), como [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="03b54-110">Métodos na [API com para WMI](com-api-for-wmi.md), como [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="03b54-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="03b54-111">Chamando um método de provedor usando scripts</span><span class="sxs-lookup"><span data-stu-id="03b54-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="03b54-112">Qualquer linguagem de automação, como VBScript, PowerShell ou Perl, pode chamar um método WMI.</span><span class="sxs-lookup"><span data-stu-id="03b54-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="03b54-113">Algumas linguagens podem usar o [acesso direto](/windows), mas outras devem usar [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para executar o método de provedor indiretamente.</span><span class="sxs-lookup"><span data-stu-id="03b54-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="03b54-114">O procedimento a seguir descreve como chamar um método de provedor usando a API de script e usando o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="03b54-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="03b54-115">**Para chamar um método de provedor usando a API de script e o acesso direto**</span><span class="sxs-lookup"><span data-stu-id="03b54-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="03b54-116">Use essa abordagem para VBScript ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="03b54-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="03b54-117">Determine se o método que você deseja executar é implementado.</span><span class="sxs-lookup"><span data-stu-id="03b54-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="03b54-118">Algumas classes têm métodos definidos que não têm suporte de um provedor.</span><span class="sxs-lookup"><span data-stu-id="03b54-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="03b54-119">Se um método não for implementado, você não poderá executá-lo.</span><span class="sxs-lookup"><span data-stu-id="03b54-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="03b54-120">Você pode determinar se um método é implementado verificando se o método tem o qualificador [**implementado**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="03b54-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="03b54-121">Para obter mais informações, consulte [qualificadores WMI](wmi-qualifiers.md) e [acessando um qualificador WMI](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="03b54-122">Você também pode determinar se um método de classe de provedor tem o qualificador **implementado** definido executando o utilitário de Wbemtest.exe sem suporte, disponível em qualquer sistema operacional com o WMI instalado.</span><span class="sxs-lookup"><span data-stu-id="03b54-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="03b54-123">Determine se o método que você deseja executar é um [*método estático*](gloss-s.md) ou não estático.</span><span class="sxs-lookup"><span data-stu-id="03b54-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="03b54-124">Os métodos estáticos se aplicam somente a classes WMI e não a instâncias específicas de uma classe.</span><span class="sxs-lookup"><span data-stu-id="03b54-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="03b54-125">Por exemplo, o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe [**\_ process do Win32**](/windows/desktop/CIMWin32Prov/win32-process) é um método estático, pois use-o para criar um novo processo sem uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="03b54-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="03b54-126">Os métodos não estáticos se aplicam somente a instâncias de uma classe.</span><span class="sxs-lookup"><span data-stu-id="03b54-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="03b54-127">Por exemplo, o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) da classe **\_ process do Win32** é um método não estático, pois faz sentido finalizar um processo se existir uma instância desse processo.</span><span class="sxs-lookup"><span data-stu-id="03b54-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="03b54-128">Você pode determinar se um método é estático verificando se o qualificador [**estático**](standard-wmi-qualifiers.md) está associado ao método.</span><span class="sxs-lookup"><span data-stu-id="03b54-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="03b54-129">Recupere a classe ou instância que contém o método que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="03b54-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="03b54-130">Para obter mais informações, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="03b54-131">Defina as configurações de segurança que o método pode exigir.</span><span class="sxs-lookup"><span data-stu-id="03b54-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="03b54-132">Geralmente, você pode determinar os privilégios que um método requer examinando os valores no qualificador [**Privileges**](swbemsecurity-privileges.md) do método.</span><span class="sxs-lookup"><span data-stu-id="03b54-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="03b54-133">Por exemplo, o método de [**desligamento**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) de classe do [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requer que você defina o privilégio "SeShutdownPrivilege".</span><span class="sxs-lookup"><span data-stu-id="03b54-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="03b54-134">Para obter mais informações, consulte [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="03b54-135">Chame o método e examine o valor de retorno para determinar se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="03b54-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="03b54-136">O exemplo de código a seguir cria um processo do bloco de notas e obtém a ID do processo usando o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="03b54-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="03b54-137">O procedimento a seguir descreve como chamar um método de provedor usando a API de script e o [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="03b54-138">**Para chamar um método de provedor usando a API de script e SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="03b54-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="03b54-139">Recupere a definição de classe WMI para executar um método estático.</span><span class="sxs-lookup"><span data-stu-id="03b54-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="03b54-140">Recupere a instância da classe WMI para executar um método não estático.</span><span class="sxs-lookup"><span data-stu-id="03b54-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="03b54-141">Recupere o método a ser executado da coleção [**SWbemObject. \_ Methods**](swbemobject-methods-.md) de sua classe ou instância usando o método [**SWbemObjectSet. Item**](swbemobjectset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="03b54-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="03b54-142">Obtenha um objeto de [**inparâmetros**](swbemmethod-inparameters.md) para o método e configure os parâmetros conforme descrito em [construindo objetos de inparâmetros](constructing-inparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="03b54-143">Chame o método **SWbemServices.ExecMethod** para executar e atribuir o valor de retorno a um objeto [**SWbemObject**](swbemobject.md) para armazenar os parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="03b54-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="03b54-144">Verifique os valores no objeto de parâmetros de saída para verificar se o método foi executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="03b54-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="03b54-145">O exemplo de código VBScript a seguir executa a mesma operação que o script anterior pela abordagem indireta por meio da chamada de [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="03b54-146">O procedimento a seguir descreve como chamar um método de provedor usando C++.</span><span class="sxs-lookup"><span data-stu-id="03b54-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="03b54-147">**Para chamar um método de provedor usando C++**</span><span class="sxs-lookup"><span data-stu-id="03b54-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="03b54-148">Conecte-se ao WMI.</span><span class="sxs-lookup"><span data-stu-id="03b54-148">Connect to WMI.</span></span>

    <span data-ttu-id="03b54-149">Para chamar um método no WMI, primeiro você deve ter uma conexão em funcionamento com um namespace do WMI.</span><span class="sxs-lookup"><span data-stu-id="03b54-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="03b54-150">Para obter mais informações, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md) e [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="03b54-151">O exemplo a seguir mostra como se conectar ao WMI.</span><span class="sxs-lookup"><span data-stu-id="03b54-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="03b54-152">Para obter mais informações sobre problemas de segurança nas chamadas do provedor WMI, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="03b54-153">Chame [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar a definição da classe do método que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="03b54-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="03b54-154">O método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a definição de classe.</span><span class="sxs-lookup"><span data-stu-id="03b54-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="03b54-155">Para métodos que exigem parâmetros de entrada, chame o método [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para obter o objeto de classe de parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="03b54-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="03b54-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a classe de parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="03b54-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="03b54-157">Gere uma instância da classe de parâmetro de entrada com uma chamada para o método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="03b54-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="03b54-158">Defina as propriedades da classe de parâmetro de entrada com uma chamada para o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="03b54-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="03b54-159">Invoque o método com uma chamada para [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="03b54-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="03b54-160">Para [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), o WMI retorna quaisquer parâmetros de saída na chamada.</span><span class="sxs-lookup"><span data-stu-id="03b54-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="03b54-161">Para [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), o WMI retorna quaisquer parâmetros de saída por meio de uma chamada para [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="03b54-162">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="03b54-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="03b54-163">O código a seguir é um exemplo completo para chamar um método de provedor.</span><span class="sxs-lookup"><span data-stu-id="03b54-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="03b54-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03b54-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b54-165">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="03b54-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
