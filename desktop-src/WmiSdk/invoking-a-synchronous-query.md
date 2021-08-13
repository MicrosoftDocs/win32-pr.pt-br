---
description: Uma consulta síncrona é uma consulta que mantém o controle sobre o processo do aplicativo durante a consulta.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Invocando uma consulta síncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f089ac5a2d315aa55fe7af7e648d3b001bae032b92ed5b7d67a1b6b120b96561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556114"
---
# <a name="invoking-a-synchronous-query"></a>Invocando uma consulta síncrona

Uma consulta síncrona é uma consulta que mantém o controle sobre o processo do aplicativo durante a consulta. Uma consulta síncrona requer uma única chamada de interface e, portanto, é mais simples do que uma chamada assíncrona. No entanto, uma consulta síncrona tem o potencial de bloquear seu aplicativo para consultas grandes ou consultas em uma rede.

O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando o PowerShell.

**Para emitir uma consulta de dados síncrona no PowerShell**

-   Descreva sua consulta ao WMI usando o cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) do WMI e o *parâmetro -query.* O cmdlet retorna um único objeto ou uma coleção de objetos, dependendo de quantos objetos se ajustam à consulta.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C#.

**Para emitir uma consulta de dados síncrona em C# (Microsoft.Management.Infrastructure)**

1.  Descreva sua consulta ao WMI usando CimSession.QueryInstances. Esse método retorna uma coleção de objetos CimInstance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Use técnicas de coleção de linguagem C# padrão para acessar cada objeto retornado.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C#.

**Para emitir uma consulta de dados síncrona em C# (System.Management)**

1.  Crie a consulta com um [objeto ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) e recupere as informações com uma chamada para [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).

    Esse método retorna um [objeto ManagementObjectCollection.](/dotnet/api/system.management.managementobjectcollection)

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Use técnicas de coleção de linguagem C# padrão para acessar cada objeto retornado.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando o VBScript.

**Para emitir uma consulta de dados síncrona no VBScript**

1.  Descreva sua consulta ao WMI usando [**SWbemServices.ExecQuery**](swbemservices-execquery.md). Esse método retorna um [**SWbemObjectSet**](swbemobjectset.md).

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Use técnicas de coleção [de](accessing-a-collection.md) linguagem de script padrão para acessar cada objeto retornado.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

O procedimento a seguir descreve como emitir uma consulta de dados síncrona usando C++.

**Para emitir uma consulta síncrona em C++**

1.  Descreva sua consulta ao WMI por meio de uma chamada para [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    O [**método ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) assume uma cadeia de caracteres de pesquisa WQL como um parâmetro que descreve sua consulta. O WMI executa a consulta e retorna um ponteiro de interface [**IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Por meio da interface **IEnumWbemClassObject,** você pode acessar as classes ou instâncias que compoem o conjunto de resultados.

2.  Depois de receber a consulta, você pode enumerar sua consulta com uma chamada para [**IEnumWbemClassObject::Next.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) Para obter mais informações, consulte [Enumerando WMI](enumerating-wmi.md).

    O exemplo de código a seguir requer as seguintes referências e \# instruções include para compilar corretamente.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    O exemplo de código a seguir descreve como consultar os objetos que representam os usuários e grupos no WMI.

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

    

 

 
