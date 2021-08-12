---
description: Contém um objeto para cada propriedade do Publicador da coleção SubscriptionsForComponent pai.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Coleção publisherproperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e5876e01a557e9a585423a9e438e773366ca9eaa73e9e67fdaeae8a957b90c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547150"
---
# <a name="publisherproperties-collection"></a>Coleção publisherproperties

Contém um objeto para cada propriedade do Publicador da coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) pai.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **publisherproperties** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)
-   [Valor](#value)

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da propriedade. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Padrão        | "Nova propriedade"                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Valor



| Entrada | Valor |
|----------------|---------------------------|
| Descrição    | Um valor para a propriedade. |
| Acesso         | ReadWrite                 |
| Digite           | Variante                   |
| Padrão        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
