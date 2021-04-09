---
description: A coleção RolesForPartition sempre está relacionada a um objeto na coleção de partições. Ele contém um objeto para cada função atribuída à partição à qual ele está relacionado.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Coleção RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089049"
---
# <a name="rolesforpartition-collection"></a>Coleção RolesForPartition

A coleção **RolesForPartition** sempre está relacionada a um objeto na coleção de [**partições**](partitions.md) . Ele contém um objeto para cada função atribuída à partição à qual ele está relacionado.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **RolesForPartition** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Partições**](partitions.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Descrição](#description)
-   [Nome](#name)

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|----------------------------|
| Descrição    | Uma descrição da função. |
| Access         | ReadOnly                   |
| Type           | String                     |
| Padrão        | ""                         |
| Sistema mínimo | Windows Server 2003        |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da função. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                                                                      |
| Padrão        | ""                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
