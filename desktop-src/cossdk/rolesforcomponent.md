---
description: Contém um objeto para cada função atribuída ao componente ao qual a coleção está relacionada. As funções já devem ser atribuídas no nível do aplicativo.
ms.assetid: c253c72f-908e-4990-ac1a-27e32c99283c
title: Coleção RolesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: e0acd1bfd374c4d0cdb2eb43b49288f0527847abeec97d8bb96c0c5aecd74585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547003"
---
# <a name="rolesforcomponent-collection"></a>Coleção RolesForComponent

Contém um objeto para cada função atribuída ao componente ao qual a coleção está relacionada. As funções já devem ser atribuídas no nível do aplicativo.

Essa coleção dá suporte [**aos métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção RolesForComponent** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da função. Já deve ser uma função atribuída ao aplicativo (que aparece na coleção Funções). Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando [**o método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propriedade Key ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto dessa coleção. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| Type           | String                                                                                                                                                                                                                                                                                                                                              |
| Padrão        | "Nova função"                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
