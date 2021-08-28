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
ms.openlocfilehash: 0815c9124020ff08e7033f7d1f18f8d9c5b6736763d401a3564bbdd8c6ffdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120396"
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
| Descrição    | Representa o tipo de bit de bits binário do componente. em sistemas que usam Windows de 64 bits, essa propriedade distingue entre componentes de 64 bits e componentes de 32 bits. |
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
| Padrão        | Verdadeiro                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Descrição    | Especifica as contas de usuário que têm permissão permitida ou negada para iniciar esse componente. |
| Access         | ReadWrite                                                                              |
| Type           | String                                                                                 |
| Padrão        | N/D                                                                                    |
| Sistema mínimo | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Especifica o caminho completo para um aplicativo de servidor local de 32 bits. Para ajudar a proteger a segurança do sistema, use cadeias de caracteres entre aspas no caminho para indicar onde o nome de arquivo executável termina e os argumentos começam. Por exemplo, " \\ "C: Arquivos de Empresa de Arquivos \\ de ProgramasApplication.exe" \\ \\ \\ param1 param2". |
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
| Descrição    | Define a senha usada pelo processo do servidor para fazer logoff na identidade RunAs especificada. A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)porque a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade ficam fora de sincronia, o componente não pode ser lançado até que eles sejam redefinidos por um administrador. |
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



 

### <a name="remoteserver"></a>Remoteserver



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
| Descrição    | Especifica o usuário em cuja identidade o componente será executado. A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)porque a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade ficam fora de sincronia, o componente não pode ser lançado até que eles sejam redefinidos por um administrador. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Padrão        | N/D                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------|
| Descrição    | Especifica os parâmetros passados para o aplicativo quando invocados como um aplicativo de serviço. |
| Access         | ReadWrite                                                                                 |
| Type           | String                                                                                    |
| Padrão        | N/D                                                                                       |
| Sistema mínimo | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o nível de confiança SRP (política de restrição de software) do componente. O nível de confiança SRP refere-se ao nível de confiança que você está disposto a dar a um componente. Um nível de confiança SRP irrestrito corresponde ao valor de enum SAFER LEVELID FULLYTRUSTED, enquanto um nível de confiança SRP não permitido corresponde ao valor de \_ \_ enum SAFER \_ LEVELID \_ DISALLOWED. A enumeração para os níveis de confiança é definida em Winsafer.h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Valores long possible:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Padrão        | LEVELID \_ MAIS \_ SEGURO TOTALMENTETRUSTED                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Um componente em que você está disposto a confiar com o acesso irrestrito deve ter a segurança mais rigorosa anexada a ele. Aplicativos irrestritos podem carregar apenas componentes irrestritos, enquanto aplicativos não permitidos não terão permissão para serem executados e, portanto, não podem carregar nenhum componente.

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como as instâncias do componente são atribuídas a threads para execução de método. Os valores correspondem aos modelos de threading COM.                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| Tipo           | Valores long possible:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4) |
| Padrão        | N/D                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
