---
title: Método CanAccessLicenseServer da classe Win32_TerminalServiceSetting
description: O CanAccessLicenseServer não está mais disponível.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanAccessLicenseServer
- Método CanAccessLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085310"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método CanAccessLicenseServer da classe Win32 \_ TerminalServiceSetting

\[O **CanAccessLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]

* * Windows Server 2008: * *

Determina se o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) tem permissão para solicitar Serviços de Área de Trabalho Remota CALs (licenças de acesso para cliente) de um servidor de licença Área de Trabalho Remota com base no seguinte:

-   A configuração da política de grupo "grupo de segurança do servidor de licenças" no servidor de licença Área de Trabalho Remota.
-   Associação no grupo local computadores Terminal Server no servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do Server* \[ no\]
</dt> <dd>

O nome do servidor de licença de Área de Trabalho Remota.

</dd> <dt>

*AccessAllowed* \[ fora\]
</dt> <dd>

Se o servidor de Host da Sessão RD tem permissão para solicitar RDS CALs do servidor de licença.

<dt>

0
</dt> <dd>

A solicitação é permitida.

</dd> <dt>

1
</dt> <dd>

A solicitação não é permitida.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se o servidor de host da Sessão RD tiver acesso ao servidor de licença. Retornará **S \_ false** se o servidor de host da Sessão RD não tiver acesso ao servidor de licença.

## <a name="remarks"></a>Comentários

A configuração de política "grupo de segurança de servidor de licenças" permite que você especifique os servidores de Host da Sessão RD que têm permissão para contatar o servidor de licença para obter RDS CALs. Se a configuração de política estiver habilitada no servidor de licença, o servidor de licença responderá apenas às solicitações de RDS CAL de Host da Sessão RD servidores cujas contas de computador são membros do grupo local de computadores Terminal Server no servidor de licença.

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6. O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte do servidor<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

