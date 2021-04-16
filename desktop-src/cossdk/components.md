---
description: Contém um objeto para cada componente no aplicativo relacionado.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Coleção de componentes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501091"
---
# <a name="components-collection"></a>Coleção de componentes

Contém um objeto para cada componente no aplicativo relacionado. A coleção de **componentes** está sempre relacionada a um objeto na coleção de [**aplicativos**](applications.md) . As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.

Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membros

A coleção de **componentes** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Aplicativos**](applications.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [Número de bits](#bitness)
-   [CLSID](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [Construtorstring](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [Descrição](#description)
-   [DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [ExceptionClass](#exceptionclass)
-   [FireInParallel](#fireinparallel)
-   [IISIntrinsics](#iisintrinsics)
-   [InitializeServerApplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [IsEventClass](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [IsPrivateComponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [MultiInterfacePublisherFilterCLSID](#multiinterfacepublisherfilterclsid)
-   [MustRunInClientContext](#mustruninclientcontext)
-   [MustRunInDefaultContext](#mustrunindefaultcontext)
-   [ObjectPoolingEnabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [SoapAssemblyName](#soapassemblyname)
-   [SoapTypeName](#soaptypename)
-   [Sincronização](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [Transação](#componenttransactiontimeout)
-   [TxIsolationLevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [VersionSubBuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>AllowInprocSubscribers



| Entrada | Valor |
|----------------|--------------------------------------------------------------------|
| Descrição    | Habilita os assinantes do processo se o componente for uma classe de evento. |
| Access         | ReadWrite                                                          |
| Tipo           | Bool                                                               |
| Padrão        | True                                                               |
| Sistema mínimo | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O GUID do aplicativo que contém o componente. Deve ser um GUID de aplicativo válido, que é verificado antes que [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) seja chamado. Se esse valor for alterado para ser um GUID para um aplicativo diferente, o componente será movido para esse aplicativo. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                        |
| Type           | String                                                                                                                                                                                                                                                                                           |
| Padrão        | N/D                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Número de bits



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Representa o tipo de bit de bits binário de um componente. Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                            |
| Tipo           | Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                       |
| Padrão        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID para o componente. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se as verificações de acesso baseado em função são executadas em chamadas no componente e funcionam em conjunto com as propriedades AccessChecksLevel e ApplicationAccessChecksEnabled no aplicativo. |
| Access         | ReadWrite                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                       |
| Padrão        | Falso                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Quando usado em uma transação, especifica o período de tempo em que esse componente faz com que a transação expire. O padrão é 60 segundos e não pode ter mais de 3600 segundos (1 hora). O valor de tempo limite pode ser definido como 0, especificando um período de tempo limite de transação infinito. Para que essa propriedade seja usada, ComponentTransactionTimeoutEnabled deve ser true. O valor dessa propriedade substitui o tempo limite da transação global especificado pela propriedade TransactionTimeout da coleção [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Tipo           | Longo (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Padrão        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Especifica se o período de tempo limite da transação está habilitado para este componente. Por padrão, o recurso de tempo limite da transação é desabilitado. Quando essa propriedade é true, o tempo limite especificado por ComponentTransactionTimeout é usado. Quando essa propriedade é falsa, o tempo limite especificado pela propriedade TransactionTimeout da coleção [**LocalComputer**](localcomputer.md) é usado. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Habilita a passagem de propriedades de contexto do COMTI (integrador de transações COM) para o contexto desta classe. A COMTI facilita a tarefa de encapsular as transações de mainframe e a lógica de negócios como componentes COM. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Padrão        | Falso                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------|
| Descrição    | Determina se constructorString são passados para o objeto quando ele é construído. |
| Access         | ReadWrite                                                                                |
| Tipo           | Bool                                                                                     |
| Padrão        | Falso                                                                                    |
| Sistema mínimo | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>Construtorstring



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Cadeia de inicialização para construção de componente. Você pode criar objetos diferentes do mesmo componente genérico usando cadeias de caracteres do construtor de objetos. Se ConstructionEnabled for false, essa propriedade será ignorada. |
| Access         | ReadWrite                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                             |
| Padrão        | ""                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Ao criar o objeto, o número de milissegundos antes de um erro de tempo limite é retornado. O tempo limite máximo é de 2147483647 milissegundos (cerca de 25 dias). |
| Access         | ReadWrite                                                                                                                                              |
| Tipo           | Longo (0-2147483647)                                                                                                                                    |
| Padrão        | 0                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|--------------------------|
| Descrição    | Descreve o componente. |
| Access         | ReadWrite                |
| Type           | String                   |
| Padrão        | ""                       |
| Sistema mínimo | Windows 2000             |



 

### <a name="dll"></a>DLL



| Entrada | Valor |
|----------------|---------------------------------------------------------|
| Descrição    | O nome e o caminho do arquivo que contém o componente. |
| Access         | ReadOnly                                                |
| Type           | String                                                  |
| Padrão        | N/D                                                     |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se os eventos são rastreados. Os eventos incluem ações como o desligamento do aplicativo; criação e liberação de objeto; referências de objeto, consistência, ativação e desativação; chamadas de método, retornos e exceções; inicialização da transação, preparação para confirmação e anulação; conexão, alocação e reciclagem de dispensadores de recursos; alocação e reciclagem de threads. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Padrão        | True                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>ExceptionClass



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O CLSID, que pode ser um GUID ou uma cadeia de caracteres do moniker, para ativar um programa alternativo durante o processo de lidar com um programa de componentes enfileirados com falha repetidamente. |
| Access         | ReadWrite                                                                                                                                                                 |
| Type           | String                                                                                                                                                                    |
| Padrão        | ""                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------|
| Descrição    | Habilita eventos a serem acionados em paralelo se o componente for uma classe de evento. |
| Access         | ReadWrite                                                                  |
| Tipo           | Bool                                                                       |
| Padrão        | Falso                                                                      |
| Sistema mínimo | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Habilita a passagem de propriedades de contexto do IIS, como um objeto de sessão de aplicativo ou um objeto de sessão de usuário, para o contexto dessa classe. |
| Access         | ReadWrite                                                                                                                                   |
| Tipo           | Bool                                                                                                                                        |
| Padrão        | Falso                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------|
| Descrição    | Indica se o componente é usado para inicializar um aplicativo de servidor. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Padrão        | Falso                                                                       |
| Sistema mínimo | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descrição    | False se o aplicativo ou componente COM+ estiver desabilitado. Se o aplicativo ou componente COM+ estiver habilitado, IsEnabled será true. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Padrão        | True                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| Entrada | Valor |
|----------------|----------------------------------------------------|
| Descrição    | Indica se o componente é uma classe de evento. |
| Access         | ReadOnly                                           |
| Tipo           | Bool                                               |
| Padrão        | Falso                                              |
| Sistema mínimo | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------|
| Descrição    | Indica se o componente está instalado em um aplicativo. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Padrão        | Falso                                                           |
| Sistema mínimo | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se um aplicativo de servidor é um componente particular. Um componente particular em um aplicativo de servidor pode ser ativado somente de dentro do aplicativo. Por exemplo, se você chamar [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em um componente particular, ele falhará de fora do processo, mas terá êxito no processo. Por outro lado, se você chamar **CoCreateInstance** em um componente público, ele terá sucesso em processo e fora do processo. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se a [ativação JIT](enabling-jit-activation-for-a-component.md) está habilitada para o componente. Essa propriedade é definida como true quando o [suporte à transação](setting-the-transaction-attribute.md) é definido como Required, requer novo ou tem suporte. Quando JustInTimeActivation é definido como true, o [suporte à sincronização](setting-the-synchronization-attribute.md) deve ser definido como Required (o padrão) ou requer New. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Se o serviço de balanceamento de carga do componente estiver instalado e habilitado no servidor, o determinará se o componente participa do balanceamento de carga. |
| Access         | ReadWrite                                                                                                                                        |
| Tipo           | Bool                                                                                                                                             |
| Padrão        | Falso                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Entrada | Valor |
|----------------|-----------------------------------|
| Descrição    | Número máximo de objetos agrupados. |
| Access         | ReadWrite                         |
| Tipo           | Longo (1-1048576)                  |
| Padrão        | 1048576                           |
| Sistema mínimo | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Entrada | Valor |
|----------------|-----------------------------------|
| Descrição    | Número mínimo de objetos agrupados. |
| Access         | ReadWrite                         |
| Tipo           | Longo (0-1048576)                  |
| Padrão        | 0                                 |
| Sistema mínimo | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------|
| Descrição    | CLSID para o filtro de editor usado se o componente for uma classe de evento. |
| Access         | ReadWrite                                                               |
| Type           | String                                                                  |
| Padrão        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientContext



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------|
| Descrição    | Indica que o componente deve ser ativado no contexto do chamador original. Caso contrário, a ativação falhará. |
| Access         | ReadWrite                                                                                                 |
| Tipo           | Bool                                                                                                      |
| Padrão        | Falso                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultContext



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica que o componente deve ser ativado no contexto do chamador padrão. Caso contrário, a ativação falhará. |
| Access         | ReadWrite                                                                                                    |
| Tipo           | Bool                                                                                                         |
| Padrão        | Falso                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------|
| Descrição    | Determina se o [pool de objetos com+](com--object-pooling.md) está habilitado para o componente. |
| Access         | ReadWrite                                                                                       |
| Tipo           | Bool                                                                                            |
| Padrão        | Falso                                                                                           |
| Sistema mínimo | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome amigável usado para identificar o componente. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                |
| Padrão        | N/D                                                                                                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Valor |
|----------------|------------------------------------------------------------------------|
| Descrição    | Identificador do editor de eventos se o componente for uma classe de evento. |
| Access         | ReadWrite                                                              |
| Type           | String                                                                 |
| Padrão        | ""                                                                     |
| Sistema mínimo | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID que identifica o assembly GAC que é executado quando o componente é invocado como um serviço SOAP. |
| Access         | ReadWrite                                                                                        |
| Type           | String                                                                                           |
| Padrão        | NULO                                                                                             |
| Sistema mínimo | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------|
| Descrição    | O nome do tipo gerenciado para um componente que pode ser invocado como um serviço SOAP. |
| Access         | ReadWrite                                                                    |
| Type           | String                                                                       |
| Padrão        | NULO                                                                         |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Sincronização



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina a [sincronização](setting-the-synchronization-attribute.md) de chamadas para o componente.                                                                                                     |
| Access         | ReadWrite                                                                                                                                                                                           |
| Tipo           | Valores longos possíveis: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4) |
| Padrão        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como as instâncias do componente são atribuídas a threads para execução do método. Os valores correspondem aos modelos de Threading COM.                                                                                        |
| Access         | ReadOnly                                                                                                                                                                                                                  |
| Tipo           | Valores longos possíveis: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5) |
| Padrão        | N/D                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transação



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como um componente dá suporte a [Transações](setting-the-transaction-attribute.md). É recomendável que você use as constantes na enumeração e não os valores numéricos. |
| Access         | ReadWrite                                                                                                                                                                              |
| Tipo           | Valores longos possíveis: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)        |
| Padrão        | COMAdminTransactionNone (1)                                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>TxIsolationLevel



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica os níveis de isolamento da transação. Há cinco níveis de isolamento: nenhum, leitura não confirmada, leitura confirmada, leitura repetida e serializada. O nível de isolamento padrão é serializado.                           |
| Access         | ReadWrite                                                                                                                                                                                                                  |
| Tipo           | Valores longos possíveis: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4) |
| Padrão        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Entrada | Valor |
|----------------|---------------------------|
| Descrição    | Identificador de compilação da versão. |
| Access         | ReadOnly                  |
| Type           | String                    |
| Padrão        | ""                        |
| Sistema mínimo | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Entrada | Valor |
|----------------|---------------------|
| Descrição    | Identificador de versão. |
| Access         | ReadOnly            |
| Type           | String              |
| Padrão        | ""                  |
| Sistema mínimo | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Entrada | Valor |
|----------------|-------------------------|
| Descrição    | Subidentificador de versão. |
| Access         | ReadOnly                |
| Type           | String                  |
| Padrão        | ""                      |
| Sistema mínimo | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| Entrada | Valor |
|----------------|-------------------------------|
| Descrição    | Identificador de subcompilação de versão. |
| Access         | ReadOnly                      |
| Type           | String                        |
| Padrão        | ""                            |
| Sistema mínimo | Windows 2000                  |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
