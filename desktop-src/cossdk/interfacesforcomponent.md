---
description: Contém um objeto para cada interface exposta pelo componente ao qual a coleção está relacionada.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Coleção InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089309"
---
# <a name="interfacesforcomponent-collection"></a>Coleção InterfacesForComponent

Contém um objeto para cada interface exposta pelo componente ao qual a coleção está relacionada.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **InterfacesForComponent** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [CLSID](#clsid)
-   [Descrição](#description)
-   [IID](#iid)
-   [Nome](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|---------------------------|
| Descrição    | Um GUID para o componente. |
| Access         | ReadOnly                  |
| Type           | String                    |
| Padrão        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|----------------------------------|
| Descrição    | Uma descrição para a interface. |
| Access         | ReadWrite                        |
| Type           | String                           |
| Padrão        | ""                               |
| Sistema mínimo | Windows 2000                     |



 

### <a name="iid"></a>IID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID para a interface. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome para a interface. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                    |
| Type           | String                                                                                                                                                      |
| Padrão        | N/D                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Marca a interface como queuable e pode ser definida usando o SDK do administrador ou a ferramenta administrativa serviços de componentes. No entanto, apenas uma interface que tem o sinalizador **com suporte do enfileiramento** pode ter o sinalizador **habilitado para enfileiramento** . |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                               |
| Padrão        | Falso                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | A interface dá suporte à enfileiramento. Para uma interface oferecer suporte ao enfileiramento, todos os métodos devem ter apenas em parâmetros. O **enfileiramento com suporte** é exposto como uma propriedade somente leitura. |
| Access         | ReadOnly                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                   |
| Padrão        | Falso                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
