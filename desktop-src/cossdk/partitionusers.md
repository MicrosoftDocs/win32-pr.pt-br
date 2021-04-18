---
description: Contém um objeto para cada usuário da partição.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Coleção PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807809"
---
# <a name="partitionusers-collection"></a>Coleção PartitionUsers

Contém um objeto para cada usuário da partição.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **PartitionUsers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [AccountName](#accountname)
-   [Defaultparticionaid](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Nome da conta do usuário da partição. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                       |
| Padrão        | "Novo usuário"                                                                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>Defaultparticionaid



| Entrada | Valor |
|----------------|--------------------------------------------------------------------|
| Descrição    | O identificador global exclusivo para a partição de aplicativo base. |
| Access         | ReadWrite                                                          |
| Type           | String                                                             |
| Padrão        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Sistema mínimo | Windows Server 2003                                                |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
