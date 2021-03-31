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
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="2b10c-106">Método IMsTscAxEvents:: OnLogonError</span><span class="sxs-lookup"><span data-stu-id="2b10c-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="2b10c-107">Chamado quando ocorre um erro de logon ou outro evento de logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b10c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b10c-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="2b10c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b10c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b10c-110">*lError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b10c-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b10c-111">O código de erro de logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-111">The logon error code.</span></span> <span data-ttu-id="2b10c-112">Esta lista de códigos não é exaustiva.</span><span class="sxs-lookup"><span data-stu-id="2b10c-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="2b10c-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**\_ Arbitragem \_ \_ Opções de choque de código** (-5 (0xFFFFFFFB))</span><span class="sxs-lookup"><span data-stu-id="2b10c-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-114">O Winlogon está exibindo a caixa de diálogo de **contenção de sessão** .</span><span class="sxs-lookup"><span data-stu-id="2b10c-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="2b10c-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**\_ Arbitragem O código \_ continua o \_ logon** (-2 (0xFFFFFFFE))</span><span class="sxs-lookup"><span data-stu-id="2b10c-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-116">O Winlogon continua com o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="2b10c-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**\_ Arbitragem \_ \_ Término do código de continuação** (-3 (0xFFFFFFFD))</span><span class="sxs-lookup"><span data-stu-id="2b10c-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-118">O Winlogon está terminando silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="2b10c-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="2b10c-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**\_ Arbitragem \_ \_ Caixa de diálogo código noperm** (-6 (0xFFFFFFFA))</span><span class="sxs-lookup"><span data-stu-id="2b10c-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-120">O Winlogon está exibindo a caixa de diálogo **sem permissões** .</span><span class="sxs-lookup"><span data-stu-id="2b10c-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="2b10c-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**\_ Arbitragem \_Caixa de \_ diálogo código recusado** (-7 (0xFFFFFFF9))</span><span class="sxs-lookup"><span data-stu-id="2b10c-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-122">O Winlogon está exibindo a caixa de diálogo **Desconectar recusada** .</span><span class="sxs-lookup"><span data-stu-id="2b10c-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="2b10c-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**\_ Arbitragem \_ \_ Opções de reconecção de código** (-4 (0xFFFFFFFC))</span><span class="sxs-lookup"><span data-stu-id="2b10c-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-124">O Winlogon está exibindo a caixa de diálogo **reconectar** .</span><span class="sxs-lookup"><span data-stu-id="2b10c-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="2b10c-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Erro \_ do Acesso ao código \_ \_ negado** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="2b10c-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-126">O acesso ao usuário foi negado.</span><span class="sxs-lookup"><span data-stu-id="2b10c-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="2b10c-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Logon \_ do \_ \_ Senha inadequada com falha** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2b10c-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-128">O logon falhou porque as credenciais de logon não são válidas.</span><span class="sxs-lookup"><span data-stu-id="2b10c-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="2b10c-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Logon \_ do \_Outro com falha** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="2b10c-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-130">Ocorreu outro erro de logon ou pós-logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="2b10c-131">O cliente Área de Trabalho Remota exibe uma tela de logon para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2b10c-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="2b10c-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Logon \_ do FALHA na \_ atualização da \_ senha** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="2b10c-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-133">A senha expirou.</span><span class="sxs-lookup"><span data-stu-id="2b10c-133">The password is expired.</span></span> <span data-ttu-id="2b10c-134">O usuário deve atualizar sua senha para continuar a fazer logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="2b10c-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Logon \_ do AVISO** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="2b10c-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-136">O cliente Área de Trabalho Remota exibe uma caixa de diálogo que contém informações importantes para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2b10c-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="2b10c-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Status \_ do \_Restrição de conta** (-1073741714 (0xC000006E))</span><span class="sxs-lookup"><span data-stu-id="2b10c-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-138">As informações de nome de usuário e de autenticação são válidas, mas a autenticação foi bloqueada devido a restrições na conta de usuário, como restrições de hora do dia.</span><span class="sxs-lookup"><span data-stu-id="2b10c-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="2b10c-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Status \_ do \_Falha de logon** (-1073741715 (0xC000006D))</span><span class="sxs-lookup"><span data-stu-id="2b10c-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-140">A tentativa de logon não é válida.</span><span class="sxs-lookup"><span data-stu-id="2b10c-140">The attempted logon is not valid.</span></span> <span data-ttu-id="2b10c-141">Isso ocorre devido a um nome de usuário incorreto ou a informações de autenticação incorretas.</span><span class="sxs-lookup"><span data-stu-id="2b10c-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="2b10c-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Status \_ do A senha \_ deve ser \_ alterada** (-1073741276 (0xC0000224))</span><span class="sxs-lookup"><span data-stu-id="2b10c-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="2b10c-143">A senha expirou.</span><span class="sxs-lookup"><span data-stu-id="2b10c-143">The password is expired.</span></span> <span data-ttu-id="2b10c-144">O usuário deve atualizar sua senha para continuar a fazer logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b10c-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b10c-145">Return value</span></span>

<span data-ttu-id="2b10c-146">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2b10c-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b10c-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b10c-147">Remarks</span></span>

<span data-ttu-id="2b10c-148">Implemente esse método em seu coletor de eventos para receber uma notificação de que ocorreu um erro de logon.</span><span class="sxs-lookup"><span data-stu-id="2b10c-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="2b10c-149">Esta lista de códigos não é exaustiva.</span><span class="sxs-lookup"><span data-stu-id="2b10c-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b10c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b10c-150">Requirements</span></span>



| <span data-ttu-id="2b10c-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b10c-151">Requirement</span></span> | <span data-ttu-id="2b10c-152">Valor</span><span class="sxs-lookup"><span data-stu-id="2b10c-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b10c-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b10c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2b10c-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b10c-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2b10c-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b10c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2b10c-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b10c-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2b10c-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b10c-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b10c-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b10c-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b10c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="2b10c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b10c-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b10c-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b10c-161">IID</span><span class="sxs-lookup"><span data-stu-id="2b10c-161">IID</span></span><br/>                      | <span data-ttu-id="2b10c-162">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="2b10c-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="2b10c-163">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2b10c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b10c-164">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="2b10c-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





