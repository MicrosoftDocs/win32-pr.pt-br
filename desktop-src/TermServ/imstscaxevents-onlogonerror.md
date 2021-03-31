---
title: Método IMsTscAxEvents OnLogonError
description: Chamado quando ocorre um erro de logon ou outro evento de logon.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnLogonError
- Método OnLogonError Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644804"
---
# <a name="imstscaxeventsonlogonerror-method"></a>Método IMsTscAxEvents:: OnLogonError

Chamado quando ocorre um erro de logon ou outro evento de logon.

## <a name="syntax"></a>Sintaxe


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lError* \[ no\]
</dt> <dd>

O código de erro de logon. Esta lista de códigos não é exaustiva.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**\_ Arbitragem \_ \_ Opções de choque de código** (-5 (0xFFFFFFFB))


</dt> <dd>

O Winlogon está exibindo a caixa de diálogo de **contenção de sessão** .

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**\_ Arbitragem O código \_ continua o \_ logon** (-2 (0xFFFFFFFE))


</dt> <dd>

O Winlogon continua com o processo de logon.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**\_ Arbitragem \_ \_ Término do código de continuação** (-3 (0xFFFFFFFD))


</dt> <dd>

O Winlogon está terminando silenciosamente.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**\_ Arbitragem \_ \_ Caixa de diálogo código noperm** (-6 (0xFFFFFFFA))


</dt> <dd>

O Winlogon está exibindo a caixa de diálogo **sem permissões** .

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**\_ Arbitragem \_Caixa de \_ diálogo código recusado** (-7 (0xFFFFFFF9))


</dt> <dd>

O Winlogon está exibindo a caixa de diálogo **Desconectar recusada** .

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**\_ Arbitragem \_ \_ Opções de reconecção de código** (-4 (0xFFFFFFFC))


</dt> <dd>

O Winlogon está exibindo a caixa de diálogo **reconectar** .

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Erro \_ do Acesso ao código \_ \_ negado** (-1 (0xFFFFFFFF))


</dt> <dd>

O acesso ao usuário foi negado.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Logon \_ do \_ \_ Senha inadequada com falha** (0 (0x0))


</dt> <dd>

O logon falhou porque as credenciais de logon não são válidas.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Logon \_ do \_Outro com falha** (2 (0x2))


</dt> <dd>

Ocorreu outro erro de logon ou pós-logon. O cliente Área de Trabalho Remota exibe uma tela de logon para o usuário.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Logon \_ do FALHA na \_ atualização da \_ senha** (1 (0x1))


</dt> <dd>

A senha expirou. O usuário deve atualizar sua senha para continuar a fazer logon.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Logon \_ do AVISO** (3 (0x3))


</dt> <dd>

O cliente Área de Trabalho Remota exibe uma caixa de diálogo que contém informações importantes para o usuário.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Status \_ do \_Restrição de conta** (-1073741714 (0xC000006E))


</dt> <dd>

As informações de nome de usuário e de autenticação são válidas, mas a autenticação foi bloqueada devido a restrições na conta de usuário, como restrições de hora do dia.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Status \_ do \_Falha de logon** (-1073741715 (0xC000006D))


</dt> <dd>

A tentativa de logon não é válida. Isso ocorre devido a um nome de usuário incorreto ou a informações de autenticação incorretas.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Status \_ do A senha \_ deve ser \_ alterada** (-1073741276 (0xC0000224))


</dt> <dd>

A senha expirou. O usuário deve atualizar sua senha para continuar a fazer logon.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método em seu coletor de eventos para receber uma notificação de que ocorreu um erro de logon.

Esta lista de códigos não é exaustiva.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





