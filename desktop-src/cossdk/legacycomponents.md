---
description: Contém um objeto para cada componente não configurado na coleção de aplicativos. Os componentes não configurados não podem fazer uso de serviços COM+. As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Coleção LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646318"
---
# <a name="legacycomponents-collection"></a>Coleção LegacyComponents

Contém um objeto para cada componente não configurado na coleção de aplicativos. Os componentes não configurados não podem fazer uso de serviços COM+. As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.

Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membros

A coleção **LegacyComponents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Aplicativos**](applications.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Número de bits](#bitness)
-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [Senha](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [Fileparameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------|
| Descrição    | Especifica as contas de usuário que têm o acesso permitido ou negado ao componente. |
| Access         | ReadWrite                                                                       |
| Type           | String                                                                          |
| Padrão        | N/D                                                                             |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Entrada | Valor |
|----------------|------------------------------------------------------------------|
| Descrição    | Especifica se o servidor deve ser executado no computador de armazenamento de dados. |
| Access         | ReadWrite                                                        |
| Tipo           | Valores possíveis de cadeia de caracteres: "N" "Y"                                    |
| Padrão        | "N"                                                              |
| Sistema mínimo | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Entrada | Valor |
|----------------|---------------------|
| Descrição    | A ID do aplicativo. |
| Access         | ReadOnly            |
| Type           | String              |
| Padrão        | N/D                 |
| Sistema mínimo | Windows XP          |



 

### <a name="appname"></a>AppName



| Entrada | Valor |
|----------------|------------------------------|
| Descrição    | O nome do aplicativo. |
| Access         | ReadOnly                     |
| Type           | String                       |
| Padrão        | N/D                          |
| Sistema mínimo | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define o nível de autenticação para chamadas, com valores correspondentes às configurações de autenticação RPC (chamada de procedimento remoto). Quando COMAdminAuthenticationDefault é escolhido, a configuração na propriedade DefaultAuthenticationLevel dentro da coleção [**LocalComputer**](localcomputer.md) é usada. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Padrão        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> É recomendável que você use as constantes na enumeração e não os valores numéricos.

 

### <a name="bitness"></a>Número de bits



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Representa o tipo de bit de bits binário do componente. Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                              |
| Tipo           | Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                         |
| Padrão        | N/D                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Entrada | Valor |
|----------------|------------------------|
| Descrição    | O nome da classe. |
| Access         | ReadOnly               |
| Type           | String                 |
| Padrão        | N/D                    |
| Sistema mínimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID para o componente. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Padrão        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Entrada | Valor |
|----------------|------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para um aplicativo de servidor surragate. |
| Access         | ReadWrite                                                  |
| Type           | String                                                     |
| Padrão        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Entrada | Valor |
|----------------|--------------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para uma DLL de manipulador personalizado em processo de 32 bits. |
| Access         | ReadWrite                                                          |
| Type           | String                                                             |
| Padrão        | N/D                                                                |
| Sistema mínimo | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Valor |
|----------------|------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para uma DLL de servidor em processo de 32 bits. |
| Access         | ReadWrite                                                  |
| Type           | String                                                     |
| Padrão        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Se o aplicativo ou componente COM+ estiver desabilitado, IsEnabled será false. Se o aplicativo ou componente COM+ estiver habilitado, IsEnabled será true. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Padrão        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Descrição    | Especifica as contas de usuário que são permitidas ou com permissão negada para iniciar este componente. |
| Access         | ReadWrite                                                                              |
| Type           | String                                                                                 |
| Padrão        | N/D                                                                                    |
| Sistema mínimo | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para um aplicativo de servidor local de 32 bits. Para ajudar a proteger a segurança do sistema, use cadeias de caracteres entre aspas no caminho para indicar onde o nome do arquivo executável termina e os argumentos começam. Por exemplo, " \\ C: \\ Program Files \\ arquivos da empresa \\Application.exe\\ " param1 param2 ". |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                                                      |
| Padrão        | N/D                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| Entrada | Valor |
|----------------|-----------------------------------------------------|
| Descrição    | Especifica o caminho completo para o aplicativo de serviço. |
| Access         | ReadWrite                                           |
| Type           | String                                              |
| Padrão        | N/D                                                 |
| Sistema mínimo | Windows XP                                          |



 

### <a name="password"></a>Senha



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define a senha usada pelo processo do servidor para fazer logon na identidade RunAs especificada. A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade forem obtidas fora de sincronia, o componente não poderá ser iniciado até que eles sejam redefinidos por um administrador. |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Padrão        | NULO                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome que identifica o componente. Essa propriedade é retornada quando o método de propriedade Name é chamado em um objeto desta coleção. |
| Access         | ReadOnly                                                                                                                             |
| Type           | String                                                                                                                               |
| Padrão        | N/D                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Entrada | Valor |
|----------------|---------------------------------------|
| Descrição    | Especifica o computador do servidor remoto. |
| Access         | ReadWrite                             |
| Type           | String                                |
| Padrão        | N/D                                   |
| Sistema mínimo | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Especifica o usuário sob a identidade cujo componente será executado. A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade forem obtidas fora de sincronia, o componente não poderá ser iniciado até que eles sejam redefinidos por um administrador. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Padrão        | N/D                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>Fileparameter



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------|
| Descrição    | Especifica os parâmetros passados para o aplicativo quando chamado como um aplicativo de serviço. |
| Access         | ReadWrite                                                                                 |
| Type           | String                                                                                    |
| Padrão        | N/D                                                                                       |
| Sistema mínimo | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o nível de confiança da política de restrição de software (SRP) do componente. O nível de confiança do SRP refere-se ao nível de confiança que você está disposto a dar a um componente. Um nível de confiança de SRP irrestrito corresponde ao valor de \_ enumeração de FULLYTRUSTED de nível mais seguro \_ , enquanto um nível de confiança SRP não permitido corresponde ao valor de enumeração mais seguro de \_ levelid não \_ permitido. A enumeração para os níveis de confiança é definida em Winsafer. h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Valores longos possíveis: nível mais seguro \_ de redistribuirid não \_ permitido (0x0) \_ FULLYTRUSTED de nível mais seguro \_ (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Padrão        | nível mais seguro de \_ \_ FULLYTRUSTED                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Um componente ao qual você está disposto a confiar com acesso irrestrito deve ter a segurança mais rigorosa anexada a ele. Os aplicativos que são irrestritos podem carregar apenas componentes irrestritos, enquanto os aplicativos não permitidos não poderão ser executados e, portanto, não poderão carregar nenhum componente.

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como as instâncias do componente são atribuídas a threads para execução do método. Os valores correspondem aos modelos de Threading COM.                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| Tipo           | Valores longos possíveis: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) |
| Padrão        | N/D                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
