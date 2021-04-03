---
description: Você pode exibir ou manipular todas as informações disponibilizadas por meio do WMI usando scripts.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Criando um script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922875"
---
# <a name="creating-a-wmi-script"></a>Criando um script WMI

Você pode exibir ou manipular todas as informações disponibilizadas por meio do WMI usando scripts. Os scripts podem ser escritos em qualquer linguagem de script que dê suporte à Hospedagem de script do Microsoft ActiveX, incluindo Visual Basic Scripting Edition (VBScript), PowerShell e Perl. O WSH (Windows Script Host), as páginas Active Server e o Internet Explorer podem todos os scripts WMI de host.

> [!Note]
>
> A linguagem de script primária com suporte no momento pelo WMI é o PowerShell. No entanto, o WMI também contém um corpo robusto de suporte a scripts para VBScript e outras linguagens que acessam a [API de script para WMI](scripting-api-for-wmi.md).

 

## <a name="wmi-scripting-languages"></a>Linguagens de script WMI

Os dois idiomas principais com suporte do WMI são PowerShell e VBScript (por meio do Windows Script Host ou do WSH).

-   O **PowerShell** foi projetado com forte integração com o WMI em mente. Dessa forma, grande parte dos elementos subjacentes do WMI são criados nos cmdlets do WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)e [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). A tabela a seguir descreve os processos gerais usados para acessar informações do WMI. Observe que, embora a maioria desses exemplos use Get-WMIObject, muitos dos cmdlets WMI do PowerShell têm os mesmos parâmetros, como *-Class* ou *-Credentials*. Portanto, muitos desses processos também funcionam para outros objetos. Para obter uma discussão mais detalhada sobre o PowerShell e o WMI, consulte [usando o Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) e [o Windows PowerShell-a conexão WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   O **VBScript**, por outro lado, faz chamadas explicitamente para a [API de script para WMI](scripting-api-for-wmi.md), conforme mencionado acima. Outras linguagens, como Perl, também podem usar a API de script para o WMI. No entanto, para os fins desta documentação, a maioria dos exemplos que demonstram a API de script para WMI usará o VBScript. No entanto, quando uma técnica de programação é específica do VBScript, ela será chamada.

    Essencialmente, o VBScript tem duas maneiras separadas de acessar o WMI. A primeira é usar um objeto [**SWbemLocator**](swbemlocator.md) para se conectar ao WMI. Como alternativa, você pode usar [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) e um moniker. Um moniker é uma cadeia de caracteres que pode descrever um número de elementos: suas credenciais, configurações de representação, em qual computador você deseja se conectar, o [*namespace*](gloss-n.md) WMI (ou seja, o local geral em que o WMI armazena grupos de objetos) e o objeto WMI que você deseja recuperar. Muitos dos exemplos a seguir descrevem as duas técnicas. Para obter mais informações, consulte [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md) e [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

    Independentemente de qual técnica você usa para se conectar ao WMI, você provavelmente vai recuperar um ou mais objetos da API de script. O mais comum é [**SWbemObject**](swbemobject.md), que o WMI usa para descrever um objeto WMI. Como alternativa, você pode usar um objeto [**SWbemServices**](swbemservices.md) para descrever o próprio serviço WMI ou um objeto [**SWbemObjectPath**](swbemobjectpath.md) para descrever o local de um objeto WMI. Para obter mais informações, consulte [scripts com](scripting-with-swbemobject.md) [objetos auxiliares SWbemObject e scripting](scripting-helper-objects.md).

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Usando o WMI e uma linguagem de script, como faço...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... conectar-se ao WMI?
</dt> <dd>

Para o VBScript e a API de script para WMI, recupere um objeto [**SWbemServices**](swbemservices.md) com um moniker e uma chamada para [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)). Como alternativa, você pode se conectar ao servidor com uma chamada para [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Em seguida, você pode usar o objeto para acessar um namespace WMI específico ou uma instância de classe WMI.

Para o PowerShell, a conexão ao WMI geralmente é feita diretamente na chamada de cmdlet; como tal, nenhuma etapa adicional é necessária.

Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md), [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md)e [conectando-se ao WMI com o VBScript](connecting-to-wmi-with-vbscript.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... recuperar informações do WMI?
</dt> <dd>

Para o VBScript e a API de script para WMI, use uma função de recuperação, como [**WbemServices. Get**](swbemservices-get.md) ou [**WbemServices. InstancesOf**](swbemservices-instancesof.md). Você também pode posicionar o nome da classe do objeto a ser recuperado em um moniker, o que pode ser mais eficiente.

Para o PowerShell, use o parâmetro *-Class* . Observe que-Class é o parâmetro padrão; assim, você não precisa defini-lo explicitamente.

Para obter mais informações, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... criar uma consulta WMI?
</dt> <dd>

Para o VBScript e a API de script para WMI, use o método [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .

Para o PowerShell, use o parâmetro *-Query* . Você também pode filtrar usando o parâmetro *-Filter* .

Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... enumerar por meio de uma lista de objetos WMI?
</dt> <dd>

Para o VBScript e a API de script para WMI, use o objeto de contêiner [**SWbemObjectSet**](swbemobjectset.md) , que é tratado no script como uma coleção que pode ser enumerada. Você pode recuperar um **SWbemObjectSet** de uma chamada de [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).

O PowerShell é capaz de recuperar e manipular enumerações como faria com qualquer outro objeto; Não há nada especialmente exclusivo para o WMI.

Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... acessar um namespace WMI diferente?
</dt> <dd>

Para o VBScript e a API de script para WMI, declare o namespace no moniker ou, caso contrário, você pode declarar explicitamente o namespace na chamada para [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

Para o PowerShell, use o parâmetro *-namespace* . O namespace padrão é "raiz \\ cimV2"; no entanto, muitas classes mais antigas são armazenadas em "raiz \\ padrão".

Para localizar o local de uma determinada classe WMI, examine a página de referência. Como alternativa, você pode explorar manualmente um namespace usando Get-WmiObject.


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... recuperar todas as instâncias filho de uma classe?
</dt> <dd>

Para idiomas que usam diretamente a API de script para WMI e PowerShell, o WMI dá suporte à recuperação de classes filho de uma classe base. Assim, para recuperar as instâncias filho, você precisa pesquisar somente a classe pai. O exemplo a seguir pesquisa [**o \_ LogicalDisk do CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), que é uma classe do WMI pré-instalado que representa discos lógicos em um sistema de computador baseado no Windows. Dessa forma, a pesquisa por essa classe pai também retorna instâncias [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que é o que o Windows usa para descrever discos rígidos. Para obter mais informações, consulte [modelo CIM](common-information-model.md). O WMI fornece um esquema inteiro de tais classes pré-instalados que permitem acessar e controlar objetos gerenciados. Para obter mais informações, consulte [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider) e [classes WMI](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... localizar um objeto WMI?
</dt> <dd>

Para a API de script para WMI e PowerShell, o WMI usa uma combinação de namespace, nome de classe e propriedades de chave para identificar exclusivamente uma determinada instância do WMI. Juntos, isso é conhecido como o caminho do objeto WMI. Para o VBScript, a propriedade [**SWbemObject \_ . Path**](swbemobject-path-.md) descreve o caminho para qualquer objeto dado retornado pela API de script. Para o PowerShell, cada objeto WMI terá uma \_ \_ propriedade Path. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md)

Além do namespace e do nome da classe, um objeto WMI também terá uma propriedade de chave, que identifica exclusivamente essa instância em comparação com outras instâncias em seu computador. Por exemplo, a propriedade **DeviceID** é a propriedade de chave para a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Para obter mais informações, consulte [formato MOF (MOF)](managed-object-format--mof-.md).

Por fim, o caminho relativo é simplesmente uma forma abreviada do caminho e inclui o nome da classe e o valor da chave. Nos exemplos abaixo, o caminho pode ser " \\ \\ NomeDoComputador \\ raiz \\ cimv2: Win32 \_ LogicalDisk. DeviceID =" d: "", enquanto o caminho relativo seria "" Win32LogicalDisk. DeviceID = "d" "".


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... definir informações no WMI?
</dt> <dd>

Para o VBScript e a API de script para WMI, use o método [**SWbemObject \_ . put**](swbemobject-put-.md) .

Para o PowerShell, você pode usar o método Put ou, caso contrário, [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

Para obter mais informações, consulte [modificando uma propriedade de instância](modifying-an-instance-property.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... usar credenciais diferentes?
</dt> <dd>

Para o VBScript e a API de script para WMI, use os parâmetros de *nome de usuário* e *senha* no método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

Para o PowerShell, use o parâmetro *-Credential* .

Observe que você só pode usar credenciais alternativas em um sistema remoto. Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... acessar um computador remoto?
</dt> <dd>

Para o VBScript e a API de script para WMI, declare explicitamente o nome do computador no moniker ou, caso contrário, na chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Para obter mais informações, consulte [conectando-se ao WMI remotamente com o VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Para o PowerShell, use o parâmetro *-ComputerName* . Para obter mais informações, consulte [conectando-se ao WMI remotamente com o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... definir os níveis de autenticação e representação?
</dt> <dd>

Para o VBScript e a API de script para WMI, use a propriedade [**SWbemServices \_ . Security**](swbemlocator-security-.md) no objeto de servidor retornado, ou então defina os valores relevantes no moniker.

Para o PowerShell, use os parâmetros *-Authentication* e *-Impersonation* , respectivamente. Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).

Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... tratar erros no WMI?
</dt> <dd>

Para a API de script do WMI, o provedor pode fornecer um objeto [**SWbemLastError**](swbemlasterror.md) para fornecer mais informações sobre um erro.

No VBScript em particular, o tratamento de erros também tem suporte usando o objeto de **erro** nativo. Você também pode acessar o objeto [**SWbemLastError**](swbemlasterror.md), conforme descrito acima. Para obter mais informações, consulte [recuperando um código de erro](retrieving-an-error-code.md).

Para o PowerShell, você pode usar as técnicas padrão de tratamento de erros do PowerShell. Para obter mais informações, consulte [uma introdução ao tratamento de erros no PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
