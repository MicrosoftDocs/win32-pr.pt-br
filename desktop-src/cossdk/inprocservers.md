---
description: Contém uma lista dos servidores em processo registrados no sistema. Ele contém um objeto para cada componente registrado como um servidor em processo.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Coleção InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790326"
---
# <a name="inprocservers-collection"></a>Coleção InprocServers

Contém uma lista dos servidores em processo registrados no sistema. Ele contém um objeto para cada componente registrado como um servidor em processo.

Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membros

A coleção **InprocServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

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
| Access         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Valor |
|----------------|----------------------------------|
| Descrição    | O caminho do arquivo para o componente. |
| Access         | ReadOnly                         |
| Type           | String                           |
| Padrão        | N/D                              |
| Sistema mínimo | Windows 2000                     |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome que identifica o componente. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | String                                                                                                                                                              |
| Padrão        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
