---
description: Recupera informações sobre as propriedades compatíveis com uma coleção especificada.
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

Recupera informações sobre as propriedades compatíveis com uma coleção especificada. A **coleção PropertyInfo** é acessível de [**qualquer objeto COMAdminCatalogCollection**](comadmincatalogcollection.md) usando o [**método GetCollection.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) A **coleção PropertyInfo** contém um objeto para cada propriedade com suporte da coleção original.

## <a name="members"></a>Membros

A **coleção PropertyInfo** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   **Propertyinfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção de cada coleção.

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da propriedade. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto dessa coleção. |
| Access         | ReadOnly                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                           |
| Padrão        | Nenhum                                                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
