---
description: Coleção UsersInPartitionRole – contém um objeto para cada usuário na função à qual a coleção está relacionada.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Coleção UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: d07c62fc6c6cc871f803b1f752201bd500e2705c3cfca272ff350ffd018f6018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499637"
---
# <a name="usersinpartitionrole-collection"></a>Coleção UsersInPartitionRole

Contém um objeto para cada usuário na função à qual a coleção está relacionada.

Essa coleção dá suporte [**aos métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção UsersInPartitionRole** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Usuário](#usersinpartitionrole-collection)

### <a name="user"></a>Usuário



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do usuário. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto dessa coleção. |
| Access         | WriteOnce                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                |
| Padrão        | "Novo usuário"                                                                                                                                                                            |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
