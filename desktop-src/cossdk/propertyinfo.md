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
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089306"
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

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da propriedade. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                           |
| Padrão        | Nenhum                                                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
