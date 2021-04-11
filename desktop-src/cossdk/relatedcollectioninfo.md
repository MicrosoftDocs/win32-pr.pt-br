---
description: Recupera informações sobre outras coleções relacionadas à coleção da qual ela é chamada.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Coleção RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164018"
---
# <a name="relatedcollectioninfo-collection"></a>Coleção RelatedCollectionInfo

Recupera informações sobre outras coleções relacionadas à coleção da qual ela é chamada. A coleção **RelatedCollectionInfo** pode ser acessada de qualquer objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . A coleção **RelatedCollectionInfo** contém um objeto para cada coleção que é acessível da coleção original. As coleções relacionadas seguem a hierarquia da coleção de ferramentas de administração de serviços de componentes.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **RelatedCollectionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

Você pode navegar até essa coleção de cada coleção.

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da coleção relacionada. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                     |
| Padrão        | Nenhum                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
