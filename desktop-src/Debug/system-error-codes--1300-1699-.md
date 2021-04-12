---
description: Descreve os códigos de erro 1300-1699 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Códigos de erro do sistema (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457024"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="48675-103">Códigos de erro do sistema (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="48675-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="48675-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="48675-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="48675-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="48675-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="48675-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 1300 a 1699.</span><span class="sxs-lookup"><span data-stu-id="48675-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="48675-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="48675-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="48675-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="48675-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="48675-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERRO \_ nem \_ todos \_ atribuídos**</span><span class="sxs-lookup"><span data-stu-id="48675-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="48675-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="48675-111">Nem todos os privilégios ou grupos referenciados são atribuídos ao chamador.</span><span class="sxs-lookup"><span data-stu-id="48675-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERRO \_ algum \_ não \_ mapeado**</span><span class="sxs-lookup"><span data-stu-id="48675-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="48675-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="48675-114">Não foi feito um mapeamento entre os nomes de conta e as IDs de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERRO \_ sem \_ cotas \_ para a \_ conta**</span><span class="sxs-lookup"><span data-stu-id="48675-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="48675-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="48675-117">Nenhum limite de cota de sistema é definido especificamente para essa conta.</span><span class="sxs-lookup"><span data-stu-id="48675-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERRO \_ de \_ \_ chave de sessão de usuário local \_**</span><span class="sxs-lookup"><span data-stu-id="48675-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="48675-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="48675-120">Nenhuma chave de criptografia está disponível.</span><span class="sxs-lookup"><span data-stu-id="48675-120">No encryption key is available.</span></span> <span data-ttu-id="48675-121">Uma chave de criptografia bem conhecida foi retornada.</span><span class="sxs-lookup"><span data-stu-id="48675-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERRO \_ de \_ senha LM nula \_**</span><span class="sxs-lookup"><span data-stu-id="48675-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="48675-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="48675-124">A senha é muito complexa para ser convertida em uma senha do Gerenciador de LAN.</span><span class="sxs-lookup"><span data-stu-id="48675-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="48675-125">A senha do Gerenciador de LAN retornada é uma cadeia de caracteres **nula** .</span><span class="sxs-lookup"><span data-stu-id="48675-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**revisão de erro \_ desconhecida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="48675-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="48675-128">O nível de revisão é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="48675-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**incompatibilidade de revisão de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="48675-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-131">Indica que dois níveis de revisão são incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="48675-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**\_proprietário inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="48675-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-134">Esta ID de segurança não pode ser atribuída como o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="48675-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERRO \_ de \_ grupo primário inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="48675-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-137">Essa ID de segurança não pode ser atribuída como o grupo primário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="48675-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERRO \_ sem \_ token de representação \_**</span><span class="sxs-lookup"><span data-stu-id="48675-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="48675-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-140">Foi feita uma tentativa de operar em um token de representação por um thread que não está representando um cliente no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERRO não é possível \_ \_ desabilitar \_ obrigatório**</span><span class="sxs-lookup"><span data-stu-id="48675-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="48675-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-143">O grupo pode não estar desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48675-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERRO \_ sem \_ servidores de logon \_**</span><span class="sxs-lookup"><span data-stu-id="48675-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="48675-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-146">No momento, não há servidores de logon disponíveis para atender à solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="48675-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERRO \_ sem \_ \_ sessão de logon \_**</span><span class="sxs-lookup"><span data-stu-id="48675-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="48675-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="48675-149">Uma sessão de logon especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-149">A specified logon session does not exist.</span></span> <span data-ttu-id="48675-150">Ele pode já ter sido encerrado.</span><span class="sxs-lookup"><span data-stu-id="48675-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERRO \_ sem \_ esse \_ privilégio**</span><span class="sxs-lookup"><span data-stu-id="48675-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="48675-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="48675-153">Um privilégio especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**privilégio de erro \_ \_ não \_ mantido**</span><span class="sxs-lookup"><span data-stu-id="48675-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="48675-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="48675-156">O cliente não possui o privilégio exigido.</span><span class="sxs-lookup"><span data-stu-id="48675-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**\_nome de \_ conta \_ inválido do erro**</span><span class="sxs-lookup"><span data-stu-id="48675-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="48675-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="48675-159">O nome fornecido não é um nome de conta formado corretamente.</span><span class="sxs-lookup"><span data-stu-id="48675-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERRO o \_ usuário \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="48675-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="48675-162">A conta especificada já existe.</span><span class="sxs-lookup"><span data-stu-id="48675-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERRO \_ não é \_ desse \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="48675-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="48675-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="48675-165">A conta especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**o \_ grupo de erros \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="48675-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="48675-168">O grupo especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="48675-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERRO \_ não \_ existe \_ grupo**</span><span class="sxs-lookup"><span data-stu-id="48675-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="48675-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="48675-171">O grupo especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_membro \_ de erro no \_ grupo**</span><span class="sxs-lookup"><span data-stu-id="48675-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="48675-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="48675-174">A conta de usuário especificada já é um membro do grupo especificado ou o grupo especificado não pode ser excluído porque contém um membro.</span><span class="sxs-lookup"><span data-stu-id="48675-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**o \_ membro \_ de erro não está \_ no \_ grupo**</span><span class="sxs-lookup"><span data-stu-id="48675-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="48675-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="48675-177">A conta de usuário especificada não é membro da conta de grupo especificada.</span><span class="sxs-lookup"><span data-stu-id="48675-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERRO do \_ último \_ administrador**</span><span class="sxs-lookup"><span data-stu-id="48675-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="48675-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-180">Esta operação não é permitida, pois pode resultar em uma conta de administração desabilitada, excluída ou não conseguir fazer logon.</span><span class="sxs-lookup"><span data-stu-id="48675-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERRO \_ de \_ senha incorreta**</span><span class="sxs-lookup"><span data-stu-id="48675-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="48675-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-183">Não é possível atualizar a senha.</span><span class="sxs-lookup"><span data-stu-id="48675-183">Unable to update the password.</span></span> <span data-ttu-id="48675-184">O valor fornecido como a senha atual está incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERRO \_ de \_ senha mal formada \_**</span><span class="sxs-lookup"><span data-stu-id="48675-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="48675-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-187">Não é possível atualizar a senha.</span><span class="sxs-lookup"><span data-stu-id="48675-187">Unable to update the password.</span></span> <span data-ttu-id="48675-188">O valor fornecido para a nova senha contém valores que não são permitidos em senhas.</span><span class="sxs-lookup"><span data-stu-id="48675-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restrição de senha de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-190">1325 (0x52D)</span><span class="sxs-lookup"><span data-stu-id="48675-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-191">Não é possível atualizar a senha.</span><span class="sxs-lookup"><span data-stu-id="48675-191">Unable to update the password.</span></span> <span data-ttu-id="48675-192">O valor fornecido para a nova senha não atende aos requisitos de comprimento, complexidade ou histórico do domínio.</span><span class="sxs-lookup"><span data-stu-id="48675-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**\_falha no logon do erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="48675-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-195">O nome de usuário ou senha está incorreta.</span><span class="sxs-lookup"><span data-stu-id="48675-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restrição de conta de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="48675-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-198">As restrições de conta estão impedindo o usuário de entrar.</span><span class="sxs-lookup"><span data-stu-id="48675-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="48675-199">Por exemplo: senhas em branco não são permitidas, tempos de entrada são limitados ou uma restrição de política foi imposta.</span><span class="sxs-lookup"><span data-stu-id="48675-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**\_horário de \_ logon \_ inválido do erro**</span><span class="sxs-lookup"><span data-stu-id="48675-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="48675-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="48675-202">Sua conta tem restrições de tempo que o impedem de entrar no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERRO \_ de \_ estação de trabalho inválida**</span><span class="sxs-lookup"><span data-stu-id="48675-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="48675-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="48675-205">Este usuário não tem permissão para entrar neste computador.</span><span class="sxs-lookup"><span data-stu-id="48675-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERRO de \_ senha \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="48675-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="48675-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="48675-208">A senha desta conta expirou.</span><span class="sxs-lookup"><span data-stu-id="48675-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**conta de erro \_ \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="48675-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="48675-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="48675-211">Este usuário não pode entrar porque esta conta está desabilitada no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERRO \_ nenhum \_ mapeado**</span><span class="sxs-lookup"><span data-stu-id="48675-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="48675-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="48675-214">Nenhum mapeamento entre os nomes de conta e as IDs de segurança foi feito.</span><span class="sxs-lookup"><span data-stu-id="48675-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERRO \_ número \_ excessivo de \_ LUIDS \_ solicitados**</span><span class="sxs-lookup"><span data-stu-id="48675-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="48675-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="48675-217">Um número excessivo de identificadores de usuário local (LUIDs) foi solicitado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="48675-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERRO \_ LUIDS \_ esgotado**</span><span class="sxs-lookup"><span data-stu-id="48675-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="48675-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="48675-220">Não há mais identificadores de usuário local (LUIDs) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="48675-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**\_sub- \_ \_ autoridade INválida de erro**</span><span class="sxs-lookup"><span data-stu-id="48675-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="48675-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="48675-223">A parte de subautoridade de uma ID de segurança é inválida para esse uso específico.</span><span class="sxs-lookup"><span data-stu-id="48675-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERRO \_ \_ ACL inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="48675-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="48675-226">A estrutura da ACL (lista de controle de acesso) é inválida.</span><span class="sxs-lookup"><span data-stu-id="48675-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERRO \_ \_ Sid inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="48675-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="48675-229">A estrutura da ID de segurança é inválida.</span><span class="sxs-lookup"><span data-stu-id="48675-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERRO \_ de \_ descr de segurança inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="48675-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-232">A estrutura do descritor de segurança é inválida.</span><span class="sxs-lookup"><span data-stu-id="48675-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERRO \_ \_ ACL de herança inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="48675-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-234">1340 (0x53C)</span><span class="sxs-lookup"><span data-stu-id="48675-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-235">Não foi possível criar a ACL (lista de controle de acesso) herdada ou a ACE (entrada de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="48675-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**servidor de erro \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="48675-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="48675-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-238">O servidor está desabilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**servidor de erro \_ \_ não \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="48675-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="48675-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-241">O servidor está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERRO \_ de \_ autoridade de identificação inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="48675-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-244">O valor fornecido era um valor inválido para uma autoridade de identificador.</span><span class="sxs-lookup"><span data-stu-id="48675-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_espaço alocado de \_ erro \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="48675-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="48675-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="48675-247">Não há mais memória disponível para atualizações de informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERRO \_ de \_ atributos de grupo inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="48675-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="48675-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="48675-250">Os atributos especificados são inválidos ou incompatíveis com os atributos do grupo como um todo.</span><span class="sxs-lookup"><span data-stu-id="48675-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERRO \_ de \_ nível de representação insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="48675-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="48675-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="48675-253">O nível de representação necessário não foi fornecido ou o nível de representação fornecido é inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERRO não é possível \_ \_ abrir \_ anônimo**</span><span class="sxs-lookup"><span data-stu-id="48675-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="48675-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="48675-256">Não é possível abrir um token de segurança de nível anônimo.</span><span class="sxs-lookup"><span data-stu-id="48675-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERRO \_ de \_ classe de validação inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="48675-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="48675-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="48675-259">A classe de informações de validação solicitada era inválida.</span><span class="sxs-lookup"><span data-stu-id="48675-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERRO \_ de \_ tipo de token insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="48675-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="48675-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="48675-262">O tipo do token não é apropriado para o uso tentado.</span><span class="sxs-lookup"><span data-stu-id="48675-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERRO \_ sem \_ segurança \_ no \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="48675-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="48675-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="48675-265">Não é possível executar uma operação de segurança em um objeto que não tem segurança associada.</span><span class="sxs-lookup"><span data-stu-id="48675-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERRO não é possível \_ \_ acessar as \_ informações do domínio \_**</span><span class="sxs-lookup"><span data-stu-id="48675-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="48675-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="48675-268">Não foi possível ler as informações de configuração do controlador de domínio porque o computador não está disponível ou o acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="48675-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERRO \_ inválido \_ no \_ estado do servidor**</span><span class="sxs-lookup"><span data-stu-id="48675-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="48675-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="48675-271">O Gerenciador de contas de segurança (SAM) ou o servidor de autoridade de segurança local (LSA) estava no estado incorreto para executar a operação de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERRO \_ de \_ estado de domínio inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="48675-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="48675-274">O domínio estava no estado incorreto para executar a operação de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERRO \_ de \_ função de domínio inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="48675-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-277">Esta operação só é permitida para o controlador de domínio primário do domínio.</span><span class="sxs-lookup"><span data-stu-id="48675-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERRO \_ no domínio inexistente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-279">1355 (0x54B)</span><span class="sxs-lookup"><span data-stu-id="48675-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-280">O domínio especificado não existe ou não pôde ser contatado.</span><span class="sxs-lookup"><span data-stu-id="48675-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**o \_ domínio de erro \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="48675-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-283">O domínio especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="48675-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**limite de domínio de erro \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="48675-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-285">1357 (0x54D)</span><span class="sxs-lookup"><span data-stu-id="48675-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-286">Foi feita uma tentativa de exceder o limite do número de domínios por servidor.</span><span class="sxs-lookup"><span data-stu-id="48675-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERRO \_ de \_ corrupção interna do BD \_**</span><span class="sxs-lookup"><span data-stu-id="48675-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-288">1358 (0x54E)</span><span class="sxs-lookup"><span data-stu-id="48675-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-289">Não é possível concluir a operação solicitada devido a uma falha catastrófica na mídia ou à corrupção de uma estrutura de dados no disco.</span><span class="sxs-lookup"><span data-stu-id="48675-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**erro \_ interno de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-291">1359 (0x54F)</span><span class="sxs-lookup"><span data-stu-id="48675-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-292">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="48675-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERRO \_ genérico \_ não \_ mapeado**</span><span class="sxs-lookup"><span data-stu-id="48675-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="48675-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="48675-295">Os tipos de acesso genéricos estavam contidos em uma máscara de acesso que já deve estar mapeada para tipos não genéricos.</span><span class="sxs-lookup"><span data-stu-id="48675-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERRO \_ de \_ formato de descritor inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="48675-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="48675-298">Um descritor de segurança não está no formato correto (absoluto ou auto-relativo).</span><span class="sxs-lookup"><span data-stu-id="48675-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERRO \_ não \_ processo de logon \_**</span><span class="sxs-lookup"><span data-stu-id="48675-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="48675-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="48675-301">A ação solicitada é restrita para uso somente por processos de logon.</span><span class="sxs-lookup"><span data-stu-id="48675-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="48675-302">O processo de chamada não foi registrado como um processo de logon.</span><span class="sxs-lookup"><span data-stu-id="48675-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**a \_ sessão de logon de erro \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="48675-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="48675-305">Não é possível iniciar uma nova sessão de logon com uma ID que já está em uso.</span><span class="sxs-lookup"><span data-stu-id="48675-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERRO \_ nenhum \_ pacote desse tipo \_**</span><span class="sxs-lookup"><span data-stu-id="48675-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="48675-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="48675-308">Um pacote de autenticação especificado é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="48675-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERRO \_ \_ estado de \_ sessão de logon insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="48675-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="48675-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="48675-311">A sessão de logon não está em um estado consistente com a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="48675-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERRO \_ de \_ colisão de sessão de logon \_**</span><span class="sxs-lookup"><span data-stu-id="48675-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="48675-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="48675-314">A ID da sessão de logon já está em uso.</span><span class="sxs-lookup"><span data-stu-id="48675-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERRO \_ de \_ tipo de logon inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="48675-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="48675-317">Uma solicitação de logon continha um valor de tipo de logon inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERRO \_ não pode \_ representar**</span><span class="sxs-lookup"><span data-stu-id="48675-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="48675-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="48675-320">Não é possível representar usando um pipe nomeado até que os dados tenham sido lidos desse pipe.</span><span class="sxs-lookup"><span data-stu-id="48675-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERRO \_ RXACT \_ \_ estado inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="48675-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="48675-323">O estado de transação de uma subárvore do registro é incompatível com a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="48675-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERRO \_ RXACT \_ \_ falha na confirmação**</span><span class="sxs-lookup"><span data-stu-id="48675-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-325">1370 (0x55A)</span><span class="sxs-lookup"><span data-stu-id="48675-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-326">Foi encontrado um banco de dados de segurança interno corrompido.</span><span class="sxs-lookup"><span data-stu-id="48675-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERRO \_ de \_ conta especial**</span><span class="sxs-lookup"><span data-stu-id="48675-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-328">1371 (0x55B)</span><span class="sxs-lookup"><span data-stu-id="48675-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-329">Não é possível executar esta operação em contas internas.</span><span class="sxs-lookup"><span data-stu-id="48675-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERRO \_ de \_ grupo especial**</span><span class="sxs-lookup"><span data-stu-id="48675-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-331">1372 (0x55C)</span><span class="sxs-lookup"><span data-stu-id="48675-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-332">Não é possível executar esta operação neste grupo especial interno.</span><span class="sxs-lookup"><span data-stu-id="48675-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERRO \_ especial do \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="48675-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="48675-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-335">Não é possível executar esta operação neste usuário especial interno.</span><span class="sxs-lookup"><span data-stu-id="48675-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ grupo primário de membros de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="48675-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-338">O usuário não pode ser removido de um grupo porque o grupo é atualmente o grupo primário do usuário.</span><span class="sxs-lookup"><span data-stu-id="48675-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**o \_ token \_ de erro já está \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="48675-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-340">1375 (0x55F)</span><span class="sxs-lookup"><span data-stu-id="48675-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-341">O token já está em uso como um token primário.</span><span class="sxs-lookup"><span data-stu-id="48675-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERRO \_ sem \_ \_ alias**</span><span class="sxs-lookup"><span data-stu-id="48675-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="48675-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="48675-344">O grupo local especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**o \_ membro \_ do erro não está \_ no \_ alias**</span><span class="sxs-lookup"><span data-stu-id="48675-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="48675-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="48675-347">O nome de conta especificado não é um membro do grupo.</span><span class="sxs-lookup"><span data-stu-id="48675-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_membro \_ de erro no \_ alias**</span><span class="sxs-lookup"><span data-stu-id="48675-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="48675-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="48675-350">O nome de conta especificado já é um membro do grupo.</span><span class="sxs-lookup"><span data-stu-id="48675-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**o \_ alias de erro \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="48675-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="48675-353">O grupo local especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="48675-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERRO de \_ logon \_ não \_ concedido**</span><span class="sxs-lookup"><span data-stu-id="48675-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="48675-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="48675-356">Falha de logon: o usuário não recebeu o tipo de logon solicitado neste computador.</span><span class="sxs-lookup"><span data-stu-id="48675-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERRO \_ de \_ muitos \_ segredos**</span><span class="sxs-lookup"><span data-stu-id="48675-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="48675-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="48675-359">O número máximo de segredos que podem ser armazenados em um único sistema foi excedido.</span><span class="sxs-lookup"><span data-stu-id="48675-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**segredo de erro \_ \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="48675-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="48675-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="48675-362">O comprimento de um segredo excede o comprimento máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="48675-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**erro \_ interno do \_ BD de \_ erros**</span><span class="sxs-lookup"><span data-stu-id="48675-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="48675-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="48675-365">O banco de dados da autoridade de segurança local contém uma inconsistência interna.</span><span class="sxs-lookup"><span data-stu-id="48675-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERRO em excesso de \_ \_ \_ IDs de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="48675-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="48675-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="48675-368">Durante uma tentativa de logon, o contexto de segurança do usuário acumulou muitas identificações de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**tipo de logon de erro \_ \_ \_ não \_ concedido**</span><span class="sxs-lookup"><span data-stu-id="48675-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="48675-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="48675-371">Falha de logon: o usuário não recebeu o tipo de logon solicitado neste computador.</span><span class="sxs-lookup"><span data-stu-id="48675-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERRO \_ de \_ criptografia cruzada do NT \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="48675-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="48675-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-374">Uma senha com criptografia cruzada é necessária para alterar uma senha de usuário.</span><span class="sxs-lookup"><span data-stu-id="48675-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**\_não há \_ tal \_ membro**</span><span class="sxs-lookup"><span data-stu-id="48675-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="48675-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-377">Um membro não pôde ser adicionado ou removido do grupo local porque o membro não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**\_membro inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="48675-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-380">Não foi possível adicionar um novo membro a um grupo local porque o membro tem o tipo de conta incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERRO em excesso de \_ \_ \_ SIDs**</span><span class="sxs-lookup"><span data-stu-id="48675-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="48675-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-383">Foram especificadas muitas IDs de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERRO \_ de \_ criptografia cruzada de LM \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="48675-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="48675-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-386">Uma senha com criptografia cruzada é necessária para alterar essa senha de usuário.</span><span class="sxs-lookup"><span data-stu-id="48675-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERRO \_ sem \_ herança**</span><span class="sxs-lookup"><span data-stu-id="48675-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-388">1391 (0x56F)</span><span class="sxs-lookup"><span data-stu-id="48675-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-389">Indica que uma ACL não contém componentes herdáveis.</span><span class="sxs-lookup"><span data-stu-id="48675-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**arquivo de erro \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="48675-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="48675-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="48675-392">O arquivo ou diretório está corrompido e ilegível.</span><span class="sxs-lookup"><span data-stu-id="48675-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**disco de erro \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="48675-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="48675-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="48675-395">A estrutura do disco está corrompida e ilegível.</span><span class="sxs-lookup"><span data-stu-id="48675-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERRO \_ sem \_ \_ chave de sessão de usuário \_**</span><span class="sxs-lookup"><span data-stu-id="48675-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="48675-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="48675-398">Não há nenhuma chave de sessão de usuário para a sessão de logon especificada.</span><span class="sxs-lookup"><span data-stu-id="48675-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**cota de licença de erro \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="48675-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="48675-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="48675-401">O serviço que está sendo acessado é licenciado para um determinado número de conexões.</span><span class="sxs-lookup"><span data-stu-id="48675-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="48675-402">Não é possível fazer mais conexões com o serviço no momento porque já existem tantas conexões quantas o serviço pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="48675-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERRO \_ de \_ nome de destino incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="48675-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="48675-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="48675-405">O nome da conta de destino está incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERRO \_ de \_ autenticação mútua \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="48675-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="48675-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="48675-408">Falha na autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="48675-408">Mutual Authentication failed.</span></span> <span data-ttu-id="48675-409">A senha do servidor está desatualizada no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="48675-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**distorção de tempo de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="48675-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="48675-412">Há uma diferença de hora e/ou data entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="48675-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERRO \_ \_ domínio atual \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="48675-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="48675-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="48675-415">Esta operação não pode ser executada no domínio atual.</span><span class="sxs-lookup"><span data-stu-id="48675-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERRO \_ de \_ identificador de janela inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="48675-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="48675-418">Identificador de janela inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERRO \_ de \_ identificador de menu inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="48675-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="48675-421">Identificador de menu inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERRO \_ de \_ identificador de cursor inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="48675-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-424">Identificador de cursor inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERRO \_ \_ identificador de da aceleração extra inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="48675-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-427">Identificador de tabela de acelerador inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERRO \_ de \_ identificador de gancho inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-429">1404 (0x57C)</span><span class="sxs-lookup"><span data-stu-id="48675-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-430">Identificador de gancho inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERRO \_ de \_ identificador DWP inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="48675-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-433">Identificador inválido para uma estrutura de posição de várias janelas.</span><span class="sxs-lookup"><span data-stu-id="48675-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERRO \_ TLW \_ com \_ WSCHILD**</span><span class="sxs-lookup"><span data-stu-id="48675-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-435">1406 (0x57E)</span><span class="sxs-lookup"><span data-stu-id="48675-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-436">Não é possível criar uma janela filho de nível superior.</span><span class="sxs-lookup"><span data-stu-id="48675-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERRO \_ não é possível \_ localizar a \_ \_ classe WND**</span><span class="sxs-lookup"><span data-stu-id="48675-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-438">1407 (0x57F)</span><span class="sxs-lookup"><span data-stu-id="48675-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-439">Não é possível localizar a classe Window.</span><span class="sxs-lookup"><span data-stu-id="48675-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_janela \_ de erro de \_ outro \_ thread**</span><span class="sxs-lookup"><span data-stu-id="48675-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="48675-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="48675-442">Janela inválida; Ele pertence a outro thread.</span><span class="sxs-lookup"><span data-stu-id="48675-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERRO de \_ tecla de atalho \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="48675-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-444">1409 (0x581)</span><span class="sxs-lookup"><span data-stu-id="48675-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="48675-445">A tecla de acesso já está registrada.</span><span class="sxs-lookup"><span data-stu-id="48675-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**a \_ classe de erro \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="48675-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="48675-448">A classe já existe.</span><span class="sxs-lookup"><span data-stu-id="48675-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**a classe de erro não \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="48675-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="48675-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="48675-451">A classe não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**classe de erro \_ \_ tem \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="48675-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="48675-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="48675-454">A classe ainda tem janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="48675-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERRO \_ de \_ índice inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="48675-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="48675-457">Índice inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERRO \_ \_ identificador de ícone inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="48675-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="48675-460">Identificador de ícone inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERRO \_ de \_ índice de caixa de diálogo particular \_**</span><span class="sxs-lookup"><span data-stu-id="48675-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="48675-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="48675-463">Usando palavras de janela de caixa de diálogo particulares.</span><span class="sxs-lookup"><span data-stu-id="48675-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ID da caixa de listagem de erro \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="48675-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="48675-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="48675-466">O identificador da caixa de listagem não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="48675-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERRO \_ nenhum caractere \_ curinga \_**</span><span class="sxs-lookup"><span data-stu-id="48675-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="48675-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="48675-469">Nenhum caractere curinga foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="48675-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**área de transferência de erro \_ \_ não \_ aberta**</span><span class="sxs-lookup"><span data-stu-id="48675-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-471">1418 (0x58A)</span><span class="sxs-lookup"><span data-stu-id="48675-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-472">O thread não tem uma área de transferência aberta.</span><span class="sxs-lookup"><span data-stu-id="48675-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERRO de \_ tecla de atalho \_ não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="48675-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-474">1419 (0x58B)</span><span class="sxs-lookup"><span data-stu-id="48675-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-475">A tecla de acesso não está registrada.</span><span class="sxs-lookup"><span data-stu-id="48675-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**janela de erro \_ \_ não \_ caixa de diálogo**</span><span class="sxs-lookup"><span data-stu-id="48675-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-477">1420 (0x58C)</span><span class="sxs-lookup"><span data-stu-id="48675-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-478">A janela não é uma janela de diálogo válida.</span><span class="sxs-lookup"><span data-stu-id="48675-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ID de controle de erro \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="48675-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-480">1421 (0x58D)</span><span class="sxs-lookup"><span data-stu-id="48675-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-481">ID de controle não encontrada.</span><span class="sxs-lookup"><span data-stu-id="48675-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERRO \_ \_ mensagem de ComboBox inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-483">1422 (0x58E)</span><span class="sxs-lookup"><span data-stu-id="48675-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-484">Mensagem inválida para uma caixa de combinação porque não tem um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="48675-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**janela de erro \_ \_ sem \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="48675-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-486">1423 (0x58F)</span><span class="sxs-lookup"><span data-stu-id="48675-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-487">A janela não é uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="48675-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERRO \_ de \_ edição de \_ altura inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="48675-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="48675-490">A altura deve ser menor que 256.</span><span class="sxs-lookup"><span data-stu-id="48675-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERRO de \_ DC \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="48675-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="48675-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="48675-493">Identificador de contexto de dispositivo (DC) inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERRO \_ de \_ filtro de gancho inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="48675-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="48675-496">Tipo de procedimento de Hook inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERRO \_ \_ procedimento de filtro inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="48675-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="48675-499">Procedimento de gancho inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**o \_ gancho de erro \_ precisa de \_ HMOD**</span><span class="sxs-lookup"><span data-stu-id="48675-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="48675-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="48675-502">Não é possível definir um gancho não local sem um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="48675-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_ \_ somente gancho global \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="48675-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="48675-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="48675-505">Esse procedimento de gancho só pode ser definido globalmente.</span><span class="sxs-lookup"><span data-stu-id="48675-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_conjunto de \_ ganchos do diário de erros \_**</span><span class="sxs-lookup"><span data-stu-id="48675-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="48675-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="48675-508">O procedimento de gancho de diário já está instalado.</span><span class="sxs-lookup"><span data-stu-id="48675-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**gancho de erro \_ \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="48675-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="48675-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="48675-511">O procedimento de gancho não está instalado.</span><span class="sxs-lookup"><span data-stu-id="48675-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERRO \_ de \_ mensagem lb inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="48675-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="48675-514">Mensagem inválida para caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="48675-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERRO \_ SetCount \_ em \_ lb insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="48675-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="48675-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="48675-517">\_Contagem de lb para a caixa de listagem não Lazy enviada.</span><span class="sxs-lookup"><span data-stu-id="48675-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERRO \_ lb \_ sem \_ TabStops**</span><span class="sxs-lookup"><span data-stu-id="48675-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-519">1434 (0x59A)</span><span class="sxs-lookup"><span data-stu-id="48675-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-520">Esta caixa de listagem não dá suporte para paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="48675-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERRO \_ destruir \_ objeto \_ de \_ outro \_ thread**</span><span class="sxs-lookup"><span data-stu-id="48675-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-522">1435 (0x59B)</span><span class="sxs-lookup"><span data-stu-id="48675-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-523">Não é possível destruir o objeto criado por outro thread.</span><span class="sxs-lookup"><span data-stu-id="48675-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menu da \_ janela \_ filho do erro**</span><span class="sxs-lookup"><span data-stu-id="48675-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-525">1436 (0x59C)</span><span class="sxs-lookup"><span data-stu-id="48675-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-526">Janelas filhas não podem ter menus.</span><span class="sxs-lookup"><span data-stu-id="48675-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERRO \_ nenhum \_ menu do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="48675-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-528">1437 (0x59D)</span><span class="sxs-lookup"><span data-stu-id="48675-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-529">A janela não tem um menu do sistema.</span><span class="sxs-lookup"><span data-stu-id="48675-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERRO \_ \_ estilo MSGBOX \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-531">1438 (0x59E)</span><span class="sxs-lookup"><span data-stu-id="48675-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-532">Estilo de caixa de mensagem inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERRO \_ de \_ valor SPI inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-534">1439 (0x59F)</span><span class="sxs-lookup"><span data-stu-id="48675-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-535">Parâmetro de todo o sistema (SPI \_ \* ) inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**tela de erro \_ \_ já \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="48675-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-537">1440 (0x5A0)</span><span class="sxs-lookup"><span data-stu-id="48675-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="48675-538">Tela já bloqueada.</span><span class="sxs-lookup"><span data-stu-id="48675-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**os \_ HWNDs de erro \_ têm o \_ \_ pai diff**</span><span class="sxs-lookup"><span data-stu-id="48675-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-540">1441 (0x5A1)</span><span class="sxs-lookup"><span data-stu-id="48675-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="48675-541">Todos os identificadores para o Windows em uma estrutura de posição de várias janelas devem ter o mesmo pai.</span><span class="sxs-lookup"><span data-stu-id="48675-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERRO \_ não \_ é \_ janela filho**</span><span class="sxs-lookup"><span data-stu-id="48675-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-543">1442 (0x5A2)</span><span class="sxs-lookup"><span data-stu-id="48675-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="48675-544">A janela não é uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="48675-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERRO \_ inválido \_ do \_ comando GW**</span><span class="sxs-lookup"><span data-stu-id="48675-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-546">1443 (0x5A3)</span><span class="sxs-lookup"><span data-stu-id="48675-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="48675-547">Comando GW inválido \_ \* .</span><span class="sxs-lookup"><span data-stu-id="48675-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERRO \_ \_ ID de thread inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-549">1444 (0x5A4)</span><span class="sxs-lookup"><span data-stu-id="48675-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="48675-550">Identificador de thread inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERRO \_ de \_ janela não MDICHILD \_**</span><span class="sxs-lookup"><span data-stu-id="48675-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-552">1445 (0x5A5)</span><span class="sxs-lookup"><span data-stu-id="48675-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="48675-553">Não é possível processar uma mensagem de uma janela que não seja uma janela de interface de vários documentos (MDI).</span><span class="sxs-lookup"><span data-stu-id="48675-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_pop-up de erro \_ já \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="48675-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-555">1446 (0x5A6)</span><span class="sxs-lookup"><span data-stu-id="48675-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="48675-556">O menu pop-up já está ativo.</span><span class="sxs-lookup"><span data-stu-id="48675-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERRO \_ sem \_ barras de rolagem**</span><span class="sxs-lookup"><span data-stu-id="48675-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-558">1447 (0x5A7)</span><span class="sxs-lookup"><span data-stu-id="48675-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="48675-559">A janela não tem barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="48675-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERRO \_ de \_ intervalo de barra de rolagem inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-561">1448 (0x5A8)</span><span class="sxs-lookup"><span data-stu-id="48675-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="48675-562">O intervalo da barra de rolagem não pode ser maior que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="48675-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERRO \_ de \_ comando SHOWWIN inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-564">1449 (0x5A9)</span><span class="sxs-lookup"><span data-stu-id="48675-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="48675-565">Não é possível mostrar ou remover a janela da maneira especificada.</span><span class="sxs-lookup"><span data-stu-id="48675-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERRO \_ sem \_ recursos do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="48675-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-567">1450 (0x5AA)</span><span class="sxs-lookup"><span data-stu-id="48675-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="48675-568">Existem recursos do sistema insuficientes para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERRO de \_ recursos do \_ sistema não paginável \_**</span><span class="sxs-lookup"><span data-stu-id="48675-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-570">1451 (0x5AB)</span><span class="sxs-lookup"><span data-stu-id="48675-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="48675-571">Existem recursos do sistema insuficientes para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERRO na \_ paginação de \_ recursos do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="48675-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-573">1452 (0x5AC)</span><span class="sxs-lookup"><span data-stu-id="48675-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="48675-574">Existem recursos do sistema insuficientes para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERRO \_ de \_ cota de conjunto de trabalho \_**</span><span class="sxs-lookup"><span data-stu-id="48675-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-576">1453 (0x5AD)</span><span class="sxs-lookup"><span data-stu-id="48675-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="48675-577">Cota insuficiente para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**\_cota de arquivo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-579">1454 (0x5AE)</span><span class="sxs-lookup"><span data-stu-id="48675-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="48675-580">Cota insuficiente para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_limite de compromisso de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-582">1455 (0x5AF)</span><span class="sxs-lookup"><span data-stu-id="48675-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="48675-583">O arquivo de paginação é muito pequeno para que esta operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="48675-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ITEM de menu de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="48675-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-585">1456 (0x5B0)</span><span class="sxs-lookup"><span data-stu-id="48675-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="48675-586">Um item de menu não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="48675-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERRO \_ de \_ identificador de teclado inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-588">1457 (0x5B1)</span><span class="sxs-lookup"><span data-stu-id="48675-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="48675-589">Identificador de layout de teclado inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**tipo de gancho de erro \_ \_ \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="48675-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-591">1458 (0x5B2)</span><span class="sxs-lookup"><span data-stu-id="48675-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="48675-592">Tipo de gancho não permitido.</span><span class="sxs-lookup"><span data-stu-id="48675-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERRO \_ requer \_ \_ WINDOWSTATION interativo**</span><span class="sxs-lookup"><span data-stu-id="48675-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-594">1459 (0x5B3)</span><span class="sxs-lookup"><span data-stu-id="48675-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="48675-595">Esta operação requer uma estação de janela interativa.</span><span class="sxs-lookup"><span data-stu-id="48675-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_tempo limite do erro**</span><span class="sxs-lookup"><span data-stu-id="48675-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-597">1460 (0x5B4)</span><span class="sxs-lookup"><span data-stu-id="48675-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="48675-598">Esta operação foi retornada porque o período de tempo limite expirou.</span><span class="sxs-lookup"><span data-stu-id="48675-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERRO \_ de \_ identificador de monitor inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-600">1461 (0x5B5)</span><span class="sxs-lookup"><span data-stu-id="48675-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="48675-601">Identificador de monitor inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**\_Tamanho incorreto do erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-603">1462 (0x5B6)</span><span class="sxs-lookup"><span data-stu-id="48675-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="48675-604">Argumento de tamanho incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERRO \_ de \_ classe SYMLINK \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="48675-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-606">1463 (0x5B7)</span><span class="sxs-lookup"><span data-stu-id="48675-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="48675-607">O link simbólico não pode ser seguido porque seu tipo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48675-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERRO \_ SYMLINK \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="48675-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-609">1464 (0x5B8)</span><span class="sxs-lookup"><span data-stu-id="48675-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="48675-610">Este aplicativo não oferece suporte à operação atual em links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="48675-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**erro de \_ análise de XML de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-612">1465 (0x5B9)</span><span class="sxs-lookup"><span data-stu-id="48675-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="48675-613">O Windows não pôde analisar os dados XML solicitados.</span><span class="sxs-lookup"><span data-stu-id="48675-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**erro \_ XMLDSIG \_**</span><span class="sxs-lookup"><span data-stu-id="48675-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-615">1466 (0x5BA)</span><span class="sxs-lookup"><span data-stu-id="48675-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="48675-616">Foi encontrado um erro ao processar uma assinatura digital XML.</span><span class="sxs-lookup"><span data-stu-id="48675-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERRO ao \_ reiniciar o \_ aplicativo**</span><span class="sxs-lookup"><span data-stu-id="48675-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-618">1467 (0x5BB)</span><span class="sxs-lookup"><span data-stu-id="48675-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="48675-619">Esse aplicativo deve ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="48675-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**\_compartimento errado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-621">1468 (0x5BC)</span><span class="sxs-lookup"><span data-stu-id="48675-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="48675-622">O chamador fez a solicitação de conexão no compartimento de roteamento incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERRO de \_ AUTHIP da \_ falha**</span><span class="sxs-lookup"><span data-stu-id="48675-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-624">1469 (0x5BD)</span><span class="sxs-lookup"><span data-stu-id="48675-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="48675-625">Houve uma falha de AuthIP ao tentar se conectar ao host remoto.</span><span class="sxs-lookup"><span data-stu-id="48675-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERRO \_ nenhum \_ recurso de NVRAM \_**</span><span class="sxs-lookup"><span data-stu-id="48675-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-627">1470 (0x5BE)</span><span class="sxs-lookup"><span data-stu-id="48675-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="48675-628">Existem recursos de NVRAM insuficientes para concluir o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="48675-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="48675-629">Uma reinicialização pode ser necessária.</span><span class="sxs-lookup"><span data-stu-id="48675-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERRO \_ não \_ processo de GUI \_**</span><span class="sxs-lookup"><span data-stu-id="48675-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-631">1471 (0x5BF)</span><span class="sxs-lookup"><span data-stu-id="48675-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="48675-632">Não é possível concluir a operação solicitada porque o processo especificado não é um processo de GUI.</span><span class="sxs-lookup"><span data-stu-id="48675-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERRO \_ de \_ arquivo EventLog \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="48675-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-634">1500 (0x5DC)</span><span class="sxs-lookup"><span data-stu-id="48675-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="48675-635">O arquivo de log de eventos está corrompido.</span><span class="sxs-lookup"><span data-stu-id="48675-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERRO \_ EventLog não \_ consegue \_ Iniciar**</span><span class="sxs-lookup"><span data-stu-id="48675-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-637">1501 (0x5DD)</span><span class="sxs-lookup"><span data-stu-id="48675-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="48675-638">Nenhum arquivo de log de eventos pôde ser aberto, portanto, o serviço de log de eventos não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="48675-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**arquivo de log de erros \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="48675-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-640">1502 (0x5DE)</span><span class="sxs-lookup"><span data-stu-id="48675-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="48675-641">O arquivo de log de eventos está cheio.</span><span class="sxs-lookup"><span data-stu-id="48675-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERRO \_ de \_ arquivo EventLog \_ alterado**</span><span class="sxs-lookup"><span data-stu-id="48675-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-643">1503 (0x5DF)</span><span class="sxs-lookup"><span data-stu-id="48675-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="48675-644">O arquivo de log de eventos foi alterado entre operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="48675-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**nome da tarefa de erro \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="48675-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-647">O nome de tarefa especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERRO \_ de \_ índice de tarefa inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="48675-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-650">O índice de tarefa especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_thread \_ de erro já está \_ na \_ tarefa**</span><span class="sxs-lookup"><span data-stu-id="48675-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="48675-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="48675-653">O thread especificado já está ingressando em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="48675-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERRO \_ ao \_ instalar \_ falha do serviço**</span><span class="sxs-lookup"><span data-stu-id="48675-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="48675-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="48675-656">Não foi possível acessar o serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="48675-657">Isso pode ocorrer se o Windows Installer não estiver instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="48675-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="48675-658">Contate a equipe de suporte para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="48675-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERRO ao \_ instalar o \_ UserExit**</span><span class="sxs-lookup"><span data-stu-id="48675-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="48675-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="48675-661">O usuário cancelou a instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**\_falha na instalação do erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="48675-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="48675-664">Erro fatal durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERRO ao \_ instalar \_ suspensão**</span><span class="sxs-lookup"><span data-stu-id="48675-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="48675-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="48675-667">Instalação suspensa, incompleta.</span><span class="sxs-lookup"><span data-stu-id="48675-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERRO \_ de \_ produto desconhecido**</span><span class="sxs-lookup"><span data-stu-id="48675-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="48675-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="48675-670">Esta ação só é válida para produtos que estão instalados no momento.</span><span class="sxs-lookup"><span data-stu-id="48675-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERRO \_ desconhecido \_ recurso**</span><span class="sxs-lookup"><span data-stu-id="48675-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="48675-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="48675-673">ID do recurso não registrada.</span><span class="sxs-lookup"><span data-stu-id="48675-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERRO \_ de \_ componente desconhecido**</span><span class="sxs-lookup"><span data-stu-id="48675-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="48675-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="48675-676">ID do componente não registrada.</span><span class="sxs-lookup"><span data-stu-id="48675-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERRO \_ de \_ Propriedade desconhecida**</span><span class="sxs-lookup"><span data-stu-id="48675-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="48675-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="48675-679">Propriedade desconhecida.</span><span class="sxs-lookup"><span data-stu-id="48675-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERRO \_ de \_ identificador de \_ estado inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="48675-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="48675-682">O identificador está em um estado inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERRO \_ de \_ configuração incorreta**</span><span class="sxs-lookup"><span data-stu-id="48675-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-684">1610 (0x64A)</span><span class="sxs-lookup"><span data-stu-id="48675-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-685">Os dados de configuração deste produto estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="48675-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="48675-686">Contate a equipe de suporte.</span><span class="sxs-lookup"><span data-stu-id="48675-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**índice de erro \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="48675-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-688">1611 (0x64B)</span><span class="sxs-lookup"><span data-stu-id="48675-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-689">Qualificador de componente não presente.</span><span class="sxs-lookup"><span data-stu-id="48675-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERRO \_ de \_ origem de instalação \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="48675-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-691">1612 (0x64C)</span><span class="sxs-lookup"><span data-stu-id="48675-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-692">A origem da instalação para este produto não está disponível.</span><span class="sxs-lookup"><span data-stu-id="48675-692">The installation source for this product is not available.</span></span> <span data-ttu-id="48675-693">Verifique se a origem existe e se você pode acessá-la.</span><span class="sxs-lookup"><span data-stu-id="48675-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERRO ao \_ instalar a \_ versão do pacote \_**</span><span class="sxs-lookup"><span data-stu-id="48675-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-695">1613 (0x64D)</span><span class="sxs-lookup"><span data-stu-id="48675-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-696">Este pacote de instalação não pode ser instalado pelo serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="48675-697">Você deve instalar um service pack do Windows que contenha uma versão mais recente do serviço Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**produto de erro \_ \_ desinstalado**</span><span class="sxs-lookup"><span data-stu-id="48675-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-699">1614 (0x64E)</span><span class="sxs-lookup"><span data-stu-id="48675-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-700">O produto será desinstalado.</span><span class="sxs-lookup"><span data-stu-id="48675-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERRO \_ de \_ sintaxe de consulta inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="48675-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-702">1615 (0x64F)</span><span class="sxs-lookup"><span data-stu-id="48675-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-703">Sintaxe de consulta SQL inválida ou sem suporte.</span><span class="sxs-lookup"><span data-stu-id="48675-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**campo de erro \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="48675-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="48675-706">O campo de registro não existe.</span><span class="sxs-lookup"><span data-stu-id="48675-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**dispositivo de erro \_ \_ removido**</span><span class="sxs-lookup"><span data-stu-id="48675-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="48675-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="48675-709">O dispositivo foi removido.</span><span class="sxs-lookup"><span data-stu-id="48675-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERRO de \_ instalação \_ já \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="48675-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="48675-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="48675-712">Outra instalação já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="48675-712">Another installation is already in progress.</span></span> <span data-ttu-id="48675-713">Conclua essa instalação antes de prosseguir com esta instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERRO \_ \_ falha ao \_ abrir o pacote de instalação \_**</span><span class="sxs-lookup"><span data-stu-id="48675-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="48675-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="48675-716">Não foi possível abrir este pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-716">This installation package could not be opened.</span></span> <span data-ttu-id="48675-717">Verifique se o pacote existe e se você pode acessá-lo ou contate o fornecedor do aplicativo para verificar se esse é um pacote de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="48675-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERRO ao \_ instalar o \_ pacote \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="48675-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="48675-720">Não foi possível abrir este pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-720">This installation package could not be opened.</span></span> <span data-ttu-id="48675-721">Contate o fornecedor do aplicativo para verificar se este é um pacote de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="48675-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERRO ao \_ instalar \_ falha da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="48675-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="48675-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="48675-724">Erro ao iniciar a interface do usuário do serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="48675-725">Contate a equipe de suporte.</span><span class="sxs-lookup"><span data-stu-id="48675-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERRO \_ ao \_ instalar \_ falha no log**</span><span class="sxs-lookup"><span data-stu-id="48675-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="48675-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="48675-728">Erro ao abrir o arquivo de log de instalação.</span><span class="sxs-lookup"><span data-stu-id="48675-728">Error opening installation log file.</span></span> <span data-ttu-id="48675-729">Verifique se o local do arquivo de log especificado existe e se você pode gravar nele.</span><span class="sxs-lookup"><span data-stu-id="48675-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERRO ao \_ instalar o \_ idioma \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="48675-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="48675-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="48675-732">O idioma deste pacote de instalação não é suportado pelo seu sistema.</span><span class="sxs-lookup"><span data-stu-id="48675-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERRO ao \_ instalar a \_ falha de transformação \_**</span><span class="sxs-lookup"><span data-stu-id="48675-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="48675-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="48675-735">Erro ao aplicar transformações.</span><span class="sxs-lookup"><span data-stu-id="48675-735">Error applying transforms.</span></span> <span data-ttu-id="48675-736">Verifique se os caminhos de transformação especificados são válidos.</span><span class="sxs-lookup"><span data-stu-id="48675-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERRO ao \_ instalar \_ pacote \_ rejeitado**</span><span class="sxs-lookup"><span data-stu-id="48675-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="48675-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="48675-739">Essa instalação é proibida pela política do sistema.</span><span class="sxs-lookup"><span data-stu-id="48675-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="48675-740">Entre em contato com o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="48675-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**função de erro \_ \_ não \_ chamada**</span><span class="sxs-lookup"><span data-stu-id="48675-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-742">1626 (0x65A)</span><span class="sxs-lookup"><span data-stu-id="48675-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-743">A função não pôde ser executada.</span><span class="sxs-lookup"><span data-stu-id="48675-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**\_falha na função de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-745">1627 (0x65B)</span><span class="sxs-lookup"><span data-stu-id="48675-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-746">A função falhou durante a execução.</span><span class="sxs-lookup"><span data-stu-id="48675-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERRO \_ de \_ tabela inválida**</span><span class="sxs-lookup"><span data-stu-id="48675-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-748">1628 (0x65C)</span><span class="sxs-lookup"><span data-stu-id="48675-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-749">Tabela inválida ou desconhecida especificada.</span><span class="sxs-lookup"><span data-stu-id="48675-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**tipo de dados de erro \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="48675-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-751">1629 (0x65D)</span><span class="sxs-lookup"><span data-stu-id="48675-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-752">Os dados fornecidos são do tipo incorreto.</span><span class="sxs-lookup"><span data-stu-id="48675-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERRO de \_ tipo sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="48675-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-754">1630 (0x65E)</span><span class="sxs-lookup"><span data-stu-id="48675-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-755">Não há suporte para dados desse tipo.</span><span class="sxs-lookup"><span data-stu-id="48675-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**\_ \_ falha ao criar erro**</span><span class="sxs-lookup"><span data-stu-id="48675-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-757">1631 (0x65F)</span><span class="sxs-lookup"><span data-stu-id="48675-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-758">Falha ao iniciar o serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="48675-759">Contate a equipe de suporte.</span><span class="sxs-lookup"><span data-stu-id="48675-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERRO ao \_ instalar o \_ Temp não \_ gravável**</span><span class="sxs-lookup"><span data-stu-id="48675-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="48675-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="48675-762">A pasta temporária está em uma unidade que está cheia ou está inacessível.</span><span class="sxs-lookup"><span data-stu-id="48675-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="48675-763">Libere espaço na unidade ou verifique se você tem permissão de gravação na pasta Temp.</span><span class="sxs-lookup"><span data-stu-id="48675-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERRO ao \_ instalar \_ plataforma \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="48675-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="48675-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="48675-766">Este pacote de instalação não tem suporte deste tipo de processador.</span><span class="sxs-lookup"><span data-stu-id="48675-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="48675-767">Contate o fornecedor do produto.</span><span class="sxs-lookup"><span data-stu-id="48675-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERRO de \_ instalação \_ não usada**</span><span class="sxs-lookup"><span data-stu-id="48675-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="48675-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="48675-770">Componente não usado neste computador.</span><span class="sxs-lookup"><span data-stu-id="48675-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERRO \_ \_ ao abrir o pacote de patches \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48675-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="48675-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="48675-773">Não foi possível abrir este pacote de atualização.</span><span class="sxs-lookup"><span data-stu-id="48675-773">This update package could not be opened.</span></span> <span data-ttu-id="48675-774">Verifique se o pacote de atualização existe e se você pode acessá-lo ou contate o fornecedor do aplicativo para verificar se este é um pacote de atualização de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="48675-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERRO \_ de \_ pacote de patch \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="48675-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="48675-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="48675-777">Não foi possível abrir este pacote de atualização.</span><span class="sxs-lookup"><span data-stu-id="48675-777">This update package could not be opened.</span></span> <span data-ttu-id="48675-778">Contate o fornecedor do aplicativo para verificar se este é um pacote de atualização de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="48675-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**pacote de patch de erro \_ \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="48675-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="48675-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="48675-781">Este pacote de atualização não pode ser processado pelo serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="48675-782">Você deve instalar um service pack do Windows que contenha uma versão mais recente do serviço Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48675-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_versão do produto de erro \_**</span><span class="sxs-lookup"><span data-stu-id="48675-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="48675-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="48675-785">Outra versão deste produto já está instalada.</span><span class="sxs-lookup"><span data-stu-id="48675-785">Another version of this product is already installed.</span></span> <span data-ttu-id="48675-786">Não é possível continuar a instalação desta versão.</span><span class="sxs-lookup"><span data-stu-id="48675-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="48675-787">Para configurar ou remover a versão existente deste produto, use adicionar/remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="48675-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERRO \_ de \_ linha de comando inválida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="48675-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="48675-790">Argumento de linha de comando inválido.</span><span class="sxs-lookup"><span data-stu-id="48675-790">Invalid command line argument.</span></span> <span data-ttu-id="48675-791">Consulte o SDK do Windows Installer para obter ajuda de linha de comando detalhada.</span><span class="sxs-lookup"><span data-stu-id="48675-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERRO ao \_ instalar \_ remoto não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="48675-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="48675-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="48675-794">Somente os administradores têm permissão para adicionar, remover ou configurar o software do servidor durante uma sessão remota dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="48675-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="48675-795">Se você quiser instalar ou configurar o software no servidor, entre em contato com o administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="48675-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERRO \_ de \_ reinicialização de êxito \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="48675-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="48675-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="48675-798">A operação solicitada foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="48675-798">The requested operation completed successfully.</span></span> <span data-ttu-id="48675-799">O sistema será reiniciado para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="48675-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERRO \_ de \_ destino de patch \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="48675-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-801">1642 (0x66A)</span><span class="sxs-lookup"><span data-stu-id="48675-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="48675-802">A atualização não pode ser instalada pelo serviço de Windows Installer porque o programa a ser atualizado pode estar ausente ou a atualização pode atualizar uma versão diferente do programa.</span><span class="sxs-lookup"><span data-stu-id="48675-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="48675-803">Verifique se o programa a ser atualizado existe no computador e se você tem a atualização correta.</span><span class="sxs-lookup"><span data-stu-id="48675-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERRO \_ de \_ pacote de patch \_ rejeitado**</span><span class="sxs-lookup"><span data-stu-id="48675-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-805">1643 (0x66B)</span><span class="sxs-lookup"><span data-stu-id="48675-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="48675-806">O pacote de atualização não é permitido pela política de restrição de software.</span><span class="sxs-lookup"><span data-stu-id="48675-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERRO ao \_ instalar a \_ transformação \_ rejeitada**</span><span class="sxs-lookup"><span data-stu-id="48675-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-808">1644 (0x66C)</span><span class="sxs-lookup"><span data-stu-id="48675-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="48675-809">Uma ou mais personalizações não são permitidas pela política de restrição de software.</span><span class="sxs-lookup"><span data-stu-id="48675-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERRO ao \_ instalar \_ remoto \_ proibido**</span><span class="sxs-lookup"><span data-stu-id="48675-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="48675-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="48675-812">O Windows Installer não permite a instalação de um Conexão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48675-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**remoção de patch de erro \_ \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="48675-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="48675-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="48675-815">Não há suporte para a desinstalação do pacote de atualização.</span><span class="sxs-lookup"><span data-stu-id="48675-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERRO \_ de \_ patch desconhecido**</span><span class="sxs-lookup"><span data-stu-id="48675-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-817">1647 (0x66F)</span><span class="sxs-lookup"><span data-stu-id="48675-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="48675-818">A atualização não é aplicada a este produto.</span><span class="sxs-lookup"><span data-stu-id="48675-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**PATCH de erro \_ \_ sem \_ sequência**</span><span class="sxs-lookup"><span data-stu-id="48675-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="48675-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="48675-821">Nenhuma sequência válida foi encontrada para o conjunto de atualizações.</span><span class="sxs-lookup"><span data-stu-id="48675-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**remoção de patch de erro não \_ \_ \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="48675-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="48675-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="48675-824">A remoção da atualização não foi permitida pela política.</span><span class="sxs-lookup"><span data-stu-id="48675-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERRO \_ \_ XML de patch inválido \_**</span><span class="sxs-lookup"><span data-stu-id="48675-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="48675-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="48675-827">Os dados de atualização XML são inválidos.</span><span class="sxs-lookup"><span data-stu-id="48675-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERRO \_ de \_ \_ produto anunciado gerenciado por patch \_**</span><span class="sxs-lookup"><span data-stu-id="48675-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="48675-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="48675-830">Windows Installer não permite a atualização de produtos anunciados gerenciados.</span><span class="sxs-lookup"><span data-stu-id="48675-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="48675-831">Pelo menos um recurso do produto deve ser instalado antes da aplicação da atualização.</span><span class="sxs-lookup"><span data-stu-id="48675-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERRO ao \_ instalar o \_ serviço de \_ inicialização segura**</span><span class="sxs-lookup"><span data-stu-id="48675-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="48675-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="48675-834">O serviço de Windows Installer não está acessível no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="48675-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="48675-835">Tente novamente quando o computador não estiver no modo de segurança ou você pode usar a restauração do sistema para retornar o computador a um estado bom anterior.</span><span class="sxs-lookup"><span data-stu-id="48675-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**exceção de erro com \_ falha \_ rápida \_**</span><span class="sxs-lookup"><span data-stu-id="48675-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="48675-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="48675-838">Ocorreu uma exceção fail fast.</span><span class="sxs-lookup"><span data-stu-id="48675-838">A fail fast exception occurred.</span></span> <span data-ttu-id="48675-839">Os manipuladores de exceção não serão invocados e o processo será encerrado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="48675-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48675-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**instalação de erro \_ \_ rejeitada**</span><span class="sxs-lookup"><span data-stu-id="48675-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48675-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="48675-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="48675-842">O aplicativo que você está tentando executar não tem suporte nesta versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="48675-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48675-843">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48675-843">Requirements</span></span>



| <span data-ttu-id="48675-844">Requisito</span><span class="sxs-lookup"><span data-stu-id="48675-844">Requirement</span></span> | <span data-ttu-id="48675-845">Valor</span><span class="sxs-lookup"><span data-stu-id="48675-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48675-846">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48675-846">Minimum supported client</span></span><br/> | <span data-ttu-id="48675-847">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="48675-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48675-848">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48675-848">Minimum supported server</span></span><br/> | <span data-ttu-id="48675-849">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48675-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48675-850">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48675-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="48675-851"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="48675-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48675-852">Confira também</span><span class="sxs-lookup"><span data-stu-id="48675-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48675-853">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="48675-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




