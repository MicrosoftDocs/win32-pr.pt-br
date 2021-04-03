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
# <a name="creating-a-wmi-script"></a><span data-ttu-id="91518-103">Criando um script WMI</span><span class="sxs-lookup"><span data-stu-id="91518-103">Creating a WMI Script</span></span>

<span data-ttu-id="91518-104">Você pode exibir ou manipular todas as informações disponibilizadas por meio do WMI usando scripts.</span><span class="sxs-lookup"><span data-stu-id="91518-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="91518-105">Os scripts podem ser escritos em qualquer linguagem de script que dê suporte à Hospedagem de script do Microsoft ActiveX, incluindo Visual Basic Scripting Edition (VBScript), PowerShell e Perl.</span><span class="sxs-lookup"><span data-stu-id="91518-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="91518-106">O WSH (Windows Script Host), as páginas Active Server e o Internet Explorer podem todos os scripts WMI de host.</span><span class="sxs-lookup"><span data-stu-id="91518-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="91518-107">A linguagem de script primária com suporte no momento pelo WMI é o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91518-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="91518-108">No entanto, o WMI também contém um corpo robusto de suporte a scripts para VBScript e outras linguagens que acessam a [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91518-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="91518-109">Linguagens de script WMI</span><span class="sxs-lookup"><span data-stu-id="91518-109">WMI Scripting Languages</span></span>

<span data-ttu-id="91518-110">Os dois idiomas principais com suporte do WMI são PowerShell e VBScript (por meio do Windows Script Host ou do WSH).</span><span class="sxs-lookup"><span data-stu-id="91518-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="91518-111">O **PowerShell** foi projetado com forte integração com o WMI em mente.</span><span class="sxs-lookup"><span data-stu-id="91518-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="91518-112">Dessa forma, grande parte dos elementos subjacentes do WMI são criados nos cmdlets do WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)e [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="91518-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="91518-113">A tabela a seguir descreve os processos gerais usados para acessar informações do WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="91518-114">Observe que, embora a maioria desses exemplos use Get-WMIObject, muitos dos cmdlets WMI do PowerShell têm os mesmos parâmetros, como *-Class* ou *-Credentials*.</span><span class="sxs-lookup"><span data-stu-id="91518-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="91518-115">Portanto, muitos desses processos também funcionam para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="91518-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="91518-116">Para obter uma discussão mais detalhada sobre o PowerShell e o WMI, consulte [usando o Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) e [o Windows PowerShell-a conexão WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="91518-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="91518-117">O **VBScript**, por outro lado, faz chamadas explicitamente para a [API de script para WMI](scripting-api-for-wmi.md), conforme mencionado acima.</span><span class="sxs-lookup"><span data-stu-id="91518-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="91518-118">Outras linguagens, como Perl, também podem usar a API de script para o WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="91518-119">No entanto, para os fins desta documentação, a maioria dos exemplos que demonstram a API de script para WMI usará o VBScript.</span><span class="sxs-lookup"><span data-stu-id="91518-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="91518-120">No entanto, quando uma técnica de programação é específica do VBScript, ela será chamada.</span><span class="sxs-lookup"><span data-stu-id="91518-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="91518-121">Essencialmente, o VBScript tem duas maneiras separadas de acessar o WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="91518-122">A primeira é usar um objeto [**SWbemLocator**](swbemlocator.md) para se conectar ao WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="91518-123">Como alternativa, você pode usar [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) e um moniker.</span><span class="sxs-lookup"><span data-stu-id="91518-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="91518-124">Um moniker é uma cadeia de caracteres que pode descrever um número de elementos: suas credenciais, configurações de representação, em qual computador você deseja se conectar, o [*namespace*](gloss-n.md) WMI (ou seja, o local geral em que o WMI armazena grupos de objetos) e o objeto WMI que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="91518-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="91518-125">Muitos dos exemplos a seguir descrevem as duas técnicas.</span><span class="sxs-lookup"><span data-stu-id="91518-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="91518-126">Para obter mais informações, consulte [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md) e [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="91518-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="91518-127">Independentemente de qual técnica você usa para se conectar ao WMI, você provavelmente vai recuperar um ou mais objetos da API de script.</span><span class="sxs-lookup"><span data-stu-id="91518-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="91518-128">O mais comum é [**SWbemObject**](swbemobject.md), que o WMI usa para descrever um objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="91518-129">Como alternativa, você pode usar um objeto [**SWbemServices**](swbemservices.md) para descrever o próprio serviço WMI ou um objeto [**SWbemObjectPath**](swbemobjectpath.md) para descrever o local de um objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="91518-130">Para obter mais informações, consulte [scripts com](scripting-with-swbemobject.md) [objetos auxiliares SWbemObject e scripting](scripting-helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="91518-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="91518-131">Usando o WMI e uma linguagem de script, como faço...</span><span class="sxs-lookup"><span data-stu-id="91518-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="91518-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... conectar-se ao WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="91518-133">Para o VBScript e a API de script para WMI, recupere um objeto [**SWbemServices**](swbemservices.md) com um moniker e uma chamada para [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span><span class="sxs-lookup"><span data-stu-id="91518-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="91518-134">Como alternativa, você pode se conectar ao servidor com uma chamada para [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="91518-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="91518-135">Em seguida, você pode usar o objeto para acessar um namespace WMI específico ou uma instância de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="91518-136">Para o PowerShell, a conexão ao WMI geralmente é feita diretamente na chamada de cmdlet; como tal, nenhuma etapa adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="91518-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="91518-137">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md), [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md)e [conectando-se ao WMI com o VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="91518-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


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

<span data-ttu-id="91518-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... recuperar informações do WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="91518-139">Para o VBScript e a API de script para WMI, use uma função de recuperação, como [**WbemServices. Get**](swbemservices-get.md) ou [**WbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="91518-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="91518-140">Você também pode posicionar o nome da classe do objeto a ser recuperado em um moniker, o que pode ser mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="91518-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="91518-141">Para o PowerShell, use o parâmetro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="91518-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="91518-142">Observe que-Class é o parâmetro padrão; assim, você não precisa defini-lo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="91518-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="91518-143">Para obter mais informações, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="91518-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


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

<span data-ttu-id="91518-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... criar uma consulta WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="91518-145">Para o VBScript e a API de script para WMI, use o método [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .</span><span class="sxs-lookup"><span data-stu-id="91518-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="91518-146">Para o PowerShell, use o parâmetro *-Query* .</span><span class="sxs-lookup"><span data-stu-id="91518-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="91518-147">Você também pode filtrar usando o parâmetro *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="91518-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="91518-148">Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91518-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


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

<span data-ttu-id="91518-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... enumerar por meio de uma lista de objetos WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="91518-150">Para o VBScript e a API de script para WMI, use o objeto de contêiner [**SWbemObjectSet**](swbemobjectset.md) , que é tratado no script como uma coleção que pode ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="91518-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="91518-151">Você pode recuperar um **SWbemObjectSet** de uma chamada de [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="91518-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="91518-152">O PowerShell é capaz de recuperar e manipular enumerações como faria com qualquer outro objeto; Não há nada especialmente exclusivo para o WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="91518-153">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="91518-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


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

<span data-ttu-id="91518-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... acessar um namespace WMI diferente?</span><span class="sxs-lookup"><span data-stu-id="91518-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="91518-155">Para o VBScript e a API de script para WMI, declare o namespace no moniker ou, caso contrário, você pode declarar explicitamente o namespace na chamada para [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="91518-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="91518-156">Para o PowerShell, use o parâmetro *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="91518-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="91518-157">O namespace padrão é "raiz \\ cimV2"; no entanto, muitas classes mais antigas são armazenadas em "raiz \\ padrão".</span><span class="sxs-lookup"><span data-stu-id="91518-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="91518-158">Para localizar o local de uma determinada classe WMI, examine a página de referência.</span><span class="sxs-lookup"><span data-stu-id="91518-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="91518-159">Como alternativa, você pode explorar manualmente um namespace usando Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="91518-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


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

<span data-ttu-id="91518-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... recuperar todas as instâncias filho de uma classe?</span><span class="sxs-lookup"><span data-stu-id="91518-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="91518-161">Para idiomas que usam diretamente a API de script para WMI e PowerShell, o WMI dá suporte à recuperação de classes filho de uma classe base.</span><span class="sxs-lookup"><span data-stu-id="91518-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="91518-162">Assim, para recuperar as instâncias filho, você precisa pesquisar somente a classe pai.</span><span class="sxs-lookup"><span data-stu-id="91518-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="91518-163">O exemplo a seguir pesquisa [**o \_ LogicalDisk do CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), que é uma classe do WMI pré-instalado que representa discos lógicos em um sistema de computador baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="91518-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="91518-164">Dessa forma, a pesquisa por essa classe pai também retorna instâncias [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que é o que o Windows usa para descrever discos rígidos.</span><span class="sxs-lookup"><span data-stu-id="91518-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="91518-165">Para obter mais informações, consulte [modelo CIM](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="91518-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="91518-166">O WMI fornece um esquema inteiro de tais classes pré-instalados que permitem acessar e controlar objetos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="91518-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="91518-167">Para obter mais informações, consulte [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider) e [classes WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="91518-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="91518-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... localizar um objeto WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="91518-169">Para a API de script para WMI e PowerShell, o WMI usa uma combinação de namespace, nome de classe e propriedades de chave para identificar exclusivamente uma determinada instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="91518-170">Juntos, isso é conhecido como o caminho do objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="91518-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="91518-171">Para o VBScript, a propriedade [**SWbemObject \_ . Path**](swbemobject-path-.md) descreve o caminho para qualquer objeto dado retornado pela API de script.</span><span class="sxs-lookup"><span data-stu-id="91518-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="91518-172">Para o PowerShell, cada objeto WMI terá uma \_ \_ propriedade Path.</span><span class="sxs-lookup"><span data-stu-id="91518-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="91518-173">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="91518-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="91518-174">Além do namespace e do nome da classe, um objeto WMI também terá uma propriedade de chave, que identifica exclusivamente essa instância em comparação com outras instâncias em seu computador.</span><span class="sxs-lookup"><span data-stu-id="91518-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="91518-175">Por exemplo, a propriedade **DeviceID** é a propriedade de chave para a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="91518-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="91518-176">Para obter mais informações, consulte [formato MOF (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="91518-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="91518-177">Por fim, o caminho relativo é simplesmente uma forma abreviada do caminho e inclui o nome da classe e o valor da chave.</span><span class="sxs-lookup"><span data-stu-id="91518-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="91518-178">Nos exemplos abaixo, o caminho pode ser " \\ \\ NomeDoComputador \\ raiz \\ cimv2: Win32 \_ LogicalDisk. DeviceID =" d: "", enquanto o caminho relativo seria "" Win32LogicalDisk. DeviceID = "d" "".</span><span class="sxs-lookup"><span data-stu-id="91518-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


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

<span data-ttu-id="91518-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... definir informações no WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="91518-180">Para o VBScript e a API de script para WMI, use o método [**SWbemObject \_ . put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="91518-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="91518-181">Para o PowerShell, você pode usar o método Put ou, caso contrário, [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="91518-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="91518-182">Para obter mais informações, consulte [modificando uma propriedade de instância](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="91518-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


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

<span data-ttu-id="91518-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... usar credenciais diferentes?</span><span class="sxs-lookup"><span data-stu-id="91518-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="91518-184">Para o VBScript e a API de script para WMI, use os parâmetros de *nome de usuário* e *senha* no método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="91518-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="91518-185">Para o PowerShell, use o parâmetro *-Credential* .</span><span class="sxs-lookup"><span data-stu-id="91518-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="91518-186">Observe que você só pode usar credenciais alternativas em um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="91518-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="91518-187">Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="91518-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


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

<span data-ttu-id="91518-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... acessar um computador remoto?</span><span class="sxs-lookup"><span data-stu-id="91518-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="91518-189">Para o VBScript e a API de script para WMI, declare explicitamente o nome do computador no moniker ou, caso contrário, na chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="91518-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="91518-190">Para obter mais informações, consulte [conectando-se ao WMI remotamente com o VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="91518-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="91518-191">Para o PowerShell, use o parâmetro *-ComputerName* .</span><span class="sxs-lookup"><span data-stu-id="91518-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="91518-192">Para obter mais informações, consulte [conectando-se ao WMI remotamente com o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="91518-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


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

<span data-ttu-id="91518-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... definir os níveis de autenticação e representação?</span><span class="sxs-lookup"><span data-stu-id="91518-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="91518-194">Para o VBScript e a API de script para WMI, use a propriedade [**SWbemServices \_ . Security**](swbemlocator-security-.md) no objeto de servidor retornado, ou então defina os valores relevantes no moniker.</span><span class="sxs-lookup"><span data-stu-id="91518-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="91518-195">Para o PowerShell, use os parâmetros *-Authentication* e *-Impersonation* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="91518-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="91518-196">Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="91518-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="91518-197">Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="91518-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


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

<span data-ttu-id="91518-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... tratar erros no WMI?</span><span class="sxs-lookup"><span data-stu-id="91518-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="91518-199">Para a API de script do WMI, o provedor pode fornecer um objeto [**SWbemLastError**](swbemlasterror.md) para fornecer mais informações sobre um erro.</span><span class="sxs-lookup"><span data-stu-id="91518-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="91518-200">No VBScript em particular, o tratamento de erros também tem suporte usando o objeto de **erro** nativo.</span><span class="sxs-lookup"><span data-stu-id="91518-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="91518-201">Você também pode acessar o objeto [**SWbemLastError**](swbemlasterror.md), conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="91518-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="91518-202">Para obter mais informações, consulte [recuperando um código de erro](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="91518-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="91518-203">Para o PowerShell, você pode usar as técnicas padrão de tratamento de erros do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91518-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="91518-204">Para obter mais informações, consulte [uma introdução ao tratamento de erros no PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="91518-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


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

 

 
