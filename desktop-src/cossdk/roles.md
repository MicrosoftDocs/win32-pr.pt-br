---
description: A coleção de funções sempre está relacionada a um objeto na coleção de aplicativos. Ele contém um objeto para cada função atribuída ao aplicativo ao qual ele está relacionado.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Coleção de funções
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029466"
---
# <a name="roles-collection"></a>Coleção de funções

A coleção de **funções** sempre está relacionada a um objeto na coleção de [**aplicativos**](applications.md) . Ele contém um objeto para cada função atribuída ao aplicativo ao qual ele está relacionado.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção de **funções** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Aplicativos**](applications.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Descrição](#description)
-   [Nome](#name)

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|----------------------------|
| Descrição    | Uma descrição da função. |
| Access         | ReadWrite                  |
| Type           | String                     |
| Padrão        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da função. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                      |
| Padrão        | "Nova função"                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
