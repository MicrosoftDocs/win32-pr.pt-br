---
description: Um qualificador é uma marca que fornece mais informações sobre um objeto, método ou propriedade WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Acessando um qualificador WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45601de8e7b3f8ef7054742812c24f9a81dcedf5417f7b7ba501f2471adedc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820614"
---
# <a name="accessing-a-wmi-qualifier"></a>Acessando um qualificador WMI

Um qualificador é uma marca que fornece mais informações sobre um objeto, método ou propriedade WMI. Às vezes, talvez seja necessário acessar os dados armazenados em um qualificador. Por exemplo, uma tarefa comum é determinar se um provedor implementa um método tentando recuperar o qualificador **Implementado** para esse método. Para obter mais informações, consulte [Qualificadores WMI](wmi-qualifiers.md) e [Adicionando um qualificador](adding-a-qualifier.md).

Você pode recuperar os qualificadores em um objeto WMI no PowerShell recuperando primeiro o objeto e, em seguida, examinando os qualificadores como faria com qualquer outra propriedade.

**Para recuperar um qualificador usando o PowerShell**

-   Recupere o objeto cujos qualificadores você deseja exibir usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)e acesse os qualificadores por meio da propriedade **Qualificadores:**

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

Você pode recuperar os qualificadores em uma instância WMI em C# recuperando primeiro o objeto e, em seguida, examinando os qualificadores como uma coleção.

**Para recuperar um qualificador usando C# (Microsoft.System. Gerenciamento)**

1.  Recupere a classe cujos qualificadores você deseja exibir criando um objeto CimInstance, usando o nome de classe e o namespace especificados.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

2.  Você pode recuperar os qualificadores de classe de [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), os qualificadores de propriedade de [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))e os qualificadores de método de [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

Você pode recuperar os qualificadores em um objeto WMI em C# recuperando primeiro o objeto e, em seguida, examinando os qualificadores como uma coleção.

> [!Note]  
> **System.Management era** o namespace original do .NET usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são tão dimensionamento em relação às contrapartes mais modernas **do Microsoft.Management.Infrastructure.**

 

**Para recuperar um qualificador usando C# (System.Management)**

1.  Recupere o objeto cujos qualificadores você deseja exibir usando [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

2.  Coloque os qualificadores em [um QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)e enumere por meio dos [valores de QualifierData.](/dotnet/api/system.management.qualifierdata)

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

O procedimento a seguir descreve como recuperar um qualificador usando o VBScript.

**Para recuperar um qualificador usando o VBScript**

1.  Recupere o objeto cujos qualificadores você deseja exibir, conforme mostrado no exemplo a seguir:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    A maneira mais comum de recuperar um objeto é usando o [**método GetObject.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Para obter mais informações, [consulte Recuperando uma instância WMI](retrieving-an-instance.md).

2.  Acesse os qualificadores do objeto por meio da [**propriedade \_ SWbemObject.Qualifiers,**](swbemobject-qualifiers-.md) conforme mostrado no exemplo a seguir:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

O exemplo de código a seguir descreve como acessar todos os qualificadores em um [**objeto Win32 \_ Process.**](/windows/desktop/CIMWin32Prov/win32-process)


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



O procedimento a seguir descreve como recuperar um qualificador usando C++.

**Para recuperar um qualificador usando C++**

1.  Recupere o objeto cujos qualificadores você deseja exibir.

    A maneira mais comum de recuperar um objeto é usando uma chamada para [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) Para obter mais informações, consulte Recuperando dados de instância ou classe [WMI](retrieving-class-or-instance-data.md).

2.  Recupere o qualificador definido para uma determinada propriedade com uma chamada para métodos [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) ou [**IWbemClassObject::GetMethodQualifierSet.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)

3.  Acesse os qualificadores do objeto por meio da interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) retornada.

## <a name="examples"></a>Exemplos

Para obter mais informações sobre como recuperar qualificadores, consulte o exemplo de código Do PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) na Galeria do TechNet.

 

 
