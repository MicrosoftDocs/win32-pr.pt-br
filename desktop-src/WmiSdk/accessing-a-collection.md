---
description: Uma coleção é um conceito de automação padrão que fornece uma interface uniforme para um conjunto de objetos sobre os quais você pode executar a iteração.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Acessando uma coleção WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860507"
---
# <a name="accessing-a-wmi-collection"></a>Acessando uma coleção WMI

Uma coleção é um conceito de automação padrão que fornece uma interface uniforme para um conjunto de objetos sobre os quais você pode executar a iteração. A API de script para o WMI expõe várias interfaces que estão em conformidade com o paradigma da coleção. Em cada caso, use o método **Item** para identificar os elementos usando uma cadeia de caracteres que contém o valor.

As coleções [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemMethodSet**](swbemmethodset.md) são usadas principalmente para modificar o esquema. Um objeto [**SWbemObjectSet**](swbemobjectset.md) contém objetos WMI, como uma instância [**de \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , que foram obtidos por meio de chamadas, como [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemObject. ASSOCIATORS \_**](swbemobject-associators-.md). O objeto [**SWbemRefresher**](swbemrefresher.md) só pode conter instâncias de classes WMI. O objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) pode conter objetos WMI ou qualquer outro tipo de dados que um provedor requer para a chamada de método.

> [!Note]  
> Os tópicos a seguir foram escritos principalmente para o VBScript. O C# usa a interface padrão [IEnumerable](/dotnet/api/system.collections.ienumerable) para agrupar e enumerar objetos. Por outro lado, o PowerShell geralmente usa uma coleção de objetos implícita sempre que um valor de retorno contém mais de um resultado.

 

A tabela a seguir lista as coleções na API de script para WMI e os elementos e parâmetros para cada coleção.



| Coleção                                       | Elemento                                              | Parâmetro Item ()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Caminho do objeto                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Nome da propriedade                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Nome de qualificador                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nome do método                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nome do valor                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nome do privilégio                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Índice do item no objeto [**SWbemRefresher**](swbemrefresher.md) |



 

Para obter mais informações sobre o e exemplos de adição e remoção de itens de uma coleção, consulte [removendo um único item de uma coleção](removing-a-single-item-from-a-collection.md) e [removendo vários itens de uma coleção](removing-multiple-items-from-a-collection.md). Para obter mais informações sobre como trabalhar com classes, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

 

 
