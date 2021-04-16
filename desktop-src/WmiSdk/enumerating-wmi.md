---
description: A enumeração é o ato de passar por um conjunto de objetos e possivelmente modificar cada objeto assim que você fizer isso.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Enumerando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765130"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="4e02e-103">Enumerando o WMI</span><span class="sxs-lookup"><span data-stu-id="4e02e-103">Enumerating WMI</span></span>

<span data-ttu-id="4e02e-104">A enumeração é o ato de passar por um conjunto de objetos e possivelmente modificar cada objeto assim que você fizer isso.</span><span class="sxs-lookup"><span data-stu-id="4e02e-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="4e02e-105">Por exemplo, você pode enumerar por meio de um conjunto de objetos [**\_ DiskDrive do Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) para localizar um número de série específico.</span><span class="sxs-lookup"><span data-stu-id="4e02e-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="4e02e-106">Observe que, embora você possa enumerar qualquer objeto, o WMI retorna apenas objetos aos quais você tem acesso de segurança.</span><span class="sxs-lookup"><span data-stu-id="4e02e-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="4e02e-107">Enumerações de grandes conjuntos de dados podem exigir uma grande quantidade de recursos e degradar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="4e02e-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="4e02e-108">Para obter mais informações, consulte [melhorando o desempenho de enumeração](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="4e02e-109">Você também pode solicitar dados com uma consulta mais específica.</span><span class="sxs-lookup"><span data-stu-id="4e02e-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="4e02e-110">Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="4e02e-111">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="4e02e-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="4e02e-112">Enumerando o WMI usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e02e-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="4e02e-113">Enumerando o WMI usando C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="4e02e-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="4e02e-114">Enumerando o WMI usando C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="4e02e-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="4e02e-115">Enumerando o WMI usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="4e02e-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="4e02e-116">Enumerando o WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="4e02e-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="4e02e-117">Enumerando o WMI usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e02e-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="4e02e-118">Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), com o nome da classe no parâmetro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="4e02e-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="4e02e-119">Se você quiser usar uma consulta, poderá usar o parâmetro *-Query* .</span><span class="sxs-lookup"><span data-stu-id="4e02e-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="4e02e-120">O procedimento a seguir descreve como enumerar as instâncias de uma classe usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e02e-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="4e02e-121">**Para enumerar as instâncias de uma classe usando o PowerShell**</span><span class="sxs-lookup"><span data-stu-id="4e02e-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="4e02e-122">Enumere as instâncias com uma chamada para o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4e02e-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="4e02e-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) retorna uma coleção de um ou mais objetos WMI, por meio dos quais você pode enumerar.</span><span class="sxs-lookup"><span data-stu-id="4e02e-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="4e02e-124">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="4e02e-125">Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace nos parâmetros *-Computer* e *-namespace* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4e02e-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="4e02e-126">Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="4e02e-127">Isso só funcionará se você tiver os privilégios de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="4e02e-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="4e02e-128">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="4e02e-129">Recupere quaisquer instâncias individuais que desejar usando os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="4e02e-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="4e02e-130">O exemplo de código a seguir recupera uma coleção do PowerShell e, em seguida, exibe a propriedade Size para todas as instâncias de unidades lógicas no computador local.</span><span class="sxs-lookup"><span data-stu-id="4e02e-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="4e02e-131">Enumerando o WMI usando C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="4e02e-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="4e02e-132">Adicione uma referência ao assembly de referência **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="4e02e-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="4e02e-133">(Esse assembly é fornecido como parte do [SDK (Software Development Kit) do Windows para Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e02e-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="4e02e-134">Adicione uma instrução **using** para o namespace **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="4e02e-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="4e02e-135">Crie uma instância de um objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e02e-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="4e02e-136">O trecho a seguir usa o valor "localhost" padrão para o método [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e02e-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="4e02e-137">Chame o método [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) passando o namespace CIM desejado e o WQL para usar.</span><span class="sxs-lookup"><span data-stu-id="4e02e-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="4e02e-138">O trecho a seguir retornará duas instâncias que representam dois processos padrão do Windows, em que a propriedade Handle (representando uma ID de processo ou PID) tem um valor de 0 ou 4.</span><span class="sxs-lookup"><span data-stu-id="4e02e-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="4e02e-139">Faça um loop pelos objetos [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) retornados.</span><span class="sxs-lookup"><span data-stu-id="4e02e-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="4e02e-140">O exemplo de código a seguir enumera todas as instâncias da classe de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) (que representa processos ativos) no computador local e imprime o nome de cada processo.</span><span class="sxs-lookup"><span data-stu-id="4e02e-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="4e02e-141">Em um aplicativo real, você definiria como parâmetros o nome do computador ("localhost") e o namespace CIM ("raiz \\ cimv2").</span><span class="sxs-lookup"><span data-stu-id="4e02e-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="4e02e-142">Para fins de simplicidade, eles foram codificados neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="4e02e-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="4e02e-143">Enumerando o WMI usando C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="4e02e-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="4e02e-144">Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use o objeto [ManagementClass](/dotnet/api/system.management.managementclass) para recuperar um [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contém todas as instâncias de uma determinada classe no namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="4e02e-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="4e02e-145">Como alternativa, você pode consultar o WMI por meio de um [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) para obter o mesmo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="4e02e-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="4e02e-146">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="4e02e-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="4e02e-147">O procedimento a seguir descreve como enumerar as instâncias de uma classe usando C#.</span><span class="sxs-lookup"><span data-stu-id="4e02e-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="4e02e-148">**Para enumerar as instâncias de uma classe usando C #**</span><span class="sxs-lookup"><span data-stu-id="4e02e-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="4e02e-149">Enumere as instâncias com uma chamada para [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span><span class="sxs-lookup"><span data-stu-id="4e02e-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="4e02e-150">O método [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) retorna uma coleção ou um conjunto de objetos por meio do qual você pode enumerar.</span><span class="sxs-lookup"><span data-stu-id="4e02e-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="4e02e-151">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="4e02e-152">A coleção retornada é, na verdade, um objeto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , portanto, qualquer um dos métodos desse objeto pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="4e02e-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="4e02e-153">Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace no parâmetro *path* .</span><span class="sxs-lookup"><span data-stu-id="4e02e-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="4e02e-154">Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="4e02e-155">Isso só funcionará se você tiver os privilégios de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="4e02e-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="4e02e-156">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="4e02e-157">Recupere quaisquer instâncias individuais que desejar usando os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="4e02e-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="4e02e-158">O exemplo de código a seguir recupera uma coleção C# e, em seguida, exibe a propriedade Size para todas as instâncias de unidades lógicas no computador local.</span><span class="sxs-lookup"><span data-stu-id="4e02e-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="4e02e-159">Enumerando o WMI usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="4e02e-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="4e02e-160">Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use o método [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) para retornar uma enumeração [**SWbemObjectSet**](swbemobjectset.md) de todas as instâncias de uma classe.</span><span class="sxs-lookup"><span data-stu-id="4e02e-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="4e02e-161">Como alternativa, você pode consultar o WMI por meio de [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para obter o mesmo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="4e02e-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="4e02e-162">O procedimento a seguir descreve como enumerar as instâncias de uma classe usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="4e02e-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="4e02e-163">**Para enumerar as instâncias de uma classe usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="4e02e-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="4e02e-164">Enumere as instâncias com uma chamada para o método [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .</span><span class="sxs-lookup"><span data-stu-id="4e02e-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="4e02e-165">O método [**InstancesOf**](swbemservices-instancesof.md) retorna uma coleção ou um conjunto de objetos por meio do qual você pode enumerar.</span><span class="sxs-lookup"><span data-stu-id="4e02e-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="4e02e-166">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="4e02e-167">A coleção retornada é, na verdade, um objeto [**SWbemObjectSet**](swbemobjectset.md) , portanto, qualquer um dos métodos desse objeto pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="4e02e-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="4e02e-168">Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace no moniker.</span><span class="sxs-lookup"><span data-stu-id="4e02e-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="4e02e-169">Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="4e02e-170">Isso só funcionará se você tiver os privilégios de acesso apropriados.</span><span class="sxs-lookup"><span data-stu-id="4e02e-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="4e02e-171">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="4e02e-172">Recupere quaisquer instâncias individuais que desejar usando os métodos de coleções.</span><span class="sxs-lookup"><span data-stu-id="4e02e-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="4e02e-173">O exemplo de código a seguir recupera um objeto [**SWbemServices**](swbemservices.md) e, em seguida, executa o método [**InstancesOf**](swbemservices-instancesof.md) para exibir a propriedade Size para todas as instâncias de unidades lógicas no computador local.</span><span class="sxs-lookup"><span data-stu-id="4e02e-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="4e02e-174">Enumerando o WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="4e02e-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="4e02e-175">Além de executar a enumeração básica, você pode definir vários sinalizadores e propriedades para aumentar o desempenho da sua enumeração.</span><span class="sxs-lookup"><span data-stu-id="4e02e-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="4e02e-176">Para obter mais informações, consulte [melhorando o desempenho de enumeração](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="4e02e-177">**Para enumerar um conjunto de objetos no WMI**</span><span class="sxs-lookup"><span data-stu-id="4e02e-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="4e02e-178">Crie uma interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) descrevendo o conjunto de objetos que você deseja enumerar.</span><span class="sxs-lookup"><span data-stu-id="4e02e-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="4e02e-179">Um objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contém uma lista que descreve um conjunto de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="4e02e-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="4e02e-180">Você pode usar os métodos **IEnumWbemClassObject** para enumerar encaminhamentos, ignorar objetos, começar no início e copiar o enumerador.</span><span class="sxs-lookup"><span data-stu-id="4e02e-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="4e02e-181">A tabela a seguir lista os métodos usados para criar enumeradores para diferentes tipos de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="4e02e-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="4e02e-182">Objeto</span><span class="sxs-lookup"><span data-stu-id="4e02e-182">Object</span></span></th>
    <th><span data-ttu-id="4e02e-183">Método</span><span class="sxs-lookup"><span data-stu-id="4e02e-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="4e02e-184">Classe</span><span class="sxs-lookup"><span data-stu-id="4e02e-184">Class</span></span></td>
    <td><dl><span data-ttu-id="4e02e-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: CreateClassEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e02e-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="4e02e-186">[<strong>IWbemServices:: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span><span class="sxs-lookup"><span data-stu-id="4e02e-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4e02e-187">Instância</span><span class="sxs-lookup"><span data-stu-id="4e02e-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="4e02e-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e02e-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="4e02e-189">[<strong>IWbemServices:: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span><span class="sxs-lookup"><span data-stu-id="4e02e-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="4e02e-190">Resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="4e02e-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="4e02e-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e02e-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="4e02e-192">[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span><span class="sxs-lookup"><span data-stu-id="4e02e-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4e02e-193">Notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="4e02e-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="4e02e-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e02e-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="4e02e-195">[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span><span class="sxs-lookup"><span data-stu-id="4e02e-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="4e02e-196">Percorra a enumeração retornada usando várias chamadas para [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="4e02e-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="4e02e-197">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="4e02e-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
