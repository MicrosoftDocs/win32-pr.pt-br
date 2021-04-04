---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Descreve um Área de Trabalho Remota a política de autorização de conexão (RD \ 160; CAP). RD \ 160; As CAPs são usadas para determinar se um usuário tem permissão para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayConnectionAuthorizationPolicy classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824352"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>\_Classe Win32 TSGatewayConnectionAuthorizationPolicy

Descreve um Área de Trabalho Remota RD CAP (política de autorização de conexão). As RD CAPs são usadas para determinar se um usuário tem permissão para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem esses métodos.



| Método                                                                                                                | Descrição                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Adiciona os nomes de grupo de computadores especificados à propriedade **ComputerGroupNames** .<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Adiciona os nomes de grupos de usuários especificados à propriedade **Usergroupnames** .<br/>                                                                                              |
| [**Criar**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Cria um RD CAP.<br/>                                                                                                                                                   |
| [**Apagar**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Exclui o RD CAP atual.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Define a propriedade **ClipboardDisabled** .<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Define a propriedade **DiskDrivesDisabled** .<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Define a propriedade **PlugAndPlayDevicesDisabled** .<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Define a propriedade **PrintersDisabled** .<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Define a propriedade **SerialPortsDisabled** .<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Usado para alternar a propriedade **AllowOnlySDRServers**<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                  |
| [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Move a RD CAP atual uma posição para baixo na lista.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Move a RD CAP atual uma posição para cima na lista.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Remove os nomes de grupos de computadores especificados da propriedade **ComputerGroupNames** .<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Remove os nomes de grupo de usuários especificados da propriedade **Usergroupnames** .<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Define a propriedade **ComputerGroupNames** .<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Define a propriedade **CookieAuthenticationAllowed** .<br/> **Windows Server 2008:** Este método não está disponível.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Define a propriedade **DeviceRedirectionType** .<br/>                                                                                                                         |
| [**Sethabilitado**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Habilita ou desabilita a RD CAP atual.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Define a propriedade **IdleTimeout** .<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Define um novo nome para este RD CAP. Esse método garante que os nomes serão exclusivos.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Define a propriedade **PasswordAllowed** .<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Define a propriedade **SecureIdAllowed** .<br/> **Windows Server 2008:** Esse método é reservado para uso futuro.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Define as propriedades **SessionTimeout** e **SessionTimeoutAction** .<br/> **Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Define a propriedade **SmartcardAllowed** .<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Define a propriedade **Usergroupnames** .<br/>                                                                                                                                |
| [**Cumulativo**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Atualiza o RD CAP atual.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem essas propriedades.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as conexões são permitidas apenas para proteger servidores RDS do redirecionamento de dispositivo (SDR). Essa propriedade pode ser definida usando o método [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .

**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o redirecionamento da área de transferência será desabilitado. Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de nomes de grupos de computadores separados por ponto e vírgula. Esse valor pode estar vazio. Os nomes são do formato *domínio \\ ComputerGroupName*. Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor de gateway de área de trabalho remota.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a autenticação de cookie pode ser usada para se conectar ao servidor de gateway de área de trabalho remota. Essa propriedade pode ser definida usando o método [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica quais dispositivos serão redirecionados.

<dt>

0
</dt> <dd>

Todos os dispositivos serão redirecionados.

</dd> <dt>

1
</dt> <dd>

Nenhum dispositivo será redirecionado.

</dd> <dt>

2
</dt> <dd>

Os dispositivos especificados não serão redirecionados. As propriedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controlam quais dispositivos não serão redirecionados.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o redirecionamento de unidade de disco será desabilitado. Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se este RD CAP será usado para avaliar um usuário para autorização.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o RD CAP usa atributos NAP (proteção de acesso à rede).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O valor de tempo limite de ociosidade, em minutos. Um valor de 0 significa que não há nenhum tempo limite. Essa propriedade pode ser definida usando o método [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do RD CAP.

</dd> <dt>

**Ordem**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ordem de avaliação do RD CAP. A primeira RD CAP avaliada tem um valor de "1". A propriedade **Order** pode ser alterada quando os [**métodos Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)ou [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) são chamados.

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se uma senha pode ser usada para se conectar ao servidor de gateway de área de trabalho remota. Essa propriedade pode ser alterada usando o método [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o redirecionamento de dispositivos Plug and Play será desabilitado. Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".

</dd> <dt>

**PrintersDisabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o redirecionamento de impressora será desabilitado. Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se um identificador seguro pode ser usado para se conectar ao servidor de gateway de área de trabalho remota.

**Windows Server 2008:** Essa propriedade não é usada.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o redirecionamento de porta serial será desabilitado. Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O valor de tempo limite da sessão, em minutos. Um valor de 0 significa que não há nenhum tempo limite. Essa propriedade pode ser definida usando o método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a ação a ser executada no caso de um tempo limite de sessão. Essa propriedade pode ser definida usando o método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

Isso pode ser um dos valores a seguir.

**Windows Server 2008:** Esta propriedade não está disponível.

<dt>

0
</dt> <dd>

Desconecte a sessão.

</dd> <dt>

1
</dt> <dd>

Tentativa de autorizar a sessão novamente.

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se um cartão inteligente pode ser usado para se conectar ao servidor de gateway de área de trabalho remota. Essa propriedade pode ser alterada usando o método [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**Usergroupnames**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de nomes de grupos de usuários separados por ponto e vírgula. Os nomes são do formato *domínio \\ userGroupName*. Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor de gateway de área de trabalho remota.

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

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

