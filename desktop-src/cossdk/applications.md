---
description: Contém um objeto para cada aplicativo COM+ instalado no computador local. As propriedades expostas por esses objetos contêm todas as configurações feitas no nível do aplicativo.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Coleção de aplicativos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 085983bf390998910f36a87ac41aaa15e783b55d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884822"
---
# <a name="applications-collection"></a>Coleção de aplicativos

Contém um objeto para cada aplicativo COM+ instalado no computador local. As propriedades expostas por esses objetos contêm todas as configurações feitas no nível do aplicativo.

Defina as propriedades dos componentes em um aplicativo usando a coleção de [**componentes**](components.md) relacionados. Você atribui funções a um aplicativo usando a coleção de [**funções**](roles.md) relacionadas.

Para instalar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) . Para instalar um aplicativo de um arquivo ou desligar ou exportar um aplicativo, use também métodos no objeto **COMAdminCatalog** . Caso contrário, para criar um novo aplicativo, você pode adicionar um objeto à coleção de **aplicativos** .

Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção de **aplicativos** é herdada da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Componentes**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Funções**](roles.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Partições**](partitions.md)
-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Ativação](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [Autenticação](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Mutável](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Pode ser excluído](#deleteable)
-   [Descrição](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [ID](#applications-collection)
-   [Identidade](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Nome](#applicationproxyservername)
-   [Senha](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replicáveis](#replicable)
-   [RunForever](#runforever)
-   [ServiceName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se o aplicativo pode usar 3 GB de memória em seu processo. Se isso não estiver habilitado, o aplicativo poderá usar apenas 2 GB de memória. |
| Access         | ReadWrite                                                                                                                                     |
| Type           | Bool                                                                                                                                          |
| Padrão        | Falso                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se as verificações de acesso são executadas apenas no nível do processo ou no nível do processo e do componente. É recomendável que você use as constantes na enumeração e não os valores numéricos. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| Type           | Valores long possible: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Padrão        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Ativação



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | A ativação local indica que os objetos dentro do aplicativo são executados em um processo de servidor local dedicado (aplicativo de servidor). A ativação em processo indica que os objetos são executados no processo do criador (aplicativo de biblioteca). |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| Type           | Valores long possible:COMAdminActivationInproc (0)COMAdminActivationLocal (1)                                                                                                                                                        |
| Padrão        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------|
| Descrição    | Indica se as verificações de acesso são executadas para o aplicativo quando os clientes fazem chamadas nele. |
| Access         | ReadWrite                                                                                          |
| Type           | Bool                                                                                               |
| Padrão        | True                                                                                               |
| Sistema mínimo | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>Applicationdirectory



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O caminho completo para o aplicativo. Essas informações são necessárias quando você configura assemblies lado a lado (SxS). Assemblies SxS (lado a lado) permitem que aplicativos ASP especifiquem qual versão de uma DLL do sistema com suporte para SxS usar, como MSVCRT, MSXML, COMCTL, GDIPLUS e assim por diante. Por exemplo, se o aplicativo ASP se basear na versão 2.0 do MSVCRT, você poderá garantir que seu aplicativo ainda use o MSVCRT versão 2.0 mesmo depois que os service packs são aplicados ao servidor. Qualquer nova versão do MSVCRT ainda está instalada no computador, mas a versão 2.0 permanece e é usada pelo seu aplicativo. As DLLs com suporte para SxS são armazenadas em %WINDIR% \\ WinSxS. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Padrão        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Apenas uma versão de uma DLL do sistema pode ser usada em qualquer pool de aplicativos, mesmo que esse recurso seja configurável no nível do aplicativo. Por exemplo, se o aplicativo App1 usar MSVCRT, a versão 2.5 e o aplicativo App2 usarem MSVCRT, versão 2.4, o App1 e o App2 não deverão estar no mesmo pool de aplicativos. Se for, o aplicativo carregado primeiro terá sua versão do MSVCRT carregada e o outro aplicativo será forçado a usá-lo até que os aplicativos sejam descarregados.

 

Para obter mais informações, consulte "Assemblies lado a lado" em Alterações nos serviços [COM+ no IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).

### <a name="applicationproxy"></a>ApplicationProxy



| Entrada | Valor |
|----------------|------------------------------------------------------------|
| Descrição    | Indica se o aplicativo é um proxy de aplicativo. |
| Access         | ReadOnly                                                   |
| Type           | Bool                                                       |
| Padrão        | Falso                                                      |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um nome de servidor remoto usado ao exportar o proxy de aplicativo. É para esse nome de servidor que o proxy de aplicativo aponta quando ele é instalado em um computador cliente. |
| Access         | ReadWrite                                                                                                                                                              |
| Type           | String                                                                                                                                                                 |
| Padrão        | ""                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Entrada | Valor |
|----------------|---------------------------------------------------|
| Descrição    | Um GUID que representa a ID da partição do aplicativo. |
| Access         | ReadOnly                                          |
| Type           | String                                            |
| Padrão        | &lt;Gerado&gt;                                 |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="authentication"></a>Autenticação



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define o nível de autenticação para chamadas, com valores correspondentes às configurações de autenticação de RPC (Chamada de Procedimento Remoto). Quando COMAdminAuthenticationDefault é escolhido, a configuração na propriedade DefaultAuthenticationLevel na coleção [**LocalComputer**](localcomputer.md) é usada. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Type           | Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Padrão        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Para aplicativos de biblioteca (em processo), as únicas configurações válidas aqui são COMAdminAuthenticationDefault e COMAdminAuthenticationNone. É recomendável que você use as constantes na enumeração e não os valores numéricos.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina qual identidade é apresentada quando as chamadas são representadas.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| Type           | Valores longos possíveis: COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Padrão        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Mutável



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se as alterações nas configurações do aplicativo ou de seus componentes são permitidas, seja por meio de programação ou por meio da ferramenta de administração de serviços de componentes. |
| Access         | ReadWrite                                                                                                                                                                     |
| Type           | Bool                                                                                                                                                                          |
| Padrão        | True                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma cadeia de caracteres de linha de comando para uso na depuração. O aplicativo pode ser iniciado em um depurador com a linha de comando especificada. |
| Access         | ReadWrite                                                                                                                  |
| Type           | String                                                                                                                     |
| Padrão        | ""                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------|
| Descrição    | Especifica o número máximo de aplicativos em pool que podem ser executados simultaneamente. |
| Access         | ReadWrite                                                                        |
| Type           | Longo (1-1048576)                                                                 |
| Padrão        | 1                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Entrada | Valor |
|----------------|---------------------------------------------------------------|
| Descrição    | Cadeia de caracteres informativa para descrever quem criou o aplicativo. |
| Access         | ReadWrite                                                     |
| Type           | String                                                        |
| Padrão        | ""                                                            |
| Sistema mínimo | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------|
| Descrição    | Determina se o Gerenciador de recursos de compensação está habilitado. |
| Access         | ReadWrite                                                        |
| Type           | Bool                                                             |
| Padrão        | Falso                                                            |
| Sistema mínimo | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Descrição    | Nome e caminho do arquivo para manter o log do Gerenciador de recursos de compensação (CRM). |
| Access         | ReadWrite                                                                              |
| Type           | String                                                                                 |
| Padrão        | ""                                                                                     |
| Sistema mínimo | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Pode ser excluído



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define se o aplicativo pode ser excluído, seja por meio de programação ou por meio da ferramenta de administração de serviços de componentes. |
| Access         | ReadWrite                                                                                                                   |
| Type           | Bool                                                                                                                        |
| Padrão        | True                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                |



 

### <a name="description"></a>Description



| Entrada | Valor |
|----------------|----------------------------|
| Descrição    | Descreve o aplicativo. |
| Access         | ReadWrite                  |
| Type           | String                     |
| Padrão        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------|
| Descrição    | Habilita o despejo do estado de um aplicativo COM+ no momento da falha em um diretório designado. |
| Access         | ReadWrite                                                                                             |
| Type           | Bool                                                                                                  |
| Padrão        | Falso                                                                                                 |
| Sistema mínimo | Windows XP                                                                                            |



 

> [!Note]  
> a partir do Windows Server 2003, somente os administradores têm privilégios de acesso de leitura aos arquivos de despejo COM+.

 

### <a name="dumponexception"></a>DumpOnException



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Habilita o despejo do estado de um aplicativo COM+ quando o aplicativo causa uma exceção sem tratamento e é encerrado pelo tempo de execução do COM+. |
| Access         | ReadWrite                                                                                                                                     |
| Type           | Bool                                                                                                                                          |
| Padrão        | Falso                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------|
| Descrição    | Habilita o despejo do estado de um aplicativo COM+ quando o aplicativo falha. |
| Access         | ReadWrite                                                                       |
| Type           | Bool                                                                            |
| Padrão        | Falso                                                                           |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Entrada | Valor |
|----------------|--------------------------------------------------------------|
| Descrição    | O caminho do diretório no qual os arquivos de despejo são salvos. |
| Access         | ReadWrite                                                    |
| Type           | String                                                       |
| Padrão        | "% SystemRoot% \\ System32 \\ com \\ DMP"                           |
| Sistema mínimo | Windows XP                                                   |



 

> [!Note]  
> a partir do Windows Server 2003, somente os administradores têm privilégios de acesso de leitura aos arquivos de despejo COM+.

 

### <a name="eventsenabled"></a>EventsEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------|
| Descrição    | Indica se os eventos estão habilitados para o aplicativo. |
| Access         | ReadWrite                                                 |
| Type           | Bool                                                      |
| Padrão        | True                                                      |
| Sistema mínimo | Windows 2000                                              |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Um GUID que representa o aplicativo. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                            |
| Type           | String                                                                                                                                                               |
| Padrão        | &lt;Gerado&gt;                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identidade



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define a identidade do processo do servidor para o aplicativo. Especifique uma conta de usuário válida ou "Usuário Interativo" para que o aplicativo assuma a identidade do usuário conectado atual. Você também pode especificar as cadeias de caracteres "nt authority \\ localservice", "nt authority \\ networkservice" e "nt authority \\ system". A senha padrão para essas três contas é "" (cadeia de caracteres vazia). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Padrão        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

A propriedade Identity não está habilitada para aplicativos de biblioteca, que são executados no processo do cliente.

A propriedade Password deve ser definida ao mesmo tempo que Identity, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade ficam fora de sincronia, o aplicativo não pode ser lançado até que eles sejam redefinidos por um administrador.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define o nível de representação usado para chamadas feitas a outros aplicativos.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| Type           | Valores long possible:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Padrão        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Se o aplicativo OU componente COM+ estiver desabilitado, IsEnabled será False. Se o aplicativo OU componente COM+ estiver habilitado, IsEnabled será True. |
| Access         | ReadWrite                                                                                                                                 |
| Type           | Bool                                                                                                                                      |
| Padrão        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Entrada | Valor |
|----------------|--------------------------------------|
| Descrição    | Identifica aplicativos do sistema COM+. |
| Access         | ReadOnly                             |
| Type           | Bool                                 |
| Padrão        | Falso                                |
| Sistema mínimo | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------|
| Descrição    | Indica o número máximo de arquivos a serem gerados antes da substituição. |
| Access         | ReadWrite                                                                        |
| Type           | Long (1 a 200)                                                                     |
| Padrão        | 5                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do aplicativo. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o [**método de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) propriedade Name é chamado em um objeto desta coleção. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                               |
| Padrão        | "Novo aplicativo"                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Nomes exclusivos devem ser escolhidos para aplicativos. Se vários aplicativos são criados com o mesmo nome, ele pode interferir em referenciar os aplicativos por nome, resultando em comportamento imprevisível.

 

### <a name="password"></a>Senha



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------|
| Descrição    | Define a senha usada pelo processo do servidor para fazer logoff na identidade. |
| Access         | WriteOnly                                                                  |
| Type           | String                                                                     |
| Padrão        | ""                                                                         |
| Sistema mínimo | Windows 2000                                                               |



 

A senha deve ser definida ao mesmo tempo que a identidade, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), pois a senha e a identidade são validadas antes de serem salvas. Se a senha e a identidade forem obtidas fora de sincronia, o aplicativo não poderá ser iniciado até que ele seja redefinido por um administrador.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica em quais circunstâncias as solicitações enfileiradas para um aplicativo são autenticadas.                                                 |
| Access         | ReadWrite                                                                                                                               |
| Type           | Valores longos possíveis: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2) |
| Padrão        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Sistema mínimo | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o número máximo de threads de ouvinte simultâneos. O intervalo válido para essa propriedade é de 0 a 1000. Para um aplicativo recém-criado, a configuração é derivada do algoritmo usado atualmente para determinar o número padrão de threads de ouvinte: 16 vezes o número de CPUs no servidor. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Type           | Longo (0-1000)                                                                                                                                                                                                                                                                                             |
| Padrão        | 0                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Essa propriedade também está disponível com a funcionalidade de leitura/gravação na guia **enfileiramento** da ferramenta administrativa serviços de componentes.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se o ouvinte de componentes na fila está habilitado para o aplicativo. Se habilitada, o ouvinte será iniciado quando o aplicativo for iniciado. Essa propriedade entrará em vigor somente se QueuingEnabled estiver definido como true. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Type           | Bool                                                                                                                                                                                                                 |
| Padrão        | Falso                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Descrição    | Indica se o serviço de componentes em fila COM+ está habilitado para o aplicativo. |
| Access         | ReadWrite                                                                            |
| Type           | Bool                                                                                 |
| Padrão        | Falso                                                                                |
| Sistema mínimo | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o número máximo de ativações de objetos configurados no aplicativo a serem aceitos antes da reciclagem do processo. O número padrão de ativações é 0. |
| Access         | ReadWrite                                                                                                                                                            |
| Type           | Longo (0-1048576)                                                                                                                                                     |
| Padrão        | 0                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o número máximo de chamadas para permitir que os objetos configurados no aplicativo sejam aceitos antes da reciclagem do processo. O número padrão de chamadas é 0. |
| Access         | ReadWrite                                                                                                                                                      |
| Type           | Longo (0-1048576)                                                                                                                                               |
| Padrão        | 0                                                                                                                                                              |
| Sistema mínimo | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica a quantidade de tempo (em minutos) para permitir que um processo reciclado seja executado antes de desligá-lo. A contagem regressiva começa imediatamente após o processo ser reciclado. O tempo limite máximo de expiração é de 1440 minutos (24 horas) e o padrão é 15 minutos. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| Type           | Longo (1-1440)                                                                                                                                                                                                                                                    |
| Padrão        | 15                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o número máximo de minutos para permitir que um processo seja executado antes de reciclá-lo. O limite máximo de tempo de vida é de 30240 minutos (21 dias) e o padrão é 0 minutos. |
| Access         | ReadWrite                                                                                                                                                                   |
| Type           | Longo (0-30240)                                                                                                                                                              |
| Padrão        | 0                                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica a quantidade máxima de uso de memória (em quilobytes) que permitia um processo antes de ser reciclado. Se o uso de memória do processo exceder o número especificado por um período de mais de um minuto, o processo será reciclado. A quantidade padrão de uso de memória é 0 KB. |
| Access         | ReadWrite                                                                                                                                                                                                                                                              |
| Type           | Longo (0-1048576)                                                                                                                                                                                                                                                       |
| Padrão        | 0                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replicáveis



| Entrada | Valor |
|----------------|------------------------------------------------------|
| Descrição    | Indica se o aplicativo pode ser replicado. |
| Access         | ReadWrite                                            |
| Type           | Bool                                                 |
| Padrão        | True                                                 |
| Sistema mínimo | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Permite que um processo do servidor continue se um aplicativo estiver ocioso. Se definido como true, o processo do servidor não é desligado quando deixado ocioso. Se definido como false, o processo será desligado de acordo com o valor definido pela propriedade ShutdownAfter. RunForever não está habilitado para aplicativos de biblioteca (em processo). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Type           | Bool                                                                                                                                                                                                                                                                                                     |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do serviço correspondente ao aplicativo configurado para ser executado como um aplicativo de serviço. Se esse valor for **nulo**, o aplicativo não será configurado para ser executado como um serviço. Caso contrário, as informações de configuração para o serviço podem ser encontradas usando o nome do serviço. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                                                                                                           |
| Padrão        | ""                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Define o atraso antes de desligar um processo do servidor depois que ele se torna ocioso. Intervalos de latência de desligamento de 0 a 1440 minutos (24 horas). Se RunForever for definido como true, essa propriedade será ignorada. ShutdownAfter não está habilitado para aplicativos de biblioteca (em processo). |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| Type           | Longo (0-1440)                                                                                                                                                                                                                                                      |
| Padrão        | 3                                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Descrição    | Indica se este aplicativo é exposto para consumo por meio do protocolo SOAP. |
| Access         | ReadWrite                                                                            |
| Type           | Bool                                                                                 |
| Padrão        | Falso                                                                                |
| Sistema mínimo | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------|
| Descrição    | O ponto de extremidade de URL no qual esse aplicativo é exposto por meio do protocolo SOAP. |
| Access         | ReadWrite                                                                    |
| Type           | String                                                                       |
| Padrão        | ""                                                                           |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------|
| Descrição    | O endereço de email no qual esse aplicativo é exposto por meio do protocolo SOAP. |
| Access         | ReadWrite                                                                     |
| Type           | String                                                                        |
| Padrão        | ""                                                                            |
| Sistema mínimo | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descrição    | O diretório raiz virtual do IIS no qual residem os scripts de acesso que expõem o aplicativo por meio do protocolo SOAP. |
| Access         | ReadWrite                                                                                                            |
| Type           | String                                                                                                               |
| Padrão        | ""                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina a SRP (política de restrição de software) para o aplicativo. Se definido como True, a propriedade SRPTrustLevel para o aplicativo será usada. Se definido como False, as políticas de restrição de software das configurações de segurança local serão usadas. As configurações de segurança local são controladas por meio do snap-in política de segurança local do Console de Gerenciamento Microsoft. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica o nível de confiança SRP (política de restrição de software) do aplicativo. Essa propriedade será usada somente se a propriedade SRPEnabled estiver definida como True. O nível de confiança SRP refere-se ao nível de confiança que você está disposto a dar a um aplicativo. Um nível de confiança SRP irrestrito corresponde ao valor de enum SAFER LEVELID FULLYTRUSTED, enquanto um nível de confiança SRP não permitido corresponde ao valor de \_ \_ enum SAFER \_ LEVELID \_ DISALLOWED. A enumeração para os níveis de confiança é definida em Winsafer.h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Type           | Valores long possible:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Padrão        | SAFER \_ LEVELID \_ FULLYTRUSTED (0X40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Um aplicativo em que você está disposto a confiar com acesso irrestrito deve ter a segurança mais rigorosa anexada a ele. Aplicativos irrestritos podem carregar apenas componentes irrestritos, enquanto aplicativos não permitidos não terão permissão para serem executados e, portanto, não podem carregar nenhum componente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
