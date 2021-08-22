---
description: Contém um único objeto que corresponde ao computador cujo catálogo você está acessando. Esse objeto contém informações de configurações no nível do computador.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Coleção de LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: b832da702942e8f84baee4303b7fa74a7fd74d683d62534cca619e8c7270e88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813460"
---
# <a name="localcomputer-collection"></a>Coleção de LocalComputer

Contém um único objeto que corresponde ao computador cujo catálogo você está acessando. Esse objeto contém informações de configurações no nível do computador. se você chamar o método [**Conexão**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) em um objeto criado a partir da classe [**COMAdminCatalog**](comadmincatalog.md) , o objeto na coleção **LocalComputer** conterá informações sobre o computador remoto cujo catálogo você está acessando.

Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membros

A coleção **LocalComputer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="related-collections"></a>Coleções relacionadas

Você pode navegar desta coleção para qualquer uma das seguintes coleções:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Você pode navegar até essa coleção das seguintes coleções:

-   [**Básica**](root.md)

## <a name="properties"></a>Propriedades

As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Descrição](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [Isroteador](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [Nome](#name)
-   [Operacional](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [Portas](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| Entrada | Valor |
|----------------|------------------------------------------------------------|
| Descrição    | Nome do servidor remoto usado por proxies de aplicativo por padrão. |
| Access         | ReadWrite                                                  |
| Type           | String                                                     |
| Padrão        | ""                                                         |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------|
| Descrição    | Indica se os serviços da Internet COM estão habilitados. |
| Access         | ReadWrite                                           |
| Tipo           | Bool                                                |
| Padrão        | Falso                                               |
| Sistema mínimo | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Entrada | Valor |
|----------------|---------------------------------------------|
| Descrição    | Defina como true para habilitar o DCOM no computador. |
| Access         | ReadWrite                                   |
| Tipo           | Bool                                        |
| Padrão        | Verdadeiro                                        |
| Sistema mínimo | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Nível de autenticação usado por aplicativos que têm a autenticação definida como padrão. Os valores correspondem às configurações de autenticação RPC (chamada de procedimento remoto).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| Tipo           | Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) |
| Padrão        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault é mapeado para COMAdminAuthenticationConnect quando o COM chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). É recomendável que você use as constantes na enumeração e não os valores numéricos.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Nível de representação para permitir se um não estiver definido.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valores long possible:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Padrão        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> É recomendável que você use as constantes na enumeração e não os valores numéricos.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------|
| Descrição    | Determina se o tipo padrão de porta fornecido deve ser Internet (True) ou intranet (False). |
| Access         | ReadWrite                                                                                           |
| Tipo           | Bool                                                                                                |
| Padrão        | Falso                                                                                               |
| Sistema mínimo | Windows 2000                                                                                        |



 

### <a name="description"></a>Descrição



| Entrada | Valor |
|----------------|--------------------------------|
| Descrição    | Uma descrição do computador. |
| Access         | ReadWrite                      |
| Type           | String                         |
| Padrão        | ""                             |
| Sistema mínimo | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Descrição    | Indica se o usuário dos mapeamentos de partição é verificado no armazenamento de domínio. |
| Access         | ReadWrite                                                                              |
| Tipo           | Bool                                                                                   |
| Padrão        | Verdadeiro                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina se as portas listadas na propriedade Portas devem ser usadas para Internet (True) ou para intranet (False). |
| Access         | ReadWrite                                                                                                             |
| Tipo           | Bool                                                                                                                  |
| Padrão        | Falso                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Definido como True se o computador for um roteador para o serviço CLB (balanceamento de carga de componente). Essa propriedade poderá ser definida como True somente se o serviço de balanceamento de carga do componente estiver instalado no computador no momento; caso contrário, ele erros com COMADMIN \_ E \_ REQUER PLATAFORMA \_ \_ DIFERENTE. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                |
| Padrão        | Falso                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                        |



 

Se essa propriedade for definida como True, o servidor CLB será configurado e iniciará na inicialização. O servidor será adicionado à coleção ApplicationCluster se ele ainda não estiver presente.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Entrada | Valor |
|----------------|-------------------------------------|
| Descrição    | O CLSID do objeto a ser balanceado. |
| Access         | ReadWrite                           |
| Type           | String                              |
| Padrão        | NULO                                |
| Sistema mínimo | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Descrição    | Indica se o usuário dos mapeamentos de partição é verificado no armazenamento local. |
| Access         | ReadWrite                                                                             |
| Tipo           | Bool                                                                                  |
| Padrão        | Verdadeiro                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nome



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O nome do computador. Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Padrão        | "Meu Computador"                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | O sistema operacional instalado no computador local.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Valores longos possíveis: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16) |
| Padrão        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Indica se as partições COM+ podem ser usadas no computador local. Se essa propriedade for falsa, qualquer tentativa de usar partições COM+ resultará em um erro. |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                    |
| Padrão        | Falso                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Portas



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Uma cadeia de caracteres que descreve as portas que são usadas para a Internet ou intranet, dependendo da propriedade InternetPortsListed; por exemplo, "500-599:600-800". |
| Access         | ReadWrite                                                                                                                                               |
| Type           | String                                                                                                                                                  |
| Padrão        | ""                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Entrada | Valor |
|----------------|-------------------------------------|
| Descrição    | Habilita o uso de dispensadores de recursos. |
| Access         | ReadWrite                           |
| Tipo           | Bool                                |
| Padrão        | Verdadeiro                                |
| Sistema mínimo | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Controla se o proxy RPC do IIS está habilitado. O proxy RPC do IIS é usado em conjunto com o IIS para encaminhar chamadas para o mecanismo RPC do IIS e é uma das partes principais dos serviços de Internet COM, que é habilitada definindo CISEnabled como true. Para obter mais informações sobre o RPCProxyEnabled, consulte [segurança http RPC](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Padrão        | Falso                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Impõe em computadores DCOM que as chamadas entre processos para os métodos [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) são protegidas. |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | Bool                                                                                                                                                                      |
| Padrão        | Falso                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Entrada | Valor |
|----------------|---------------------------------------------------------|
| Descrição    | Definido como True se o controle de segurança estiver habilitado em objetos. |
| Access         | ReadWrite                                               |
| Tipo           | Bool                                                    |
| Padrão        | Verdadeiro                                                    |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como a SRP (política de restrição de software) lida com conexões de ativar como ativador. Se definido como True, o nível de confiança SRP configurado para o objeto de servidor será comparado com o nível de confiança SRP do objeto cliente e o nível de confiança mais alto (mais rigoroso) será usado para executar o objeto de servidor. Se definido como False, o objeto de servidor será executado com o nível de confiança SRP do objeto cliente, independentemente do nível de confiança SRP com o qual o servidor está configurado. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Padrão        | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Determina como a SRP (política de restrição de software) lida com tentativas de conexões com processos existentes. Se definido como False, as tentativas de se conectar a objetos em execução não serão verificadas em busca de níveis de confiança SRP apropriados. Se definido como True, o objeto em execução deverá ter um nível de confiança SRP igual ou superior (mais rigoroso) do que o objeto cliente. Por exemplo, um objeto cliente com um nível de confiança SRP irrestrito não pode se conectar a um objeto em execução com um nível de confiança SRP não permitido. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Padrão        | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição    | Deve ser definido como um valor suficiente em segundos se você estiver fazendo várias operações dentro de uma transação. O período de tempo limite padrão é de 60 segundos e o período de tempo limite máximo é de 3600 segundos (1 hora). Definir essa propriedade como 0 desabilita os tempos de tempo de transação. Essa propriedade pode ser substituído por componentes individuais usando a propriedade ComponentTransactionTimeout da coleção [**Components.**](components.md) |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Padrão        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Exemplo

O exemplo de Visual Basic Microsoft a seguir demonstra como se conectar a um computador remoto e obter sua propriedade SecurityTrackingEnabled usando a coleção **LocalComputer** do computador remoto. Para usar este exemplo, adicione a Biblioteca de Tipos de Administrador COM+ como uma referência ao seu Visual Basic projeto.


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



Para usar a função , forneça um valor de cadeia de caracteres para o nome do computador remoto. O código Visual Basic a seguir mostra como se conectar ao computador chamado "RemoteComputerName".


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleções de administração COM+](com--administration-collections.md)
</dt> </dl>

 

 
