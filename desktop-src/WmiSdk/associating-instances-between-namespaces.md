---
description: Uma classe de exibição de associação permite que você use ASSOCIAdores de consultas em classes que residem em namespaces diferentes.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associando instâncias entre namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296894"
---
# <a name="associating-instances-between-namespaces"></a>Associando instâncias entre namespaces

Uma classe de exibição de associação permite que você use [ASSOCIADORES de](associators-of-statement.md) consultas em classes que residem em namespaces diferentes.

O procedimento a seguir descreve como associar instâncias entre namespaces.

**Para associar instâncias entre namespaces**

1.  Comece sua definição de classe com o qualificador de cadeia de [**Associação**](meta-qualifiers.md) .

    Os qualificadores **junção**, [**Associação**](meta-qualifiers.md)e **União** são mutuamente exclusivos.

2.  Crie as consultas que definem as instâncias de origem usadas na classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .
3.  Defina os nomes e o local dos namespaces nos quais as instâncias de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Defina as propriedades desejadas em sua classe de exibição de associação com o qualificador [**PropertySources**](propertysources-qualifier.md) .

    Se necessário, você pode marcar qualquer uma das propriedades como pertencente a uma classe de origem usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Marque todas as propriedades relevantes com o qualificador **direto** .

    O qualificador **direto** impede que o provedor de exibição mapeie a referência de associação marcada para uma referência de exibição.

Os exemplos de código a seguir mostram como criar classes de exibição de associação.

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



