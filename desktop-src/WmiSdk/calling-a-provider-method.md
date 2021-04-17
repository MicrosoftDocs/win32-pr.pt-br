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
# <a name="calling-a-provider-method"></a>Chamando um método de provedor

Um método de provedor é um método que é implementado por um provedor de Instrumentação de Gerenciamento do Windows (WMI). O método é encontrado em uma classe definida por um provedor para representar dados de software ou hardware. Por exemplo, a classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) tem métodos para iniciar, parar, retomar, pausar e alterar serviços.

Os métodos de provedor não devem ser confundidos com os seguintes tipos de métodos:

-   Métodos em [classes de sistema WMI](wmi-system-classes.md), [**como o método**](--systemsecurity-getsd.md) Obtido em [**\_ \_ SystemSecurity**](--systemsecurity.md).
-   Métodos em objetos na [API de script para WMI](scripting-api-for-wmi.md), como [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).
-   Métodos na [API com para WMI](com-api-for-wmi.md), como [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

## <a name="calling-a-provider-method-using-scripting"></a>Chamando um método de provedor usando scripts

Qualquer linguagem de automação, como VBScript, PowerShell ou Perl, pode chamar um método WMI. Algumas linguagens podem usar o [acesso direto](/windows), mas outras devem usar [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para executar o método de provedor indiretamente.

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

O procedimento a seguir descreve como chamar um método de provedor usando a API de script e usando o acesso direto.

**Para chamar um método de provedor usando a API de script e o acesso direto**

1.  Use essa abordagem para VBScript ou PowerShell.
2.  Determine se o método que você deseja executar é implementado.

    Algumas classes têm métodos definidos que não têm suporte de um provedor. Se um método não for implementado, você não poderá executá-lo. Você pode determinar se um método é implementado verificando se o método tem o qualificador [**implementado**](standard-wmi-qualifiers.md) . Para obter mais informações, consulte [qualificadores WMI](wmi-qualifiers.md) e [acessando um qualificador WMI](accessing-a-qualifier.md). Você também pode determinar se um método de classe de provedor tem o qualificador **implementado** definido executando o utilitário de Wbemtest.exe sem suporte, disponível em qualquer sistema operacional com o WMI instalado.

3.  Determine se o método que você deseja executar é um [*método estático*](gloss-s.md) ou não estático.

    Os métodos estáticos se aplicam somente a classes WMI e não a instâncias específicas de uma classe. Por exemplo, o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe [**\_ process do Win32**](/windows/desktop/CIMWin32Prov/win32-process) é um método estático, pois use-o para criar um novo processo sem uma instância dessa classe. Os métodos não estáticos se aplicam somente a instâncias de uma classe. Por exemplo, o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) da classe **\_ process do Win32** é um método não estático, pois faz sentido finalizar um processo se existir uma instância desse processo. Você pode determinar se um método é estático verificando se o qualificador [**estático**](standard-wmi-qualifiers.md) está associado ao método.

4.  Recupere a classe ou instância que contém o método que você deseja executar.

    Para obter mais informações, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).

5.  Defina as configurações de segurança que o método pode exigir.

    Geralmente, você pode determinar os privilégios que um método requer examinando os valores no qualificador [**Privileges**](swbemsecurity-privileges.md) do método. Por exemplo, o método de [**desligamento**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) de classe do [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requer que você defina o privilégio "SeShutdownPrivilege". Para obter mais informações, consulte [executando operações privilegiadas](executing-privileged-operations.md).

6.  Chame o método e examine o valor de retorno para determinar se o método foi bem-sucedido.

O exemplo de código a seguir cria um processo do bloco de notas e obtém a ID do processo usando o acesso direto.


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

O procedimento a seguir descreve como chamar um método de provedor usando a API de script e o [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

**Para chamar um método de provedor usando a API de script e SWbemServices.ExecMethod**

1.  Recupere a definição de classe WMI para executar um método estático. Recupere a instância da classe WMI para executar um método não estático.
2.  Recupere o método a ser executado da coleção [**SWbemObject. \_ Methods**](swbemobject-methods-.md) de sua classe ou instância usando o método [**SWbemObjectSet. Item**](swbemobjectset-item.md) .
3.  Obtenha um objeto de [**inparâmetros**](swbemmethod-inparameters.md) para o método e configure os parâmetros conforme descrito em [construindo objetos de inparâmetros](constructing-inparameters-objects.md).
4.  Chame o método **SWbemServices.ExecMethod** para executar e atribuir o valor de retorno a um objeto [**SWbemObject**](swbemobject.md) para armazenar os parâmetros de saída.
5.  Verifique os valores no objeto de parâmetros de saída para verificar se o método foi executado corretamente.

O exemplo de código VBScript a seguir executa a mesma operação que o script anterior pela abordagem indireta por meio da chamada de [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).


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




O procedimento a seguir descreve como chamar um método de provedor usando C++.

**Para chamar um método de provedor usando C++**

1.  Conecte-se ao WMI.

    Para chamar um método no WMI, primeiro você deve ter uma conexão em funcionamento com um namespace do WMI. Para obter mais informações, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md) e [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

    O exemplo a seguir mostra como se conectar ao WMI. Para obter mais informações sobre problemas de segurança nas chamadas do provedor WMI, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

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

    

2.  Chame [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar a definição da classe do método que você deseja chamar.

    O método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a definição de classe.

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  Para métodos que exigem parâmetros de entrada, chame o método [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para obter o objeto de classe de parâmetro de entrada.

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a classe de parâmetro de entrada.

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  Gere uma instância da classe de parâmetro de entrada com uma chamada para o método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  Defina as propriedades da classe de parâmetro de entrada com uma chamada para o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  Invoque o método com uma chamada para [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).

    Para [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), o WMI retorna quaisquer parâmetros de saída na chamada. Para [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), o WMI retorna quaisquer parâmetros de saída por meio de uma chamada para [**IWbemObjectSink**](iwbemobjectsink.md). Para obter mais informações, consulte [chamando um método](calling-a-method.md).

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

O código a seguir é um exemplo completo para chamar um método de provedor.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
