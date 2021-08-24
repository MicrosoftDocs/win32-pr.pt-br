---
description: A coleção RolesForPartition está sempre relacionada a um objeto na coleção Partitions. Ele contém um objeto para cada função atribuída à partição à qual ela está relacionada.
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
ms.openlocfilehash: 6c1e64e314478793a5b421d1f0a6a76c2eb028708410a14ea426f52fbd41dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637036"
---
# <a name="rolesforpartition-collection"></a>Coleção RolesForPartition

A **coleção RolesForPartition** está sempre relacionada a um objeto na [**coleção Partitions.**](partitions.md) Ele contém um objeto para cada função atribuída à partição à qual ela está relacionada.

Essa coleção não dá suporte aos [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção RolesForPartition** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Partições**](partitions.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

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
| Descrição    | O nome da função. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto dessa coleção. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                                                                      |
| Padrão        | ""                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
