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
# <a name="enumerating-wmi"></a>Enumerando o WMI

A enumeração é o ato de passar por um conjunto de objetos e possivelmente modificar cada objeto assim que você fizer isso. Por exemplo, você pode enumerar por meio de um conjunto de objetos [**\_ DiskDrive do Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) para localizar um número de série específico. Observe que, embora você possa enumerar qualquer objeto, o WMI retorna apenas objetos aos quais você tem acesso de segurança.

Enumerações de grandes conjuntos de dados podem exigir uma grande quantidade de recursos e degradar o desempenho. Para obter mais informações, consulte [melhorando o desempenho de enumeração](improving-enumeration-performance.md). Você também pode solicitar dados com uma consulta mais específica. Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).

As seções a seguir são discutidas neste tópico:

-   [Enumerando o WMI usando o PowerShell](#enumerating-wmi-using-powershell)
-   [Enumerando o WMI usando C# (Microsoft. Management. Infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Enumerando o WMI usando C# (System. Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Enumerando o WMI usando o VBScript](#enumerating-wmi-using-vbscript)
-   [Enumerando o WMI usando C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Enumerando o WMI usando o PowerShell

Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), com o nome da classe no parâmetro *-Class* . Se você quiser usar uma consulta, poderá usar o parâmetro *-Query* .

O procedimento a seguir descreve como enumerar as instâncias de uma classe usando o PowerShell.

**Para enumerar as instâncias de uma classe usando o PowerShell**

1.  Enumere as instâncias com uma chamada para o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) retorna uma coleção de um ou mais objetos WMI, por meio dos quais você pode enumerar. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

    Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace nos parâmetros *-Computer* e *-namespace* , respectivamente. Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md). Isso só funcionará se você tiver os privilégios de acesso apropriados. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).

2.  Recupere quaisquer instâncias individuais que desejar usando os membros da coleção.

O exemplo de código a seguir recupera uma coleção do PowerShell e, em seguida, exibe a propriedade Size para todas as instâncias de unidades lógicas no computador local.


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



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Enumerando o WMI usando C# (Microsoft. Management. Infrastructure)

1.  Adicione uma referência ao assembly de referência **Microsoft. Management. Infrastructure** . (Esse assembly é fornecido como parte do [SDK (Software Development Kit) do Windows para Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).
2.  Adicione uma instrução **using** para o namespace **Microsoft. Management. Infrastructure** .

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Crie uma instância de um objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) . O trecho a seguir usa o valor "localhost" padrão para o método [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Chame o método [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) passando o namespace CIM desejado e o WQL para usar. O trecho a seguir retornará duas instâncias que representam dois processos padrão do Windows, em que a propriedade Handle (representando uma ID de processo ou PID) tem um valor de 0 ou 4.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Faça um loop pelos objetos [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) retornados.

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

O exemplo de código a seguir enumera todas as instâncias da classe de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) (que representa processos ativos) no computador local e imprime o nome de cada processo.

> [!Note]  
> Em um aplicativo real, você definiria como parâmetros o nome do computador ("localhost") e o namespace CIM ("raiz \\ cimv2"). Para fins de simplicidade, eles foram codificados neste exemplo.

 


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





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Enumerando o WMI usando C# (System. Management)

Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use o objeto [ManagementClass](/dotnet/api/system.management.managementclass) para recuperar um [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contém todas as instâncias de uma determinada classe no namespace WMI. Como alternativa, você pode consultar o WMI por meio de um [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) para obter o mesmo conjunto de objetos.

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

O procedimento a seguir descreve como enumerar as instâncias de uma classe usando C#.

**Para enumerar as instâncias de uma classe usando C #**

1.  Enumere as instâncias com uma chamada para [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).

    O método [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) retorna uma coleção ou um conjunto de objetos por meio do qual você pode enumerar. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md). A coleção retornada é, na verdade, um objeto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , portanto, qualquer um dos métodos desse objeto pode ser chamado.

    Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace no parâmetro *path* . Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md). Isso só funcionará se você tiver os privilégios de acesso apropriados. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).

2.  Recupere quaisquer instâncias individuais que desejar usando os membros da coleção.

O exemplo de código a seguir recupera uma coleção C# e, em seguida, exibe a propriedade Size para todas as instâncias de unidades lógicas no computador local.


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



## <a name="enumerating-wmi-using-vbscript"></a>Enumerando o WMI usando o VBScript

Se você não souber o caminho do objeto para uma instância específica ou se quiser recuperar todas as instâncias de uma classe específica, use o método [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) para retornar uma enumeração [**SWbemObjectSet**](swbemobjectset.md) de todas as instâncias de uma classe. Como alternativa, você pode consultar o WMI por meio de [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para obter o mesmo conjunto de objetos.

O procedimento a seguir descreve como enumerar as instâncias de uma classe usando o VBScript.

**Para enumerar as instâncias de uma classe usando o VBScript**

1.  Enumere as instâncias com uma chamada para o método [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .

    O método [**InstancesOf**](swbemservices-instancesof.md) retorna uma coleção ou um conjunto de objetos por meio do qual você pode enumerar. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md). A coleção retornada é, na verdade, um objeto [**SWbemObjectSet**](swbemobjectset.md) , portanto, qualquer um dos métodos desse objeto pode ser chamado.

    Se você quiser recuperar uma instância de classe WMI em outro namespace ou em um computador diferente, especifique o computador e o namespace no moniker. Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md). Isso só funcionará se você tiver os privilégios de acesso apropriados. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md) e [executando operações privilegiadas](executing-privileged-operations.md).

2.  Recupere quaisquer instâncias individuais que desejar usando os métodos de coleções.

O exemplo de código a seguir recupera um objeto [**SWbemServices**](swbemservices.md) e, em seguida, executa o método [**InstancesOf**](swbemservices-instancesof.md) para exibir a propriedade Size para todas as instâncias de unidades lógicas no computador local.


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



## <a name="enumerating-wmi-using-c"></a>Enumerando o WMI usando C++

Além de executar a enumeração básica, você pode definir vários sinalizadores e propriedades para aumentar o desempenho da sua enumeração. Para obter mais informações, consulte [melhorando o desempenho de enumeração](improving-enumeration-performance.md).

**Para enumerar um conjunto de objetos no WMI**

1.  Crie uma interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) descrevendo o conjunto de objetos que você deseja enumerar.

    Um objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contém uma lista que descreve um conjunto de objetos WMI. Você pode usar os métodos **IEnumWbemClassObject** para enumerar encaminhamentos, ignorar objetos, começar no início e copiar o enumerador. A tabela a seguir lista os métodos usados para criar enumeradores para diferentes tipos de objetos WMI.

    

    <table>
    <thead>
    <tr class="header">
    <th>Objeto</th>
    <th>Método</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Classe</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: CreateClassEnum</strong></a><br />
[<strong>IWbemServices:: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Instância</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices:: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Resultado da consulta</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a><br />
[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Notificação de eventos</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Percorra a enumeração retornada usando várias chamadas para [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

 

 
