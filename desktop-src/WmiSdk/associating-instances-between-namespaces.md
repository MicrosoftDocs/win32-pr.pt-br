---
description: Uma classe de exibição de associação permite que você use consultas ASSOCIATORS OF em classes que residem em namespaces diferentes.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associando instâncias entre namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557014"
---
# <a name="associating-instances-between-namespaces"></a>Associando instâncias entre namespaces

Uma classe de exibição de associação permite que você use [consultas ASSOCIATORS OF](associators-of-statement.md) em classes que residem em namespaces diferentes.

O procedimento a seguir descreve como associar instâncias entre namespaces.

**Para associar instâncias entre namespaces**

1.  Comece sua definição de classe com o [**Qualificador de cadeia**](meta-qualifiers.md) de caracteres de associação.

    Os **qualificadores JoinOn,** [**Association**](meta-qualifiers.md)e **Union** são mutuamente exclusivos.

2.  Crie as consultas que definem instâncias de origem usadas na classe view com o qualificador [**ViewSources.**](viewsources-qualifier.md)
3.  Defina os nomes e o local dos namespaces nos quais as instâncias de origem estão localizadas com o qualificador [**ViewSpaces.**](viewspaces-qualifier.md)
4.  Defina as propriedades que você deseja na classe de exibição de associação com o qualificador [**PropertySources.**](propertysources-qualifier.md)

    Se necessário, você pode marcar qualquer uma das propriedades como pertencentes a uma classe de origem usando o qualificador [**HiddenDefault.**](qualifiers-specific-to-the-view-provider.md)

5.  Marque as propriedades relevantes com o **qualificador** Direto.

    O **qualificador** Direto impede que o Provedor de Exibição mapeie a referência de associação marcada para uma referência de exibição.

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

 

 



