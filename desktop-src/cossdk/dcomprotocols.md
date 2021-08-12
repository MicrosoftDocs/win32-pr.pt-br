---
description: Contém uma lista dos protocolos a serem usados pelo DCOM. Ele contém um objeto para cada protocolo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Coleção DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548015"
---
# <a name="dcomprotocols-collection"></a>Coleção DCOMProtocols

Contém uma lista dos protocolos a serem usados pelo DCOM. Ele contém um objeto para cada protocolo.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **DCOMProtocols** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Nome](#name)
-   [Ordem](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Name



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do protocolo. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | ReadWrite                                                                                                                                                   |
| Type           | String                                                                                                                                                      |
| Padrão        | "Novo protocolo"                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Ordem



| Entrada | Valor |
|----------------|-----------------------------------------|
| Descrição    | A ordem na qual tentar o protocolo. |
| Acesso         | ReadWrite                               |
| Digite           | Longo (0-65000)                          |
| Padrão        | 0                                       |
| Sistema mínimo | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O código que especifica a sequência de protocolo RPC. Os códigos de protocolo com suporte incluem o seguinte: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Acesso         | WriteOnce                                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                                      |
| Padrão        | ""                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
