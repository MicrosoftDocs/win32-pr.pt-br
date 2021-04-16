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
# <a name="retrieving-a-wmi-class"></a>Recuperando uma classe WMI

O primeiro tipo de objeto que você pode recuperar é uma classe WMI. Ao recuperar uma classe WMI, você realmente recupera uma definição de classe, que é uma lista das propriedades, qualificadores e métodos que descrevem totalmente a classe. No entanto, uma definição de classe é basicamente a própria classe.

O PowerShell usa uma consulta padrão para recuperar definições de classe, usando a classe **meta \_ Class** .

**Para recuperar uma definição de classe no PowerShell**

-   Use o [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) com uma consulta para **meta \_ Class**, com a cláusula WHERE que contém o nome da classe que você deseja recuperar.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) é o cmdlet padrão que o PowerShell usa para recuperar informações de classe e instância do WMI. A classe **meta \_ Class** define a consulta como uma consulta de esquema. Sem a classe **meta \_ Class** , essa consulta retornaria todas as instâncias do disco lógico do Win32 \_ . Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).

O processo atual para recuperar uma definição de WMI em C# é usar a classe **CIMInstance** .

**Para recuperar uma definição de classe em C# (Microsoft. Management. Infrastructure)**

1.  Usando o namespace **Microsoft. Management. Infrastructure** , crie uma classe **CIMInstance** com o namespace e o nome de classe especificados.

    A classe criada conterá todas as informações de classe, mas não os dados da instância.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Como alternativa, assim como acontece com o PowerShell, você também pode executar uma consulta, usando a marca **meta \_ Class** como parte da consulta.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Assim como no PowerShell, o C# usa uma consulta de **\_ metaclasse** para recuperar definições de classe. Como alternativa, você pode criar um objeto **ManagementClass** para acessar a definição de classe diretamente.

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

**Para recuperar uma definição de classe em C# (System. Management)**

1.  Você pode usar o [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) com uma consulta para **meta \_ Class**, com a cláusula WHERE que contém o nome da classe que você deseja recuperar.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) é a classe padrão usada pelo .net para recuperar informações de classe e instância do WMI. [ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) retorna um [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contém a classe de definição de esquema. A classe **meta \_ Class** define a consulta como uma consulta de esquema. Sem a classe **meta \_ Class** , essa consulta retornaria todas as instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Para obter mais informações sobre como consultar o WMI, consulte [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).

2.  Como alternativa, crie um novo objeto [ManagementClass](/dotnet/api/system.management.managementclass) , com o nome como o caminho, para recuperar a classe.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Você pode recuperar uma definição de classe no VBScript de forma semelhante à recuperação de uma instância específica.

**Para recuperar uma definição de classe no VBScript**

1.  Chame [**SWbemServices. Get**](swbemservices-get.md) , mas não identifique uma instância específica no caminho do objeto para a classe.
2.  O exemplo de código a seguir recupera a definição de classe para a classe que descreve unidades lógicas em seu computador.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    O WSH (Windows Script Host) também oferece suporte ao seguinte.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    No Active Server Pages (ASP), use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ou [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) no script do lado do servidor. Para obter mais informações, consulte [criando páginas de Active Server para o WMI](creating-active-server-pages-for-wmi.md).

3.  Uma classe ou instância também pode ser especificada; nesse caso, o objeto retornado é um objeto WMI, por exemplo, uma instância do [**disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), em vez de um objeto de serviços. Observe que você não pode usar as funções do VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para criar uma instância do objeto genérico [**SWbemObject**](swbemobject.md).
4.  Em páginas HTML em execução no Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) podem falhar porque os objetos de script WMI, como controles ActiveX, não são marcados como seguros para scripts. A única exceção é o objeto [**SWbemDateTime**](swbemdatetime.md) . A única maneira de que essas chamadas pode ter sucesso é quando você reduz as configurações de segurança do IE, o que não é recomendado.

Ao recuperar uma classe em C++, chame a versão de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) do [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar uma definição de classe em C++**

1.  Chame os métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar a definição de uma classe.
2.  Uma classe pode ter várias definições de classe, o que acontece normalmente quando você tem mais de um provedor de classe carregado em um namespace. Quando uma classe tem várias definições de classe, o WMI retorna a primeira definição descoberta e o código de status de **\_ \_ \_ objetos duplicados do WBEM** .

Como [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retorna uma definição de classe, ele é comumente usado como a primeira etapa na criação de uma instância. Para obter mais informações sobre como usar **GetObject**, consulte [criando e declarando uma instância usando C++](creating-and-declaring-an-instance-using-c-.md).

 

 
