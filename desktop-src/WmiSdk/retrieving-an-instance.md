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
# <a name="retrieving-a-wmi-instance"></a>Recuperando uma instância do WMI

Recuperar uma instância é um dos procedimentos de recuperação mais comuns que você provavelmente executará no WMI. Você pode recuperar uma instância existente ou criar uma nova instância sem nome. O caminho do WMI para a instância existente é um parâmetro necessário. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> Ao fornecer uma instância, um provedor pode não ser capaz de fornecer um valor para determinadas propriedades. A menos que indicado de outra forma na descrição da propriedade, você não pode inferir nenhum significado de um valor vazio. Isso não deve ser confundido com uma cadeia de caracteres que tem um valor **nulo** . Nesse caso, o valor é populado. Ele está vazio, mas tem um valor: **NULL**.

 

Recupere uma cópia local da instância com uma chamada para o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) do PowerShell.

**Para recuperar uma instância de uma classe WMI usando o PowerShell**

-   Você pode recuperar instâncias específicas usando os parâmetros *-Class* e *-Filter* .

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Você pode recuperar uma instância do WMI usando C# criando um objeto de pesquisa usando [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))e, em seguida, preenchendo-o com os valores de chave relevantes e, em seguida, procurando esse objeto com uma chamada [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

**Para recuperar uma instância de uma classe WMI usando C# (Microsoft. Management. Infrastructure)**

1.  Usando o namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , crie um novo objeto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) com o nome e o namespace da classe relevante.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Crie um [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) que contenha o nome e o valor da propriedade de chave da instância que você deseja pesquisar e adicione essa propriedade ao seu objeto de classe.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Recupere o objeto do WMI com uma chamada [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

Você pode recuperar uma instância de classe WMI específica ou uma coleção de instâncias de classe WMI, usando classes no namespace [System. Management](/dotnet/api/system.management) .

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

**Para recuperar uma instância de uma classe WMI usando C# (System. Management)**

1.  Recupere uma cópia local de uma instância específica criando um novo [ManagementObject](/dotnet/api/system.management.managementobject), com o nome e o valor de instância específico transmitidos, embora o parâmetro *ManagementPath* . Em seguida, você pode recuperar os dados da instância chamando explicitamente [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  Como alternativa, você pode recuperar todas as instâncias de uma classe WMI pesquisando-as com um [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)e enumerando por meio do [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)retornado.

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

    

    Você pode chamar implicitamente o método **Get** acessando a instância. Para obter mais informações, consulte [recuperando parte de uma instância do WMI](retrieving-part-of-an-instance.md).

Recupere uma cópia local da instância com uma chamada para o método VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .

**Para recuperar uma instância de uma classe WMI usando o VBScript**

-   Chame [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) com o caminho do objeto da instância, conforme mostrado no exemplo a seguir.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    A recuperação de uma instância específica requer o fornecimento de um nome como parte do caminho do objeto.

Em C++, chame [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar uma instância de uma classe WMI usando C++**

-   Recupere uma cópia local da instância com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). O caminho do WMI para o objeto deve ser incluído.

    Como o nome indica, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera a instância de forma assíncrona, enquanto [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera a instância de maneira síncrona. Se você quiser usar a recuperação assíncrona, deverá implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) .

## <a name="examples"></a>Exemplos

Para obter um exemplo de VBScript a ser usado como modelo para recuperar informações de classe e instância, consulte o exemplo de [script de modelo WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) na galeria do TechNet. Esse exemplo específico usa GetObject para recuperar o serviço WMI.

 

 
