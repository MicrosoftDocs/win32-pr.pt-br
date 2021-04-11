---
description: Recupera informações sobre classes de evento.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Coleção EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089134"
---
# <a name="eventclassesforiid-collection"></a>Coleção EventClassesForIID

Recupera informações sobre classes de evento.

A conexão entre o Publicador e assinantes é gerenciada por um objeto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , que é um componente com+ que contém as interfaces e os métodos usados por um Publicador para acionar eventos.

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **EventClassesForIID** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Aplicativo](#application)
-   [Número de bits](#bitness)
-   [CLSID](#clsid)
-   [Descrição](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Aplicativo



| Entrada | Valor |
|----------------|----------------------------------------------------------|
| Descrição    | O GUID do aplicativo que contém a classe de evento. |
| Access         | ReadOnly                                                 |
| Type           | String                                                   |
| Padrão        | N/D                                                      |
| Sistema mínimo | Windows XP                                               |



 

### <a name="bitness"></a>Número de bits



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Representa o tipo de bit de bits binário da classe de evento. Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                                |
| Tipo           | Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                           |
| Padrão        | N/D                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O GUID para a classe de evento. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                      |
| Type           | String                                                                                                                                                        |
| Padrão        | N/D                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|----------------------------|
| Descrição    | Descreve a classe de evento. |
| Access         | ReadOnly                   |
| Type           | String                     |
| Padrão        | ""                         |
| Sistema mínimo | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Valor |
|----------------|---------------------------------------------------------|
| Descrição    | Indica se o componente de classe de evento é privado. |
| Access         | ReadOnly                                                |
| Tipo           | Bool                                                    |
| Padrão        | Falso                                                   |
| Sistema mínimo | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome amigável usado para identificar a classe de evento. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                            |
| Type           | String                                                                                                                                                                              |
| Padrão        | ""                                                                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
