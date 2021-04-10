---
description: Recuperar uma instância é um dos procedimentos de recuperação mais comuns que você provavelmente executará no WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Recuperando uma instância do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011754"
---
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="942d5-103">Recuperando uma instância do WMI</span><span class="sxs-lookup"><span data-stu-id="942d5-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="942d5-104">Recuperar uma instância é um dos procedimentos de recuperação mais comuns que você provavelmente executará no WMI.</span><span class="sxs-lookup"><span data-stu-id="942d5-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="942d5-105">Você pode recuperar uma instância existente ou criar uma nova instância sem nome.</span><span class="sxs-lookup"><span data-stu-id="942d5-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="942d5-106">O caminho do WMI para a instância existente é um parâmetro necessário.</span><span class="sxs-lookup"><span data-stu-id="942d5-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="942d5-107">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="942d5-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="942d5-108">Ao fornecer uma instância, um provedor pode não ser capaz de fornecer um valor para determinadas propriedades.</span><span class="sxs-lookup"><span data-stu-id="942d5-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="942d5-109">A menos que indicado de outra forma na descrição da propriedade, você não pode inferir nenhum significado de um valor vazio.</span><span class="sxs-lookup"><span data-stu-id="942d5-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="942d5-110">Isso não deve ser confundido com uma cadeia de caracteres que tem um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="942d5-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="942d5-111">Nesse caso, o valor é populado.</span><span class="sxs-lookup"><span data-stu-id="942d5-111">In this case, the value is populated.</span></span> <span data-ttu-id="942d5-112">Ele está vazio, mas tem um valor: **NULL**.</span><span class="sxs-lookup"><span data-stu-id="942d5-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="942d5-113">Recupere uma cópia local da instância com uma chamada para o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="942d5-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="942d5-114">**Para recuperar uma instância de uma classe WMI usando o PowerShell**</span><span class="sxs-lookup"><span data-stu-id="942d5-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="942d5-115">Você pode recuperar instâncias específicas usando os parâmetros *-Class* e *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="942d5-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="942d5-116">Você pode recuperar uma instância do WMI usando C# criando um objeto de pesquisa usando [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))e, em seguida, preenchendo-o com os valores de chave relevantes e, em seguida, procurando esse objeto com uma chamada [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="942d5-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="942d5-117">**Para recuperar uma instância de uma classe WMI usando C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="942d5-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="942d5-118">Usando o namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , crie um novo objeto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) com o nome e o namespace da classe relevante.</span><span class="sxs-lookup"><span data-stu-id="942d5-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="942d5-119">Crie um [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) que contenha o nome e o valor da propriedade de chave da instância que você deseja pesquisar e adicione essa propriedade ao seu objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="942d5-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="942d5-120">Recupere o objeto do WMI com uma chamada [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="942d5-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="942d5-121">Você pode recuperar uma instância de classe WMI específica ou uma coleção de instâncias de classe WMI, usando classes no namespace [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="942d5-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="942d5-122">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="942d5-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="942d5-123">**Para recuperar uma instância de uma classe WMI usando C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="942d5-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="942d5-124">Recupere uma cópia local de uma instância específica criando um novo [ManagementObject](/dotnet/api/system.management.managementobject), com o nome e o valor de instância específico transmitidos, embora o parâmetro *ManagementPath* .</span><span class="sxs-lookup"><span data-stu-id="942d5-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="942d5-125">Em seguida, você pode recuperar os dados da instância chamando explicitamente [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="942d5-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="942d5-126">Como alternativa, você pode recuperar todas as instâncias de uma classe WMI pesquisando-as com um [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)e enumerando por meio do [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)retornado.</span><span class="sxs-lookup"><span data-stu-id="942d5-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    <span data-ttu-id="942d5-127">Você pode chamar implicitamente o método **Get** acessando a instância.</span><span class="sxs-lookup"><span data-stu-id="942d5-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="942d5-128">Para obter mais informações, consulte [recuperando parte de uma instância do WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="942d5-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="942d5-129">Recupere uma cópia local da instância com uma chamada para o método VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="942d5-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="942d5-130">**Para recuperar uma instância de uma classe WMI usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="942d5-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="942d5-131">Chame [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) com o caminho do objeto da instância, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="942d5-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="942d5-132">A recuperação de uma instância específica requer o fornecimento de um nome como parte do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="942d5-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="942d5-133">Em C++, chame [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="942d5-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="942d5-134">**Para recuperar uma instância de uma classe WMI usando C++**</span><span class="sxs-lookup"><span data-stu-id="942d5-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="942d5-135">Recupere uma cópia local da instância com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="942d5-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="942d5-136">O caminho do WMI para o objeto deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="942d5-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="942d5-137">Como o nome indica, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera a instância de forma assíncrona, enquanto [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera a instância de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="942d5-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="942d5-138">Se você quiser usar a recuperação assíncrona, deverá implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="942d5-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="942d5-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="942d5-139">Examples</span></span>

<span data-ttu-id="942d5-140">Para obter um exemplo de VBScript a ser usado como modelo para recuperar informações de classe e instância, consulte o exemplo de [script de modelo WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) na galeria do TechNet.</span><span class="sxs-lookup"><span data-stu-id="942d5-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="942d5-141">Esse exemplo específico usa GetObject para recuperar o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="942d5-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 
