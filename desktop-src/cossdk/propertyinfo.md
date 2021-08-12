---
description: Recupera informações sobre as propriedades com suporte de uma coleção especificada.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Coleção PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf5c354711ec9ca34af1809707a7a869d39a3026ca5cb7ca11d2245c02be049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547559"
---
# <a name="propertyinfo-collection"></a>Coleção PropertyInfo

Recupera informações sobre as propriedades com suporte de uma coleção especificada. A coleção **PropertyInfo** pode ser acessada de qualquer objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . A coleção **PropertyInfo** contém um objeto para cada propriedade que é suportada pela coleção original.

## <a name="members"></a>Membros

A coleção **PropertyInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   **PropertyInfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção de cada coleção.

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)

### <a name="name"></a>Name



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da propriedade. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | ReadOnly                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                           |
| Padrão        | Nenhum                                                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
