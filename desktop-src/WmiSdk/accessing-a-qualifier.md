---
description: Um qualificador é uma marca que fornece mais informações sobre um objeto, método ou Propriedade do WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Acessando um qualificador WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786245"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="4f4ba-103">Acessando um qualificador WMI</span><span class="sxs-lookup"><span data-stu-id="4f4ba-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="4f4ba-104">Um qualificador é uma marca que fornece mais informações sobre um objeto, método ou Propriedade do WMI.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="4f4ba-105">Às vezes, talvez seja necessário acessar os dados armazenados em um qualificador.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="4f4ba-106">Por exemplo, uma tarefa comum é determinar se um provedor implementa um método ao tentar recuperar o qualificador **implementado** para esse método.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="4f4ba-107">Para obter mais informações, consulte [qualificadores WMI](wmi-qualifiers.md) e [adicionando um qualificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="4f4ba-108">Você pode recuperar os qualificadores em um objeto WMI no PowerShell recuperando primeiro o objeto e, em seguida, examinando os qualificadores como faria com qualquer outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="4f4ba-109">**Para recuperar um qualificador usando o PowerShell**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="4f4ba-110">Recupere o objeto cujos qualificadores você deseja exibir usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)e, em seguida, acesse os qualificadores por meio da propriedade **Qualifiers** :</span><span class="sxs-lookup"><span data-stu-id="4f4ba-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="4f4ba-111">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="4f4ba-112">Você pode recuperar os qualificadores em uma instância do WMI no C# recuperando primeiro o objeto e, em seguida, examinando os qualificadores como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="4f4ba-113">**Para recuperar um qualificador usando C# (Microsoft.System. Gerenciamento**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="4f4ba-114">Recupere a classe cujos qualificadores você deseja exibir criando um objeto CimInstance, usando o nome da classe e o namespace especificados.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="4f4ba-115">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="4f4ba-116">Você pode recuperar os qualificadores de classe de [ciminstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), os qualificadores de propriedade de [ciminstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))e os qualificadores de método de [ciminstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="4f4ba-117">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="4f4ba-118">Você pode recuperar os qualificadores em um objeto WMI em C# recuperando primeiro o objeto e, em seguida, examinando os qualificadores como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="4f4ba-119">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="4f4ba-120">**Para recuperar um qualificador usando C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="4f4ba-121">Recupere o objeto cujos qualificadores você deseja exibir usando [ManagementObject](/dotnet/api/system.management.managementobject).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="4f4ba-122">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="4f4ba-123">Coloque os qualificadores em um [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)e enumere os valores de [QualifierData](/dotnet/api/system.management.qualifierdata) .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="4f4ba-124">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="4f4ba-125">O procedimento a seguir descreve como recuperar um qualificador usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="4f4ba-126">**Para recuperar um qualificador usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="4f4ba-127">Recupere o objeto cujos qualificadores você deseja exibir, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="4f4ba-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="4f4ba-128">A maneira mais comum de recuperar um objeto é usando o método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="4f4ba-129">Para obter mais informações, consulte [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="4f4ba-130">Acesse os qualificadores do objeto por meio da propriedade [**SWbemObject. \_ Qualifiers**](swbemobject-qualifiers-.md) , conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="4f4ba-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="4f4ba-131">O exemplo de código a seguir descreve como acessar todos os qualificadores em um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="4f4ba-132">O procedimento a seguir descreve como recuperar um qualificador usando C++.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="4f4ba-133">**Para recuperar um qualificador usando C++**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="4f4ba-134">Recupere o objeto cujos qualificadores você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="4f4ba-135">A maneira mais comum de recuperar um objeto é usando uma chamada para [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="4f4ba-136">Para obter mais informações, consulte [recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="4f4ba-137">Recupere o qualificador definido para uma determinada propriedade com uma chamada para os métodos [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) ou [**IWbemClassObject:: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="4f4ba-138">Acesse os qualificadores do objeto por meio da interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) retornada.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="4f4ba-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f4ba-139">Examples</span></span>

<span data-ttu-id="4f4ba-140">Para obter mais informações sobre como recuperar qualificadores, consulte o exemplo de código do PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) na galeria do TechNet.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
