---
description: Contém um objeto para cada função atribuída ao método ao qual a coleção está relacionada. As funções já devem estar atribuídas no nível do aplicativo.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Coleção RolesForMethod
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: 01579f460ceb9a3099adefef48e9fc203e042956713478273ce654fce3a34022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047274"
---
# <a name="rolesformethod-collection"></a>Coleção RolesForMethod

Contém um objeto para cada função atribuída ao método ao qual a coleção está relacionada. As funções já devem estar atribuídas no nível do aplicativo.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **RolesForMethod** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**MethodsForInterface**](methodsforinterface.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da função. Já deve ser uma função atribuída ao aplicativo (que aparece na coleção de funções). Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| Type           | String                                                                                                                                                                                                                                                                                                                                              |
| Padrão        | "Nova função"                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
