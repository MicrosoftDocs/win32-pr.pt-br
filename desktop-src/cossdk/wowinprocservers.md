---
description: Contém uma lista dos servidores em processo registrados com o sistema para componentes de 32 bits em computadores de 64 bits. Ele contém um objeto para cada componente.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Coleção WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: d85abf322d34d03c0f5e8863b5434343946b676e477e18077c82d83de78cafb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545567"
---
# <a name="wowinprocservers-collection"></a>Coleção WOWInprocServers

Contém uma lista dos servidores em processo registrados com o sistema para componentes de 32 bits em computadores de 64 bits. Ele contém um objeto para cada componente.

Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membros

A coleção **WOWInprocServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID para o componente. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Acesso         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Valor |
|----------------|----------------------------------|
| Descrição    | O caminho do arquivo para o componente. |
| Acesso         | ReadOnly                         |
| Type           | String                           |
| Padrão        | N/D                              |
| Sistema mínimo | Windows XP                       |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome que identifica o componente. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | ReadOnly                                                                                                                                                            |
| Type           | String                                                                                                                                                              |
| Padrão        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
