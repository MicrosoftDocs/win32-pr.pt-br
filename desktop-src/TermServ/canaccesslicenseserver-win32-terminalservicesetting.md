---
title: Método CanAccessLicenseServer da classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer não está mais disponível.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Método CanAccessLicenseServer Serviços de Área de Trabalho Remota
- Método CanAccessLicenseServer Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método CanAccessLicenseServer
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
ms.openlocfilehash: 0f0512f42d0d814793f4ecd62fda2dd84005a4183e8db736bd16919799b4570a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139139"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método CanAccessLicenseServer da classe Win32 \_ TerminalServiceSetting

\[**CanAccessLicenseServer** não está mais disponível para uso a partir Windows Server 2008 R2.\]

**Windows Server 2008: **

Determina se o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD Serviços de Área de Trabalho Remota) tem permissão para solicitar licenças de acesso do cliente (RDS CALs) de um servidor de licença do Área de Trabalho Remota com base no seguinte:

-   A configuração de política de grupo "grupo de segurança do servidor de licença" no servidor Área de Trabalho Remota licença.
-   Associação ao grupo local Computadores do Servidor de Terminal no servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerName* \[ Em\]
</dt> <dd>

O nome do servidor de Área de Trabalho Remota licença.

</dd> <dt>

*AccessAllowed* \[ out\]
</dt> <dd>

Se o Host da Sessão RD servidor pode solicitar CALs RDS do servidor de licença.

<dt>

0
</dt> <dd>

A solicitação é permitida.

</dd> <dt>

1
</dt> <dd>

A solicitação não é permitida.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se o Host da Sessão RD servidor tiver acesso ao servidor de licença. Retornará **S \_ FALSE** se o Host da Sessão RD servidor não tiver acesso ao servidor de licença.

## <a name="remarks"></a>Comentários

A configuração de política "grupo de segurança do servidor de licença" permite que você especifique os servidores Host da Sessão RD que têm permissão para entrar em contato com o servidor de licença para obter CALs de RDS. Se a configuração de política estiver habilitada no servidor de licença, o servidor de licença responderá apenas a solicitações de CAL RDS de servidores Host da Sessão RD cujas contas de computador são membros do grupo local Computadores do Servidor terminal no servidor de licença.

Para se conectar ao \\ \\ namespace raiz CIMV2 \\ TerminalServices, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e chamadas de script, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

