---
description: Uma classe de exibição Union é uma união lógica de instâncias de classe de origem. Uma classe de exibição Union inclui todas as instâncias das classes de origem, a menos que você limite as instâncias, incluindo uma cláusula WHERE na consulta de origem.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Criando uma classe de exibição Union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612386"
---
# <a name="creating-a-union-view-class"></a>Criando uma classe de exibição Union

Uma classe de exibição Union é uma união lógica de instâncias de classe de origem. Uma classe de exibição Union inclui todas as instâncias das classes de origem, a menos que você limite as instâncias, incluindo uma cláusula WHERE na consulta de origem.

As classes de exibição de União são úteis quando você deseja ver instâncias de classes semelhantes ou idênticas que estão localizadas em namespaces diferentes ou em computadores diferentes. Por exemplo, você pode criar uma classe Union que contém instâncias de unidades de disco diferentes para monitorar.

Você também pode basear as propriedades de uma classe de exibição Union em propriedades que não estão presentes em todas as instâncias de classe de origem. Se as instâncias da classe de origem não tiverem a mesma propriedade, as propriedades das instâncias da classe Union terão um valor de **NULL**. Por exemplo, se uma unidade de disco rígido tiver uma propriedade de **temperatura** , mas outra não, você ainda poderá criar uma União entre as duas.

O procedimento a seguir descreve como criar uma classe de exibição Union.

**Para criar uma classe de exibição Union**

1.  Comece sua definição de classe com o qualificador de cadeia de caracteres [**Union**](qualifiers-specific-to-the-view-provider.md) .

    Os qualificadores [**junção**](qualifiers-specific-to-the-view-provider.md), **Associação** e **União** são mutuamente exclusivos.

2.  Crie as consultas que definem as classes de origem usadas na classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .
3.  Defina os nomes e o local dos namespaces nos quais as classes de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Defina as propriedades que são mapeadas para as propriedades nas classes de origem com o qualificador [**PropertySources**](propertysources-qualifier.md) .

    Se necessário, você pode marcar qualquer uma das propriedades como pertencente a uma classe de origem usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Defina as propriedades de chave das classes de origem da classe de exibição Union.

    Cada classe de origem deve ter o mesmo número de propriedades de chave correspondidas por [**CIMType**](swbemproperty-cimtype.md). Além disso, as chaves da sua classe de exibição Union devem identificar exclusivamente todas as instâncias de origem. Em alguns casos, talvez seja necessário especificar as propriedades do sistema para garantir que as instâncias sejam exclusivas. Por exemplo, se você criar uma exibição da União de duas classes idênticas em dois namespaces diferentes, você poderá incluir a propriedade [**\_ \_ namespace**](--namespace.md) como uma chave na classe de exibição para diferenciar entre as duas instâncias. Se você usar duas classes semelhantes do mesmo namespace para criar uma exibição, poderá usar a propriedade **\_ \_ Class** para distinguir entre as duas. Renomeie as propriedades do sistema na exibição para que você possa evitar um conflito com as propriedades do sistema da classe View.

6.  Defina os métodos desejados usando o qualificador [**MethodName**](qualifiers-specific-to-the-view-provider.md) .

    Ao contrário de outras classes de exibição, você pode criar métodos para modificar uma exibição de União.

O exemplo de código a seguir descreve uma classe de exibição Union.

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



