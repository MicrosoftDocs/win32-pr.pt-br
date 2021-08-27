---
title: Método update da classe Win32_TSGatewayConnectionAuthorizationPolicy dados
description: Atualiza a política de Área de Trabalho Remota de conexão atual (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Atualizar o método Serviços de Área de Trabalho Remota
- Atualizar a Serviços de Área de Trabalho Remota , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método Update
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
ms.openlocfilehash: 2ec7c3d1802f4faa3da8e382d00aa14fc8b3e091baef9659ad45322ec2a909c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850875"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método update da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Atualiza a política atual Área de Trabalho Remota de autorização de conexão (RD CAP).

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

*Nome* \[ Em\]
</dt> <dd>

Nome do RD CAP. O nome deve ter 64 caracteres ou menos, exclusivo (o caso é ignorado) e não pode conter os seguintes caracteres reservados:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> <dt>

*UserGroupNames* \[ Em\]
</dt> <dd>

Lista de nomes de grupo de usuários separados por ponto e vírgula. Os nomes são do formato *Domain \\ UserGroupName*. Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor do Gateway de Área de Trabalho Remoto.

</dd> <dt>

*ComputerGroupNames* \[ Em\]
</dt> <dd>

Lista de nomes de grupos de máquinas separados por ponto e vírgula. Esse valor pode estar vazio. Os nomes são do formato *Domain \\ ComputerGroupName*. Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor do Gateway de Área de Trabalho Remoto.

</dd> <dt>

*Cartão Inteligente* \[ Em\]
</dt> <dd>

Especifica se os cartões inteligentes podem ser usados para autenticar com o servidor de Gateway de RD.

</dd> <dt>

*Senha* \[ Em\]
</dt> <dd>

Especifica se as senhas podem ser usadas para autenticar com o servidor de Gateway de RD.

</dd> <dt>

*SecureId* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> <dt>

*Habilitado* \[ Em\]
</dt> <dd>

Especifica se essa RD CAP está habilitada.

</dd> <dt>

*DeviceRedirectionType* \[ Em\]
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

Os dispositivos especificados não serão redirecionados. Os *parâmetros DiskDrivesDisabled,* *PrintersDisabled,* *SerialPortsDisabled,* *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controlam quais dispositivos não serão redirecionados.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ Em\]
</dt> <dd>

Especifica se o redirecionamento de unidade de disco deve ser desabilitado se *o parâmetro DeviceRedirectionType* for "2".

</dd> <dt>

*PrintersDisabled* \[ Em\]
</dt> <dd>

Especifica se o redirecionamento de impressora deve ser desabilitado se *o parâmetro DeviceRedirectionType* for "2".

</dd> <dt>

*SerialPortsDisabled* \[ Em\]
</dt> <dd>

Especifica se o redirecionamento de porta serial deve ser desabilitado se *o parâmetro DeviceRedirectionType* for "2".

</dd> <dt>

*ClipboardDisabled* \[ Em\]
</dt> <dd>

Especifica se o redirecionamento da área de transferência deve ser desabilitado se *o parâmetro DeviceRedirectionType* for "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ Em\]
</dt> <dd>

Especifica se o redirecionamento de Plug and Play dispositivos se *o parâmetro DeviceRedirectionType* for "2".

</dd> <dt>

*IdleTimeout* \[ Em\]
</dt> <dd>

Valor de tempo de ociosidade em minutos

</dd> <dt>

*SessionTimeout* \[ Em\]
</dt> <dd>

Valor de tempo de tempo de sessão em minutos

</dd> <dt>

*SessionTimeoutAction* \[ Em\]
</dt> <dd>

Ação de tempo de tempo de sessão em minutos

</dd> <dt>

*AllowOnlySDRServers* \[ Em\]
</dt> <dd>

Se as conexões só podem ser permitidas para servidores SDR TS

</dd> <dt>

*CookieAuthentication* \[ Em\]
</dt> <dd>

Indica se a autenticação de cookie pode ser usada para se conectar ao servidor do Gateway do TS

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

