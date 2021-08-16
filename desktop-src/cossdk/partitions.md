---
description: Especifica os aplicativos contidos em cada partição.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Coleção de partições
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3badf52755a77557c200569c25610b5918cf8dd599d17a83bdebb5c4ddfa6801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305869"
---
# <a name="partitions-collection"></a>Coleção de partições

Especifica os aplicativos contidos em cada partição.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção de **partições** é herdada da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**Aplicativos**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Mutável](#changeable)
-   [Pode ser excluído](#deleteable)
-   [Descrição](#description)
-   [ID](#partitions-collection)
-   [Nome](#name)

### <a name="changeable"></a>Mutável



| Entrada | Valor |
|----------------|--------------------------------------------------|
| Descrição    | Determina se esta partição é alterável. |
| Acesso         | ReadWrite                                        |
| Type           | Bool                                             |
| Padrão        | True                                             |
| Sistema mínimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Pode ser excluído



| Entrada | Valor |
|----------------|---------------------------------------------------|
| Descrição    | Determina se esta partição pode ser excluída. |
| Acesso         | ReadWrite                                         |
| Type           | Bool                                              |
| Padrão        | True                                              |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|---------------------------------------------------------------------|
| Descrição    | Essa propriedade representa a descrição que identifica a partição. |
| Acesso         | ReadWrite                                                           |
| Type           | String                                                              |
| Padrão        | ""                                                                  |
| Sistema mínimo | Windows Server 2003                                                 |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID que representa a partição. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Acesso         | WriteOnce                                                                                                                                                          |
| Type           | String                                                                                                                                                             |
| Padrão        | <Generated>                                                                                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Name



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Representa o nome da partição. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | ReadWrite                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                 |
| Padrão        | "Nova partição"                                                                                                                                                                                                                        |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
