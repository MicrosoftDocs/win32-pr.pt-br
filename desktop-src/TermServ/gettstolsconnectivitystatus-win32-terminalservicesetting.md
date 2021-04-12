---
title: Método GetTStoLSConnectivityStatus da classe Win32_TerminalServiceSetting
description: Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTStoLSConnectivityStatus
- Método GetTStoLSConnectivityStatus Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455390"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Método GetTStoLSConnectivityStatus da classe Win32 \_ TerminalServiceSetting

Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do Server* \[ no\]
</dt> <dd>

O nome do servidor de licença para verificar o status de conectividade.

</dd> <dt>

*TStoLSConnectivityStatus* \[ fora\]
</dt> <dd>

Um valor que indica o status de conectividade do servidor de licença. Isso pode ser um dos valores a seguir.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ CONECTADO \_ desconhecido** (0)


</dt> <dd>

Não é possível determinar o status de conectividade.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 válido conectável** (1)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença do Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 válido conectável** (2)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença do Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Incompatibilidade \_ de \_ RTM \_ beta connectável** (3)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas um dos servidores está executando uma versão beta do sistema operacional.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Versão inferior conectável** (4)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas há uma incompatibilidade entre o servidor de licença e o servidor host Serviços de Área de Trabalho Remota.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNECTável \_ não está \_ em \_ TSCGROUP** (5)


</dt> <dd>

A política de grupo de segurança está habilitada no servidor de licença, mas Serviços de Área de Trabalho Remota não faz parte da política de grupo.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ Não \_ conectável** (6)


</dt> <dd>

Serviços de Área de Trabalho Remota não pode se conectar ao servidor de licença.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validade de conexão desconhecida** (7)


</dt> <dd>

O servidor de licenças pode ser conectado ao, mas a validade da conexão não pode ser determinada.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNECTável \_ , mas \_ acesso \_ negado** (8)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas a conta de usuário não tem privilégios de administrador no servidor de licença.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ \_ \_ \_ VDI WS08R2 válido e conectável** (9)


</dt> <dd>

Serviços de Área de Trabalho Remota pode se conectar ao servidor do Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI).

**Windows Server 2008 R2:** Não há suporte para esse valor antes do Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_ \_ Não \_ há suporte para o recurso conectável** (10)


</dt> <dd>

Não há suporte para o recurso.

**Windows server 2008 R2 e Windows server 2008 R2 com SP1:** Não há suporte para esse valor antes do Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ \_ \_ Ls válido conectável** (11)


</dt> <dd>

O servidor de licença é válido.

**Windows server 2008 R2 e Windows server 2008 R2 com SP1:** Não há suporte para esse valor antes do Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





