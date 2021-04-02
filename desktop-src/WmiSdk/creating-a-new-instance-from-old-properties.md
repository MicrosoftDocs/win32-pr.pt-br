---
description: Uma classe de exibição de junção contém propriedades de instâncias de classe de origem que são conectadas por um valor de propriedade comum, como Class1. Prop1 = class2. Prop2. Cada instância em uma classe de exibição de junção consiste em partes de instâncias de classe diferentes.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Criando uma nova instância de propriedades antigas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922596"
---
# <a name="creating-a-new-instance-from-old-properties"></a>Criando uma nova instância de propriedades antigas

Uma classe de exibição de junção contém propriedades de instâncias de classe de origem que são conectadas por um valor de propriedade comum, como **Class1. Prop1**  =  **class2. Prop2**. Cada instância em uma classe de exibição de junção consiste em partes de instâncias de classe diferentes.

Você pode basear uma classe de exibição de junção em desigualdade de valores de propriedade, como **Class1. Prop1**  <>  **class2. Prop2** , em que **Prop1** e **Prop2** não são mapeados para a mesma propriedade na classe View.

Uma classe de exibição de junção é útil quando as informações que você está procurando estão contidas em classes separadas, mas relacionadas. Por exemplo, se você quiser obter informações sobre uma impressora e sobre a configuração da impressora, poderá criar uma classe de exibição de junção que contenha algumas das propriedades da classe de [**\_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e algumas das propriedades da classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) . Sem o provedor de exibição, você deve recuperar e mesclar as propriedades das instâncias separadas para obter as informações necessárias.

O procedimento a seguir descreve como criar uma classe de exibição de junção.

**Para criar uma classe de exibição de junção**

1.  Inicie uma definição de classe com o qualificador de cadeia de [**junção**](qualifiers-specific-to-the-view-provider.md) .

    Os qualificadores [**junção**](qualifiers-specific-to-the-view-provider.md), **Associação** e **União** são mutuamente exclusivos.

2.  Se necessário, filtre as instâncias desejadas na classe Join aplicando o qualificador [**PostJoinFilter**](postjoinfilter-qualifier.md) .

    O provedor [**PostJoinFilter**](postjoinfilter-qualifier.md) permite restringir as instâncias de uma classe de exibição para instâncias que atendem a condições específicas.

3.  Crie as consultas que definem instâncias de origem da classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .
4.  Defina os nomes e locais dos namespaces onde as instâncias de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .
5.  Defina as propriedades desejadas em uma classe de exibição de junção com o qualificador [**PropertySources**](propertysources-qualifier.md) .

    Quando as propriedades são adicionadas à exibição de junção com base na igualdade, as duas propriedades de origem devem ser mapeadas em um qualificador de [**PropertySources**](propertysources-qualifier.md) .

    O exemplo de código a seguir mostra duas propriedades mapeadas em um qualificador **PropertySources** .

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    Usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , você pode marcar as propriedades que pertencem a uma classe de origem.

O exemplo de código a seguir mostra uma classe de exibição de junção criada a partir das classes do provedor do monitor de desempenho [**Win32 \_ PerfRawData \_ PerfProc \_ process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) e [**Win32 \_ PerfRawData \_ PerfProc \_ thread**](/previous-versions//aa394325(v=vs.85)) com propriedades de ambas as classes Unidas pela propriedade **ProcessId** .

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
