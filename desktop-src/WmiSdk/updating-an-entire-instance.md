---
description: O meio mais comum de atualizar uma instância de classe WMI é atualizar toda a instância de uma vez.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Atualizando uma instância inteira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170603"
---
# <a name="updating-an-entire-instance"></a>Atualizando uma instância inteira

O meio mais comum de atualizar uma instância de classe WMI é atualizar toda a instância de uma vez. Ao atualizar uma instância inteira, o WMI não precisa analisar a instância em propriedades individuais e enviá-las ao seu aplicativo. Em vez disso, o WMI pode simplesmente enviar a você a instância inteira. Quando você terminar, o WMI poderá copiar toda a instância alterada na instância original.

O procedimento a seguir descreve como modificar ou atualizar uma instância usando o PowerShell.

**Para modificar ou atualizar uma instância usando o PowerShell**

1.  Recupere uma cópia local do objeto com uma chamada para Get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.

    Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Faça as alterações nas propriedades do objeto local.

    Isso altera apenas a cópia local. Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Coloque o objeto de volta no repositório WMI usando uma chamada para o método Put.

    ```PowerShell
    $mySettings.Put()
    ```

    

O procedimento a seguir descreve como modificar ou atualizar uma instância usando C#.

**Para modificar ou atualizar uma instância usando C# (Microsoft. Management. Infrastructure)**

1.  Recupere uma cópia local do objeto com uma chamada para [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), conforme descrito em [recuperando uma instância do WMI](retrieving-an-instance.md).

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.

    Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Faça as alterações nas propriedades do objeto local.

    Isso altera apenas a cópia local. Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Coloque o objeto de volta no repositório WMI usando uma chamada para [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

O procedimento a seguir descreve como modificar ou atualizar uma instância usando o PowerShell.

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

**Para modificar ou atualizar uma instância usando C# (Microsoft. Management)**

1.  Recupere uma cópia local do objeto com uma chamada para [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.

    Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Faça as alterações nas propriedades do objeto local.

    Isso altera apenas a cópia local. Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Coloque o objeto de volta no repositório WMI usando uma chamada para o método [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) ou.

    ```CSharp
    myDisk.Put();
    ```

    

O procedimento a seguir descreve como modificar ou atualizar uma instância usando o VBScript.

**Para modificar ou atualizar uma instância usando o VBScript**

1.  Recupere uma cópia local do objeto com uma chamada para **GetObject**.
2.  Se necessário, exiba as propriedades do objeto com uma chamada para o método [**Properties \_**](swbemobject-properties-.md) .

    Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.

3.  Faça as alterações nas propriedades do objeto com uma chamada para o método [**SWbemProperty. Value**](swbemproperty-value.md) .

    O método **Value** altera apenas a cópia local. Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.

4.  Coloque o objeto de volta no repositório WMI com uma chamada para os métodos [**SWbemObject \_ . put**](swbemobject-put-.md) ou [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md) .

Como os nomes sugerem, [**Coloque \_**](swbemobject-put-.md) atualizações de forma síncrona enquanto o [**PutAsync \_**](swbemobject-putasync-.md) atualiza de maneira assíncrona. O método copia sobre a instância original com sua instância modificada. No entanto, para aproveitar o processamento assíncrono, você deve criar um objeto [**SWbemSink**](swbemsink.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

O procedimento a seguir descreve como modificar ou atualizar uma instância usando C++.

**Para modificar ou atualizar uma instância usando C++**

1.  Recupere uma cópia local da instância com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Se necessário, exiba as propriedades do objeto com uma chamada para [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.

3.  Faça as alterações necessárias na cópia com uma chamada para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    O método **Put** altera apenas a cópia local. Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.

4.  Coloque sua cópia de volta no repositório WMI com uma chamada de [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) métodos de utinstanceasync.

    Como os nomes sugerem, a **PutInstance** é atualizada de forma síncrona enquanto [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) atualiza de maneira assíncrona. O método copia sobre a instância original com sua instância modificada. No entanto, para aproveitar o processamento assíncrono, você deve implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    Você deve estar ciente de que uma operação de atualização em uma instância que pertence a uma hierarquia de classe pode não ter sucesso devido a um erro envolvendo outra classe na hierarquia. O WMI chama o método [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de cada um dos provedores responsáveis pelas classes das quais a classe proprietária da instância original deriva. Se qualquer um desses provedores falhar, a solicitação de atualização original falhará. Para obter mais informações, consulte a seção comentários de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Para obter mais informações, consulte [chamando um método de provedor](calling-a-provider-method.md).

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

 

 
