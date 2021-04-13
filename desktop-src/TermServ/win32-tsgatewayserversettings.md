---
title: Classe Win32_TSGatewayServerSettings
description: Fornece métodos e propriedades para exibir e definir configurações de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayServerSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455845"
---
# <a name="win32_tsgatewayserversettings-class"></a>\_Classe Win32 TSGatewayServerSettings

Fornece métodos e propriedades para exibir e definir configurações de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). Um administrador pode usar essa classe para configurar um conjunto de protocolos, o conjunto de eventos que será gravado no log de eventos e o número máximo de conexões por meio do gateway de área de trabalho remota.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSGatewayServerSettings** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayServerSettings** tem esses métodos.



| Método                                                                                                                                             | Descrição                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](configure-win32-tsgatewayserversettings.md)                                                                                       | Define as configurações de IIS e RPC exigidas pelo serviço de gateway de área de trabalho remota.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Habilita ou desabilita a propriedade **CentralCAPEnabled** , que controla se os servidores de política de autorização de conexão central Área de Trabalho Remota (RD CAP) são usados para controlar as políticas de autorização de conexão para este servidor.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Habilita ou desabilita o registro em log do tipo de evento especificado.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Define a propriedade **OnlyConsentCapableClients** .<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                                      |
| [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Este método não tem suporte a partir do Windows Server 2016.<br/> **Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 e Windows server 2008:** Habilita ou desabilita solicitações para uma SoH (declaração de integridade).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Habilita ou desabilita o transporte especificado.<br/> **Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Enumera todos os plug-ins de autenticação registrados.<br/> **Windows Server 2008:** Este método não está disponível.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Enumera todos os plug-ins de autorização registrados.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Obtém o endereço IP de escuta e o número da porta para o transporte especificado.<br/> **Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Retorna o nome do evento de log para o índice de evento de log especificado.<br/>                                                                                                                                                                                         |
| [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Retorna o nome do protocolo para o índice de protocolo especificado.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Indica se o tipo de log de eventos especificado está habilitado.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Determina se o transporte especificado está habilitado.<br/> **Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Indica se o certificado especificado está instalado.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Recicla os pools de aplicativos RPC no IIS.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Atualiza o certificado que é usado pelo servidor de gateway de área de trabalho remota.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Define o plug-in de autenticação atual para o servidor de gateway de área de trabalho remota.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Define o plug-in de autenticação atual para o servidor de gateway de área de trabalho remota e recicla os pools de aplicativos RPC no IIS.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Define o plug-in de autorização atual para o servidor de gateway de área de trabalho remota.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Define o hash de certificado para associação HTTPS na porta 443 no IIS.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Define as listas de controle de acesso (ACLs) do certificado para este servidor.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Define os plug-ins de autenticação e autorização atuais para o servidor de gateway de área de trabalho remota e recicla os pools de aplicativos RPC no IIS.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Define a propriedade **EnforceChannelBinding** .<br/> **Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Define o endereço IP de escuta e o número da porta para o transporte especificado.<br/> **Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Define o número máximo de conexões permitidas por meio do gateway RD. Esse método altera as propriedades **MaxConnections** e **UnlimitedConnections** .<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Define o tipo de ponte SSL a ser usado pelo servidor de gateway de área de trabalho remota.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Remove a mensagem administrativa para o servidor de gateway.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Remove a mensagem administrativa para o servidor de gateway.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Atualiza a mensagem administrativa para o servidor de gateway.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Atualiza a mensagem de consentimento para o servidor de gateway.<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                                                                                   |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayServerSettings** tem essas propriedades.

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora de término da mensagem administrativa.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora de início da mensagem administrativa.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O texto da mensagem administrativa.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O CLSID do plug-in de autenticação atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A descrição do plug-in de autenticação atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do plug-in de autenticação atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O CLSID do plug-in de autorização atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A descrição do plug-in de autorização atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do plug-in de autorização atual.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se os servidores de RD CAP central são usados para controlar esse servidor. Essa propriedade pode ser alterada chamando o método [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o hash de certificado para associação HTTPS na porta 443 no IIS.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O texto da mensagem de consentimento.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a associação de canal é imposta para o transporte HTTP. Esse valor de propriedade pode ser alterado usando o método [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .

**Windows server 2008 R2 e Windows server 2008:** Essa propriedade não está disponível antes do Windows Server 2012.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se as configurações de IIS e RPC exigidas pelo serviço de gateway de área de trabalho remota estão configuradas.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Retorna o número máximo de conexões permitidas por meio do gateway de área de trabalho remota. Essa propriedade pode ser definida usando o método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número máximo de conexões que a SKU (unidade de manutenção de estoque) permite.

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Retorna o número máximo de eventos de log.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de protocolos com suporte pelo Gateway RD.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se somente clientes capazes de autorizar mensagens de consentimento têm permissão para se conectar ao gateway de área de trabalho remota.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

<dt>

diferente
</dt> <dd>

Somente clientes compatíveis com mensagens de consentimento podem se conectar.

</dd> <dt>

zero
</dt> <dd>

Clientes que não são compatíveis com mensagens de consentimento também podem se conectar.

</dd> </dl>

</dd> <dt>

**RequestSOH**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não há suporte para essa propriedade a partir do Windows Server 2016.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: * *

Especifica se o servidor deve solicitar uma SoH (declaração de integridade) do cliente. Essa propriedade pode ser alterada usando o método [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da SKU.

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de ponte SSL a ser usado pelo servidor de gateway de área de trabalho remota. Isso pode ser um dos valores a seguir.

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Sem ponte SSL.

</dd> <dt>

1
</dt> <dd>

Conexão HTTPS com HTTP.

</dd> <dt>

2
</dt> <dd>

Conexão HTTPS com HTTPS.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se um número ilimitado de conexões é permitido por meio do gateway de área de trabalho remota. Essa propriedade pode ser definida usando o método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

