---
description: Contém um objeto para cada assinatura da coleção pai Components.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Coleção SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: be18f77c4946a5d8a79adc09e97bc9ab35782fdb837f15b82794cbf5f624d59d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546158"
---
# <a name="subscriptionsforcomponent-collection"></a>Coleção SubscriptionsForComponent

Contém um objeto para cada assinatura da coleção pai [**Components.**](components.md)

Essa coleção dá suporte [**aos métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membros

A **coleção SubscriptionsForComponent** herda da interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte no [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [Descrição](#description)
-   [Habilitada](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [Filtercriteria](#filtercriteria)
-   [ID](#subscriptionsforcomponent-collection)
-   [Interfaceid](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [Nome](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [Em fila](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|-------------------------------------|
| Descrição    | Uma descrição para a assinatura. |
| Acesso         | ReadWrite                           |
| Type           | String                              |
| Padrão        | ""                                  |
| Sistema mínimo | Windows 2000                        |



 

### <a name="enabled"></a>Habilitada



| Entrada | Valor |
|----------------|----------------------------------------------------------|
| Descrição    | Indica se a assinatura está habilitada no momento. |
| Acesso         | ReadWrite                                                |
| Digite           | Bool                                                     |
| Padrão        | True                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Ao assinar uma classe de evento, usado para representar o GUID da ID de partição que contém a classe de evento. Ao assinar classes de evento, o assinante tem a opção de assinar uma classe de evento na mesma partição ou em uma partição diferente. |
| Acesso         | ReadWrite                                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                                             |
| Padrão        | NULO                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------|
| Descrição    | O CLSID para a classe de evento. Você pode indicar um EventCLSID ou um PublisherID, mas não ambos. |
| Acesso         | WriteOnce                                                                                    |
| Type           | String                                                                                       |
| Padrão        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>Filtercriteria



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma cadeia de caracteres que indica os critérios de filtro. Pode ser um CLSID para uma [**classe PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Acesso         | ReadWrite                                                                                                        |
| Type           | String                                                                                                           |
| Padrão        | N/D                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                     |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Identificador da assinatura. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Acesso         | WriteOnce                                                                                                                                                        |
| Type           | String                                                                                                                                                           |
| Padrão        | <Generated>                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Valor |
|----------------|------------------------------------------|
| Descrição    | O IID para a interface assinada. |
| Acesso         | ReadWrite                                |
| Type           | String                                   |
| Padrão        | N/D                                      |
| Sistema mínimo | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------|
| Descrição    | Um nome de computador remoto para assinaturas para classes de evento em um computador remoto. |
| Acesso         | ReadWrite                                                                       |
| Type           | String                                                                          |
| Padrão        | ""                                                                              |
| Sistema mínimo | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Entrada | Valor |
|----------------|----------------------------------------------|
| Descrição    | Método na interface que está sendo assinada. |
| Acesso         | ReadWrite                                    |
| Type           | String                                       |
| Padrão        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Name



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Nome da assinatura. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Acesso         | ReadWrite                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                             |
| Padrão        | "Nova assinatura"                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>Peruser



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------|
| Descrição    | Indica se a assinatura se aplica somente a um determinado usuário, UserName. |
| Acesso         | ReadWrite                                                                   |
| Digite           | Bool                                                                        |
| Padrão        | Falso                                                                       |
| Sistema mínimo | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Descrição    | A ID do Publicador. Você pode indicar um EventCLSID ou um PublisherID, mas não ambos. |
| Acesso         | WriteOnce                                                                               |
| Type           | String                                                                                  |
| Padrão        | ""                                                                                      |
| Sistema mínimo | Windows 2000                                                                            |



 

### <a name="queued"></a>Em fila



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descrição    | Indica se a assinatura está na fila. |
| Acesso         | ReadWrite                                     |
| Digite           | Bool                                          |
| Padrão        | Falso                                         |
| Sistema mínimo | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Descrição    | Um moniker para um assinante marcado como Na fila. Um valor padrão é gerado quando Na fila é inicialmente definido como True. |
| Acesso         | ReadWrite                                                                                                       |
| Type           | String                                                                                                          |
| Padrão        | N/D                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Ao assinar uma classe de evento na mesma partição, usado para representar o GUID da ID de partição do assinante. Ao assinar classes de evento, o assinante tem a opção de assinar uma classe de evento na mesma partição ou em uma partição diferente. |
| Acesso         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | String                                                                                                                                                                                                                                                          |
| Padrão        | <Generated>                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------|
| Descrição    | O nome do usuário ao que a assinatura se aplica, quando PerUser é True. |
| Acesso         | ReadWrite                                                                |
| Type           | String                                                                   |
| Padrão        | N/D                                                                      |
| Sistema mínimo | Windows 2000                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
