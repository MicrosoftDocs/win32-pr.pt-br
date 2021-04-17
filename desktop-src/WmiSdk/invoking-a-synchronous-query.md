---
description: Uma consulta síncrona é uma consulta que mantém o controle sobre o processo de seu aplicativo durante a consulta.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Invocando uma consulta síncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780087"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="cba82-103">Invocando uma consulta síncrona</span><span class="sxs-lookup"><span data-stu-id="cba82-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="cba82-104">Uma consulta síncrona é uma consulta que mantém o controle sobre o processo de seu aplicativo durante a consulta.</span><span class="sxs-lookup"><span data-stu-id="cba82-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="cba82-105">Uma consulta síncrona requer uma chamada de interface única e, portanto, é mais simples do que uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="cba82-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="cba82-106">No entanto, uma consulta síncrona tem o potencial de bloquear seu aplicativo para consultas ou consultas grandes em uma rede.</span><span class="sxs-lookup"><span data-stu-id="cba82-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="cba82-107">O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cba82-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="cba82-108">**Para emitir uma consulta de dados síncrona no PowerShell**</span><span class="sxs-lookup"><span data-stu-id="cba82-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="cba82-109">Descreva sua consulta ao WMI usando o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) do WMI e o parâmetro *-Query* .</span><span class="sxs-lookup"><span data-stu-id="cba82-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="cba82-110">O cmdlet retorna um único objeto ou uma coleção de objetos, dependendo de quantos objetos se ajustam à consulta.</span><span class="sxs-lookup"><span data-stu-id="cba82-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="cba82-111">O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C#.</span><span class="sxs-lookup"><span data-stu-id="cba82-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="cba82-112">**Para emitir uma consulta de dados síncrona em C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="cba82-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="cba82-113">Descreva sua consulta ao WMI usando CimSession. QueryInstances.</span><span class="sxs-lookup"><span data-stu-id="cba82-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="cba82-114">Esse método retorna uma coleção de objetos CimInstance.</span><span class="sxs-lookup"><span data-stu-id="cba82-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="cba82-115">Use as técnicas padrão da coleção de idiomas C# para acessar cada objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="cba82-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="cba82-116">O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C#.</span><span class="sxs-lookup"><span data-stu-id="cba82-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="cba82-117">**Para emitir uma consulta de dados síncrona em C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="cba82-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="cba82-118">Crie a consulta com um objeto [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) e recupere as informações com uma chamada para [ManagementObjectSearcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span><span class="sxs-lookup"><span data-stu-id="cba82-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="cba82-119">Esse método retorna um objeto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) .</span><span class="sxs-lookup"><span data-stu-id="cba82-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="cba82-120">Use as técnicas padrão da coleção de idiomas C# para acessar cada objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="cba82-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="cba82-121">O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="cba82-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="cba82-122">**Para emitir uma consulta de dados síncrona no VBScript**</span><span class="sxs-lookup"><span data-stu-id="cba82-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="cba82-123">Descreva sua consulta ao WMI usando [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="cba82-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="cba82-124">Esse método retorna um [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="cba82-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="cba82-125">Use técnicas de [coleção](accessing-a-collection.md) de idiomas de script padrão para acessar cada objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="cba82-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="cba82-126">O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C++.</span><span class="sxs-lookup"><span data-stu-id="cba82-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="cba82-127">**Para emitir uma consulta síncrona em C++**</span><span class="sxs-lookup"><span data-stu-id="cba82-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="cba82-128">Descreva sua consulta ao WMI por meio de uma chamada para [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="cba82-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="cba82-129">O método [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) usa uma cadeia de caracteres de pesquisa WQL como um parâmetro que descreve sua consulta.</span><span class="sxs-lookup"><span data-stu-id="cba82-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="cba82-130">O WMI executa a consulta e retorna um ponteiro de interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="cba82-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="cba82-131">Por meio da interface **IEnumWbemClassObject** , você pode acessar as classes ou instâncias que compõem o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cba82-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="cba82-132">Depois de receber sua consulta, você pode enumerar sua consulta com uma chamada para [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span><span class="sxs-lookup"><span data-stu-id="cba82-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="cba82-133">Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cba82-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="cba82-134">O exemplo de código a seguir requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="cba82-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="cba82-135">O exemplo de código a seguir descreve como consultar os objetos que representam os usuários e grupos no WMI.</span><span class="sxs-lookup"><span data-stu-id="cba82-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
