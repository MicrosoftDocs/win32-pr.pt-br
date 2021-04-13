---
description: Contém um objeto para cada método na interface à qual a coleção está relacionada.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Coleção MethodsForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370504"
---
# <a name="methodsforinterface-collection"></a>Coleção MethodsForInterface

Contém um objeto para cada método na interface à qual a coleção está relacionada.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **MethodsForInterface** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Preenchimento automático](#autocomplete)
-   [CLSID](#clsid)
-   [Descrição](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Nome](#name)

### <a name="autocomplete"></a>AutoComplete



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se o objeto é desativado automaticamente quando o método é concluído, sem SetComplete ou SetAbort, necessariamente sendo chamado. Isso afeta apenas a configuração padrão do bit "Done" de ativação JIT no método Start; Esse bit pode ser redefinido (como com SetComplete ou SetAbort) dentro do método para substituir o padrão. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

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
|----------------|------------------------------|
| Descrição    | Uma descrição do método. |
| Access         | ReadWrite                    |
| Type           | String                       |
| Padrão        | ""                           |
| Sistema mínimo | Windows 2000                 |



 

### <a name="iid"></a>IID



| Entrada | Valor |
|----------------|---------------------------|
| Descrição    | Um GUID para a interface. |
| Access         | ReadOnly                  |
| Type           | String                    |
| Padrão        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="index"></a>Índice



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O identificador de expedição do método. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                        |
| Tipo           | **DWORD**                                                                                                                                                       |
| Padrão        | N/D                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do método. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                           |
| Type           | String                                                                                                                                             |
| Padrão        | N/D                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
