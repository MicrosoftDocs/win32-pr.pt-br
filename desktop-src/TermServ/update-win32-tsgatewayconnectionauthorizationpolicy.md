---
title: Método Update da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Atualiza a política de autorização de conexão do Área de Trabalho Remota atual (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayConnectionAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009442"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Update da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Atualiza a RD CAP (política de autorização de conexão) do Área de Trabalho Remota atual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Nome do RD CAP. O nome deve ter 64 caracteres ou menos, exclusivo (o caso é ignorado) e não pode conter os seguintes caracteres reservados:

<> :; " / \\ \| ? \*\[Guia\]

</dd> <dt>

*Usergroupnames* \[ no\]
</dt> <dd>

Lista de nomes de grupos de usuários separados por ponto e vírgula. Os nomes são do formato *domínio \\ userGroupName*. Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor de gateway de área de trabalho remota.

</dd> <dt>

*ComputerGroupNames* \[ no\]
</dt> <dd>

Lista de nomes de grupos de computadores separados por ponto e vírgula. Esse valor pode estar vazio. Os nomes são do formato *domínio \\ ComputerGroupName*. Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor de gateway de área de trabalho remota.

</dd> <dt>

*Cartão inteligente* \[ no\]
</dt> <dd>

Especifica se os cartões inteligentes podem ser usados para autenticar com o servidor de gateway de área de trabalho remota.

</dd> <dt>

*Senha* \[ do no\]
</dt> <dd>

Especifica se as senhas podem ser usadas para autenticar com o servidor de gateway de área de trabalho remota.

</dd> <dt>

*Segurança segura* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Especifica se este RD CAP está habilitado.

</dd> <dt>

*DeviceRedirectionType* \[ no\]
</dt> <dd>

Especifica quais tipos de dispositivo serão redirecionados.

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

Os dispositivos especificados não serão redirecionados. Os parâmetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controlam quais dispositivos não serão redirecionados.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ no\]
</dt> <dd>

Especifica se o redirecionamento de unidade de disco será desabilitado se o parâmetro *DeviceRedirectionType* for "2".

</dd> <dt>

*PrintersDisabled* \[ no\]
</dt> <dd>

Especifica se o redirecionamento de impressora deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".

</dd> <dt>

*SerialPortsDisabled* \[ no\]
</dt> <dd>

Especifica se o redirecionamento de porta serial deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".

</dd> <dt>

*ClipboardDisabled* \[ no\]
</dt> <dd>

Especifica se o redirecionamento da área de transferência deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ no\]
</dt> <dd>

Especifica se é para desabilitar o redirecionamento de dispositivos Plug and Play se o parâmetro *DeviceRedirectionType* for "2".

</dd> <dt>

*IdleTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite de ociosidade em minutos

</dd> <dt>

*SessionTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite da sessão em minutos

</dd> <dt>

*SessionTimeoutAction* \[ no\]
</dt> <dd>

Ação de tempo limite da sessão em minutos

</dd> <dt>

*AllowOnlySDRServers* \[ no\]
</dt> <dd>

Se as conexões são permitidas apenas para servidores TS SDR

</dd> <dt>

*CookieAuthentication* \[ no\]
</dt> <dd>

Indica se a autenticação de cookie pode ser usada para se conectar ao servidor Gateway TS

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

