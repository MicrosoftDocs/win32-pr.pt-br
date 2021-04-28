---
description: Coleção UsersInPartitionRole – contém um objeto para cada usuário na função ao qual a coleção está relacionada.
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
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105544"
---
# <a name="usersinpartitionrole-collection"></a>Coleção UsersInPartitionRole

Contém um objeto para cada usuário na função ao qual a coleção está relacionada.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **UsersInPartitionRole** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Usuário](#usersinpartitionrole-collection)

### <a name="user"></a>Usuário



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do usuário. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                |
| Padrão        | "Novo usuário"                                                                                                                                                                            |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
