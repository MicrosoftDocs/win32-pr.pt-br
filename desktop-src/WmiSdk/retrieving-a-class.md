---
description: O primeiro tipo de objeto que você pode recuperar é uma classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recuperando uma classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739875"
---
# <a name="retrieving-a-wmi-class"></a>Recuperando uma classe WMI

O primeiro tipo de objeto que você pode recuperar é uma classe WMI. Ao recuperar uma classe WMI, você realmente recupera uma definição de classe, que é uma lista das propriedades, qualificadores e métodos que descrevem totalmente a classe. No entanto, uma definição de classe é basicamente a própria classe.

O PowerShell usa uma consulta padrão para recuperar definições de classe, usando a **classe meta. \_**

**Para recuperar uma definição de classe no PowerShell**

-   Use [o Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) com uma consulta para a meta class , com a cláusula WHERE que contém o nome da classe com a qual você deve recuperar. **\_**

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject é](https://technet.microsoft.com/library/dd315379.aspx) o cmdlet padrão que o PowerShell usa para recuperar informações de classe e instância do WMI. A **classe \_ meta** class define a consulta como uma consulta de esquema. Sem a **classe meta, \_** essa consulta retornaria todas as instâncias de \_ LogicalDisk do Win32. Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).

O processo atual para recuperar uma definição de WMI em C# é usar a **classe CIMInstance.**

**Para recuperar uma definição de classe em C# (Microsoft.Management.Infrastructure)**

1.  Usando o namespace **Microsoft.Management.Infrastructure,** crie uma **classe CIMInstance** com o namespace e o nome de classe especificados.

    A classe criada conterá todas as informações de classe, mas nenhum dado de instância.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Como alternativa, assim como no PowerShell, você também pode executar uma consulta, usando a **marca de meta \_ class** como parte da consulta.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Assim como no PowerShell, o C# usa uma **consulta de meta \_** class para recuperar definições de classe. Como alternativa, você pode criar um objeto **ManagementClass** para acessar a definição de classe diretamente.

> [!Note]  
> **System.Management era** o namespace original do .NET usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são tão dimensionamento em relação às contrapartes mais modernas **do Microsoft.Management.Infrastructure.**

 

**Para recuperar uma definição de classe em C# (System.Management)**

1.  Você pode usar [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) com uma consulta para a meta class , com a cláusula WHERE que contém o nome da classe com a qual recuperar. **\_**

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) é a classe padrão que o .NET usa para recuperar informações de classe e instância do WMI. [ManagementObjectSerarcher.Get retorna](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) [um ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contém a classe de definição de esquema. A **classe \_ meta** class define a consulta como uma consulta de esquema. Sem a **classe meta, \_** essa consulta retornaria todas as instâncias de [**\_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).

2.  Como alternativa, crie um novo [objeto ManagementClass,](/dotnet/api/system.management.managementclass) com o nome como o caminho, para recuperar a classe.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Você pode recuperar uma definição de classe no VBScript de uma maneira semelhante para recuperar uma instância específica.

**Para recuperar uma definição de classe no VBScript**

1.  Chame [**SWbemServices.Get,**](swbemservices-get.md) mas não identifique uma instância específica no caminho do objeto para a classe .
2.  O exemplo de código a seguir recupera a definição de classe para a classe que descreve unidades lógicas em seu computador.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows O Host de Script (WSH) também dá suporte ao seguinte.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    No Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ou [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) no script do lado do servidor. Para obter mais informações, consulte [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).

3.  Uma classe ou instância também pode ser especificada, caso em que o objeto retornado é um objeto WMI, por exemplo, uma instância de [**\_ LogicalDisk do Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)em vez de um objeto de serviços. Observe que você não pode usar as funções [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) do VBScript para criar uma instância do objeto [**genérico SWbemObject**](swbemobject.md).
4.  Em páginas HTML em execução no Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) podem falhar porque objetos de script WMI, como controles ActiveX, não são marcados como seguros para script. A única exceção é o [**objeto SWbemDateTime.**](swbemdatetime.md) A única maneira de essas chamadas pode ser bem-sucedida é quando você reduz as configurações de segurança do IE, o que não é recomendado.

Ao recuperar uma classe em C++, chame a [**versão IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar uma definição de classe em C++**

1.  Chame os [**métodos IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar a definição de uma classe.
2.  Uma classe pode ter várias definições de classe, o que normalmente acontece quando você tem mais de um provedor de classe carregado em um namespace. Quando uma classe tem várias definições de classe, o WMI retorna a primeira definição descoberta e o código de status **\_ WBEM S DUPLICATE \_ \_ OBJECTS.**

Como [**GetObject retorna**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) uma definição de classe, ele geralmente é usado como a primeira etapa na criação de uma instância. Para obter mais informações sobre como usar **GetObject**, consulte Criando e declarando uma [instância usando C++.](creating-and-declaring-an-instance-using-c-.md)

 

 
