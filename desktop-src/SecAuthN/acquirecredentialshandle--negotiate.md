---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Função falha AcquireCredentialsHandle (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793749"
---
# <a name="acquirecredentialshandle-negotiate-function"></a><span data-ttu-id="b529a-103">Função falha AcquireCredentialsHandle (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="b529a-103">AcquireCredentialsHandle (Negotiate) function</span></span>

<span data-ttu-id="b529a-104">A função **falha AcquireCredentialsHandle (Negotiate)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b529a-104">The **AcquireCredentialsHandle (Negotiate)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b529a-105">Esse identificador é exigido pelas funções [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) e [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="b529a-105">This handle is required by the [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) and [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) functions.</span></span> <span data-ttu-id="b529a-106">Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="b529a-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="b529a-107">Isso não é um "logon na rede" e não implica a coleta de credenciais.</span><span class="sxs-lookup"><span data-stu-id="b529a-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b529a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b529a-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="b529a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b529a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b529a-110">*pszPrincipal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="b529a-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="b529a-112">Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b529a-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="b529a-113">Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="b529a-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="b529a-114">*pszPackage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="b529a-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="b529a-116">Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="b529a-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="b529a-117">Depois que um contexto é estabelecido, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) pode ser chamado com *ULATTRIBUTE* definido como SECPKG \_ \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.</span><span class="sxs-lookup"><span data-stu-id="b529a-117">After a context is established, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="b529a-118">Para chamar essa função com êxito usando o Negotiate SSP, defina esse parâmetro como "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="b529a-118">To successfully call this function using the Negotiate SSP, set this parameter to "Negotiate".</span></span>

</dd> <dt>

<span data-ttu-id="b529a-119">*fCredentialUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-119">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-120">Um sinalizador que indica como essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="b529a-120">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="b529a-121">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b529a-121">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b529a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b529a-122">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="b529a-123">Significado</span><span class="sxs-lookup"><span data-stu-id="b529a-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="b529a-124"><dt>**SECPKG \_ Credenciais \_ \_ restritas de logon automático do cred**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b529a-124"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="b529a-125">A segurança não usa credenciais de logon padrão ou credenciais do [Gerenciador de credenciais](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="b529a-125">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="b529a-126">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b529a-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="b529a-127"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-127"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="b529a-128">Valide uma credencial de entrada ou use uma credencial local para preparar um token de saída.</span><span class="sxs-lookup"><span data-stu-id="b529a-128">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="b529a-129">Esse sinalizador habilita ambos os outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="b529a-129">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="b529a-130"><dt>**\_entrada de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-130"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="b529a-131">Valide uma credencial de servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="b529a-131">Validate an incoming server credential.</span></span> <span data-ttu-id="b529a-132">As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) ou [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b529a-132">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) or [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) is called.</span></span> <span data-ttu-id="b529a-133">Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ .</span><span class="sxs-lookup"><span data-stu-id="b529a-133">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="b529a-134">A validação é específica do pacote.</span><span class="sxs-lookup"><span data-stu-id="b529a-134">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="b529a-135"><dt>**\_saída de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-135"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="b529a-136">Permitir que uma credencial de cliente local Prepare um token de saída.</span><span class="sxs-lookup"><span data-stu-id="b529a-136">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="b529a-137"><dt>**SECPKG \_ Política de processo de credenciais \_ \_ \_ apenas**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-137"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="b529a-138">A função processa a política de servidor e retorna **s \_ e \_ nenhuma \_ credencial**, indicando que o aplicativo deve solicitar credenciais.</span><span class="sxs-lookup"><span data-stu-id="b529a-138">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="b529a-139">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b529a-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="b529a-140">*pvLogonID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-140">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-141">Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="b529a-141">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="b529a-142">Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede.</span><span class="sxs-lookup"><span data-stu-id="b529a-142">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="b529a-143">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b529a-143">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-144">*pAuthData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-144">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-145">Um ponteiro para dados específicos do pacote.</span><span class="sxs-lookup"><span data-stu-id="b529a-145">A pointer to package-specific data.</span></span> <span data-ttu-id="b529a-146">Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="b529a-146">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="b529a-147">Para usar credenciais fornecidas, passe uma **estrutura \_ \_ opaca de \_ identidade \_ de autenticação WinNT PSEC** retornada de uma chamada anterior para a função [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="b529a-147">To use supplied credentials, pass a **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** structure returned from a previous call to the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function.</span></span>

<span data-ttu-id="b529a-148">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para o tipo **opaco da identidade de autenticação do PSEC \_ \_ \_ \_ WinNT** e para a função [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="b529a-148">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** The **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** type and the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function are not supported.</span></span> <span data-ttu-id="b529a-149">Para usar credenciais fornecidas, passe um ponteiro para uma [**identidade de \_ \_ autenticação do \_ WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ou a estrutura da identidade de autenticação do Winnt de s, por [**\_ \_ \_ \_ exemplo**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) , que inclui essas credenciais.</span><span class="sxs-lookup"><span data-stu-id="b529a-149">To use supplied credentials, pass a pointer to either a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) or [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) structure that includes those credentials.</span></span>

<span data-ttu-id="b529a-150">O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="b529a-150">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="b529a-151">Ao usar o pacote Negotiate, os comprimentos máximos de caracteres para o nome de usuário, a senha e o domínio são 256, 256 e 15, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b529a-151">When using the Negotiate package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-152">*pGetKeyFn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-152">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-153">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b529a-153">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-154">*pvGetKeyArgument* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b529a-154">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-155">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b529a-155">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-156">*phCredential* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b529a-156">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-157">Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="b529a-157">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="b529a-158">*ptsExpiry* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b529a-158">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b529a-159">Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram.</span><span class="sxs-lookup"><span data-stu-id="b529a-159">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="b529a-160">O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b529a-160">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b529a-161">O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.</span><span class="sxs-lookup"><span data-stu-id="b529a-161">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b529a-162">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b529a-162">Return value</span></span>

<span data-ttu-id="b529a-163">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b529a-163">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b529a-164">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="b529a-164">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="b529a-165">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b529a-165">Return code</span></span>                                                                                                 | <span data-ttu-id="b529a-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="b529a-166">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b529a-167"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-167"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="b529a-168">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="b529a-168">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="b529a-169"><dt>**s \_ E \_ \_ erro interno**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-169"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="b529a-170">Ocorreu um erro que não foi mapeado para um código de erro SSPI.</span><span class="sxs-lookup"><span data-stu-id="b529a-170">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="b529a-171"><dt>**s \_ E \_ sem \_ credenciais**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-171"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="b529a-172">Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b529a-172">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="b529a-173"><dt>**s \_ E \_ não \_ proprietário**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-173"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="b529a-174">O chamador da função não tem as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="b529a-174">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="b529a-175"><dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-175"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="b529a-176">O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.</span><span class="sxs-lookup"><span data-stu-id="b529a-176">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b529a-177"><dt>**s \_ E \_ credenciais desconhecidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-177"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="b529a-178">As credenciais fornecidas para o pacote não foram reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="b529a-178">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="b529a-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="b529a-179">Remarks</span></span>

<span data-ttu-id="b529a-180">A função **falha AcquireCredentialsHandle (Negotiate)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="b529a-180">The **AcquireCredentialsHandle (Negotiate)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b529a-181">Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="b529a-181">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="b529a-182">Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) e [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="b529a-182">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) and [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) functions.</span></span>

<span data-ttu-id="b529a-183">Em geral, **falha AcquireCredentialsHandle (Negotiate)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="b529a-183">In general, **AcquireCredentialsHandle (Negotiate)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="b529a-184">No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="b529a-184">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="b529a-185">Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b529a-185">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="b529a-186">Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="b529a-186">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="b529a-187">Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b529a-187">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="b529a-188">Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="b529a-188">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="b529a-189">Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b529a-189">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="b529a-190">Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.</span><span class="sxs-lookup"><span data-stu-id="b529a-190">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="b529a-191">Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="b529a-191">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b529a-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b529a-192">Requirements</span></span>



| <span data-ttu-id="b529a-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="b529a-193">Requirement</span></span> | <span data-ttu-id="b529a-194">Valor</span><span class="sxs-lookup"><span data-stu-id="b529a-194">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b529a-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b529a-195">Minimum supported client</span></span><br/> | <span data-ttu-id="b529a-196">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b529a-196">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b529a-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b529a-197">Minimum supported server</span></span><br/> | <span data-ttu-id="b529a-198">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b529a-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b529a-199">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b529a-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="b529a-200"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-200"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="b529a-201">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b529a-201">Library</span></span><br/>                  | <dl> <span data-ttu-id="b529a-202"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-202"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="b529a-203">DLL</span><span class="sxs-lookup"><span data-stu-id="b529a-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b529a-204"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b529a-204"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="b529a-205">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b529a-205">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b529a-206">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b529a-206">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b529a-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="b529a-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b529a-208">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="b529a-208">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="b529a-209">**AcceptSecurityContext (negociar)**</span><span class="sxs-lookup"><span data-stu-id="b529a-209">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="b529a-210">**InitializeSecurityContext (negociar)**</span><span class="sxs-lookup"><span data-stu-id="b529a-210">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="b529a-211">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="b529a-211">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
