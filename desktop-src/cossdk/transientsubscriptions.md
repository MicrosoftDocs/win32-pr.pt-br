---
description: Contém um objeto para cada assinatura transitória. As assinaturas transitórias podem ser criadas em tempo real para executar instâncias de objeto e desaparecerem quando o objeto for destruído.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Coleção TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5053a4fd488ed38a637b4296f94caf20887f3ed924ae6d11b8f6a242669eccad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853926"
---
# <a name="transientsubscriptions-collection"></a>Coleção TransientSubscriptions

Contém um objeto para cada assinatura transitória. As assinaturas transitórias podem ser criadas em tempo real para executar instâncias de objeto e desaparecerem quando o objeto for destruído.

Essa coleção dá suporte [**aos métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção TransientSubscriptions** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Raiz**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Descrição](#description)
-   [Habilitada](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [Filtercriteria](#filtercriteria)
-   [ID](#transientsubscriptions-collection)
-   [Interfaceid](#interfaceid)
-   [MethodName](#methodname)
-   [Nome](#methodname)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|-------------------------------------|
| Descrição    | Uma descrição para a assinatura. |
| Access         | ReadWrite                           |
| Type           | String                              |
| Padrão        | ""                                  |
| Sistema mínimo | Windows 2000                        |



 

### <a name="enabled"></a>habilitado



| Entrada | Valor |
|----------------|----------------------------------------------------------|
| Descrição    | Indica se a assinatura está habilitada no momento. |
| Access         | ReadWrite                                                |
| Tipo           | Bool                                                     |
| Padrão        | Verdadeiro                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Ao assinar uma classe de evento, usado para representar o GUID da ID de partição que contém a classe de evento. Ao assinar classes de evento, o assinante tem a opção de assinar uma classe de evento na mesma partição ou em uma partição diferente. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                                             |
| Padrão        | NULO                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------|
| Descrição    | O CLSID para a classe de evento. Você pode indicar um EventCLSID ou um PublisherID, mas não ambos. |
| Access         | WriteOnce                                                                                    |
| Type           | String                                                                                       |
| Padrão        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>Filtercriteria



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma cadeia de caracteres que indica os critérios de filtro. Pode ser um CLSID para uma [**classe PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Access         | ReadWrite                                                                                                            |
| Type           | String                                                                                                               |
| Padrão        | N/D                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                         |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Identificador da assinatura. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                        |
| Type           | String                                                                                                                                                           |
| Padrão        | <Generated>                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Valor |
|----------------|----------------------------------|
| Descrição    | IID para interface assinada para. |
| Access         | WriteOnce                        |
| Type           | String                           |
| Padrão        | N/D                              |
| Sistema mínimo | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Entrada | Valor |
|----------------|----------------------------------------------|
| Descrição    | Método na interface que está sendo assinada. |
| Access         | ReadWrite                                    |
| Type           | String                                       |
| Padrão        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome da assinatura. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                 |
| Padrão        | "Nova assinatura"                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>Peruser



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se a assinatura se aplica somente a um determinado usuário, representado pela propriedade UserName. |
| Access         | ReadWrite                                                                                               |
| Tipo           | Bool                                                                                                    |
| Padrão        | Falso                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Descrição    | ID do Publicador. Você pode indicar um EventCLSID ou um PublisherID, mas não ambos. |
| Access         | WriteOnce                                                                           |
| Type           | String                                                                              |
| Padrão        | ""                                                                                  |
| Sistema mínimo | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Entrada | Valor |
|----------------|------------------------------------------|
| Descrição    | Um ponteiro para a interface do Assinante. |
| Access         | ReadWrite                                |
| Tipo           | Variante                                  |
| Padrão        | N/D                                      |
| Sistema mínimo | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Ao assinar uma classe de evento na mesma partição, usada para representar o GUID da ID de partição do Assinante. Ao assinar as classes de evento, o Assinante tem a opção de assinar uma classe de evento na mesma partição ou em outra. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | String                                                                                                                                                                                                                                                          |
| Padrão        | <Generated>                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------|
| Descrição    | O nome do usuário ao que a assinatura se aplica quando PerUser é True. |
| Access         | ReadWrite                                                               |
| Type           | String                                                                  |
| Padrão        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
