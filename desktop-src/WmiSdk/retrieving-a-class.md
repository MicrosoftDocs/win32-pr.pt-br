---
description: O primeiro tipo de objeto que você pode recuperar é uma classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recuperando uma classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105760933"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="86707-103">Recuperando uma classe WMI</span><span class="sxs-lookup"><span data-stu-id="86707-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="86707-104">O primeiro tipo de objeto que você pode recuperar é uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="86707-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="86707-105">Ao recuperar uma classe WMI, você realmente recupera uma definição de classe, que é uma lista das propriedades, qualificadores e métodos que descrevem totalmente a classe.</span><span class="sxs-lookup"><span data-stu-id="86707-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="86707-106">No entanto, uma definição de classe é basicamente a própria classe.</span><span class="sxs-lookup"><span data-stu-id="86707-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="86707-107">O PowerShell usa uma consulta padrão para recuperar definições de classe, usando a classe **meta \_ Class** .</span><span class="sxs-lookup"><span data-stu-id="86707-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="86707-108">**Para recuperar uma definição de classe no PowerShell**</span><span class="sxs-lookup"><span data-stu-id="86707-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="86707-109">Use o [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) com uma consulta para **meta \_ Class**, com a cláusula WHERE que contém o nome da classe que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="86707-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="86707-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) é o cmdlet padrão que o PowerShell usa para recuperar informações de classe e instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="86707-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="86707-111">A classe **meta \_ Class** define a consulta como uma consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="86707-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="86707-112">Sem a classe **meta \_ Class** , essa consulta retornaria todas as instâncias do disco lógico do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="86707-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="86707-113">Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="86707-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="86707-114">O processo atual para recuperar uma definição de WMI em C# é usar a classe **CIMInstance** .</span><span class="sxs-lookup"><span data-stu-id="86707-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="86707-115">**Para recuperar uma definição de classe em C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="86707-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="86707-116">Usando o namespace **Microsoft. Management. Infrastructure** , crie uma classe **CIMInstance** com o namespace e o nome de classe especificados.</span><span class="sxs-lookup"><span data-stu-id="86707-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="86707-117">A classe criada conterá todas as informações de classe, mas não os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="86707-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="86707-118">Como alternativa, assim como acontece com o PowerShell, você também pode executar uma consulta, usando a marca **meta \_ Class** como parte da consulta.</span><span class="sxs-lookup"><span data-stu-id="86707-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="86707-119">Assim como no PowerShell, o C# usa uma consulta de **\_ metaclasse** para recuperar definições de classe.</span><span class="sxs-lookup"><span data-stu-id="86707-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="86707-120">Como alternativa, você pode criar um objeto **ManagementClass** para acessar a definição de classe diretamente.</span><span class="sxs-lookup"><span data-stu-id="86707-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="86707-121">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="86707-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="86707-122">**Para recuperar uma definição de classe em C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="86707-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="86707-123">Você pode usar o [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) com uma consulta para **meta \_ Class**, com a cláusula WHERE que contém o nome da classe que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="86707-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="86707-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) é a classe padrão usada pelo .net para recuperar informações de classe e instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="86707-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="86707-125">[ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) retorna um [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contém a classe de definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="86707-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="86707-126">A classe **meta \_ Class** define a consulta como uma consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="86707-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="86707-127">Sem a classe **meta \_ Class** , essa consulta retornaria todas as instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="86707-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="86707-128">Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="86707-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="86707-129">Como alternativa, crie um novo objeto [ManagementClass](/dotnet/api/system.management.managementclass) , com o nome como o caminho, para recuperar a classe.</span><span class="sxs-lookup"><span data-stu-id="86707-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="86707-130">Você pode recuperar uma definição de classe no VBScript de forma semelhante à recuperação de uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="86707-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="86707-131">**Para recuperar uma definição de classe no VBScript**</span><span class="sxs-lookup"><span data-stu-id="86707-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="86707-132">Chame [**SWbemServices. Get**](swbemservices-get.md) , mas não identifique uma instância específica no caminho do objeto para a classe.</span><span class="sxs-lookup"><span data-stu-id="86707-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="86707-133">O exemplo de código a seguir recupera a definição de classe para a classe que descreve unidades lógicas em seu computador.</span><span class="sxs-lookup"><span data-stu-id="86707-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="86707-134">O WSH (Windows Script Host) também oferece suporte ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="86707-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="86707-135">No Active Server Pages (ASP), use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ou [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) no script do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="86707-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="86707-136">Para obter mais informações, consulte [criando páginas de Active Server para o WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="86707-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="86707-137">Uma classe ou instância também pode ser especificada; nesse caso, o objeto retornado é um objeto WMI, por exemplo, uma instância do [**disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), em vez de um objeto de serviços.</span><span class="sxs-lookup"><span data-stu-id="86707-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="86707-138">Observe que você não pode usar as funções do VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para criar uma instância do objeto genérico [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="86707-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="86707-139">Em páginas HTML em execução no Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) podem falhar porque os objetos de script WMI, como controles ActiveX, não são marcados como seguros para scripts.</span><span class="sxs-lookup"><span data-stu-id="86707-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="86707-140">A única exceção é o objeto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="86707-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="86707-141">A única maneira de que essas chamadas pode ter sucesso é quando você reduz as configurações de segurança do IE, o que não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="86707-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="86707-142">Ao recuperar uma classe em C++, chame a versão de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) do [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="86707-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="86707-143">**Para recuperar uma definição de classe em C++**</span><span class="sxs-lookup"><span data-stu-id="86707-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="86707-144">Chame os métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar a definição de uma classe.</span><span class="sxs-lookup"><span data-stu-id="86707-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="86707-145">Uma classe pode ter várias definições de classe, o que acontece normalmente quando você tem mais de um provedor de classe carregado em um namespace.</span><span class="sxs-lookup"><span data-stu-id="86707-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="86707-146">Quando uma classe tem várias definições de classe, o WMI retorna a primeira definição descoberta e o código de status de **\_ \_ \_ objetos duplicados do WBEM** .</span><span class="sxs-lookup"><span data-stu-id="86707-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="86707-147">Como [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retorna uma definição de classe, ele é comumente usado como a primeira etapa na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="86707-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="86707-148">Para obter mais informações sobre como usar **GetObject**, consulte [criando e declarando uma instância usando C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="86707-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
