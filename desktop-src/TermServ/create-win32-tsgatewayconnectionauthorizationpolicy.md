---
title: Método Create da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Cria uma política de autorização de conexão Área de Trabalho Remota (RD \ 160; CAP) usando os valores especificados. A nova RD \ 160; A CAP será inserida na parte superior da área de trabalho remota \ 160; Ordem de avaliação de CAP, com um valor de propriedade de ordem de \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16bf9dadb2a76a46d607a6cf2554192e3658686b58a089c19c3604c0c510bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871856"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Create da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Cria uma Área de Trabalho Remota política de autorização de conexão (RD CAP) usando os valores especificados. O novo RD CAP será inserido na parte superior da ordem de avaliação de RD CAP, com um valor de propriedade de **ordem** de "1".

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
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

Lista de nomes de grupos de usuários, separados por ponto e vírgula, para o novo RD CAP.

</dd> <dt>

*ComputerGroupNames* \[ no\]
</dt> <dd>

Lista de nomes de grupos de computadores, separados por ponto e vírgula, para o novo RD CAP.

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

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

