---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: Função falha AcquireCredentialsHandle (geral) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769655"
---
# <a name="acquirecredentialshandle-general-function"></a><span data-ttu-id="bbaa4-103">Função falha AcquireCredentialsHandle (geral)</span><span class="sxs-lookup"><span data-stu-id="bbaa4-103">AcquireCredentialsHandle (General) function</span></span>

<span data-ttu-id="bbaa4-104">A função **falha AcquireCredentialsHandle (geral)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-104">The **AcquireCredentialsHandle (General)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bbaa4-105">Esse identificador é exigido pelas funções [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) e [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-105">This handle is required by the [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) and [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) functions.</span></span> <span data-ttu-id="bbaa4-106">Elas podem ser credenciais preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-106">These can be either preexisting credentials, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="bbaa4-107">Isso não é um "logon na rede" e não implica a coleta de credenciais.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

<span data-ttu-id="bbaa4-108">Para obter informações sobre como usar essa função com um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) específico, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-108">For information about using this function with a specific [*security support provider*](../secgloss/s-gly.md) (SSP), see the following topics.</span></span>



| <span data-ttu-id="bbaa4-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="bbaa4-109">Topic</span></span>                                                                                           | <span data-ttu-id="bbaa4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbaa4-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbaa4-111">**Falha AcquireCredentialsHandle (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-111">**AcquireCredentialsHandle (CredSSP)**</span></span>](acquirecredentialshandle--credssp.md)<br/>     | <span data-ttu-id="bbaa4-112">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que usa o Credential Security Support Provider (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-112">Acquires a handle to preexisting credentials of a security principal that is using Credential Security Support Provider (CredSSP).</span></span><br/> |
| [<span data-ttu-id="bbaa4-113">**Falha AcquireCredentialsHandle (resumo)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-113">**AcquireCredentialsHandle (Digest)**</span></span>](acquirecredentialshandle--digest.md)<br/>       | <span data-ttu-id="bbaa4-114">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando o Digest.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-114">Acquires a handle to preexisting credentials of a security principal that is using Digest.</span></span><br/>                                         |
| [<span data-ttu-id="bbaa4-115">**Falha AcquireCredentialsHandle (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-115">**AcquireCredentialsHandle (Kerberos)**</span></span>](acquirecredentialshandle--kerberos.md)<br/>   | <span data-ttu-id="bbaa4-116">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que esteja usando Kerberos.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-116">Acquires a handle to preexisting credentials of a security principal that is using Kerberos.</span></span><br/>                                       |
| [<span data-ttu-id="bbaa4-117">**Falha AcquireCredentialsHandle (negociar)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-117">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)<br/> | <span data-ttu-id="bbaa4-118">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando Negotiate.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-118">Acquires a handle to preexisting credentials of a security principal that is using Negotiate.</span></span><br/>                                      |
| [<span data-ttu-id="bbaa4-119">**Falha AcquireCredentialsHandle (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-119">**AcquireCredentialsHandle (NTLM)**</span></span>](acquirecredentialshandle--ntlm.md)<br/>           | <span data-ttu-id="bbaa4-120">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando NTLM.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-120">Acquires a handle to preexisting credentials of a security principal that is using NTLM.</span></span><br/>                                           |
| [<span data-ttu-id="bbaa4-121">**Falha AcquireCredentialsHandle (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-121">**AcquireCredentialsHandle (Schannel)**</span></span>](acquirecredentialshandle--schannel.md)<br/>   | <span data-ttu-id="bbaa4-122">Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando Schannel.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-122">Acquires a handle to preexisting credentials of a security principal that is using Schannel.</span></span><br/>                                       |



 

## <a name="syntax"></a><span data-ttu-id="bbaa4-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbaa4-123">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bbaa4-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbaa4-124">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbaa4-125">*pszPrincipal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-125">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-126">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-126">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="bbaa4-127">Ao usar o SSP de resumo, esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-127">When using the Digest SSP, this parameter is optional.</span></span>

<span data-ttu-id="bbaa4-128">Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-128">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="bbaa4-129">Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-129">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="bbaa4-130">Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-130">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="bbaa4-131">*pszPackage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-131">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-132">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-132">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="bbaa4-133">Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-133">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="bbaa4-134">Depois que um contexto é estabelecido, [**QueryContextAttributes (geral)**](querycontextattributes--general.md) pode ser chamado com *ULATTRIBUTE* definido como \_ SECPKG \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-134">After a context is established, [**QueryContextAttributes (General)**](querycontextattributes--general.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="bbaa4-135">Ao usar o SSP de resumo, defina esse parâmetro como WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-135">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

<span data-ttu-id="bbaa4-136">Ao usar o SSP do Schannel, defina esse parâmetro como UNISP \_ nome.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-136">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-137">*fCredentialUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-137">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-138">Um sinalizador que indica como essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-138">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="bbaa4-139">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-139">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="bbaa4-140">Valor</span><span class="sxs-lookup"><span data-stu-id="bbaa4-140">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="bbaa4-141">Significado</span><span class="sxs-lookup"><span data-stu-id="bbaa4-141">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="bbaa4-142"><dt>**SECPKG \_ Credenciais \_ \_ restritas de logon automático do cred**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-142"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="bbaa4-143">A segurança não usa credenciais de logon padrão ou credenciais do [Gerenciador de credenciais](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-143">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="bbaa4-144">Esse valor só tem suporte pela [*delegação restrita*](../secgloss/s-gly.md)de Negotiate.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-144">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="bbaa4-145">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-145">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="bbaa4-146"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-146"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="bbaa4-147">Valide uma credencial de entrada ou use uma credencial local para preparar um token de saída.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-147">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="bbaa4-148">Esse sinalizador habilita ambos os outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-148">This flag enables both other flags.</span></span> <span data-ttu-id="bbaa4-149">Esse sinalizador não é válido com o Digest e o Schannel SSPs.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-149">This flag is not valid with the Digest and Schannel SSPs.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="bbaa4-150"><dt>**\_entrada de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-150"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="bbaa4-151">Valide uma credencial de servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-151">Validate an incoming server credential.</span></span> <span data-ttu-id="bbaa4-152">As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) ou [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-152">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) or [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) is called.</span></span> <span data-ttu-id="bbaa4-153">Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-153">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="bbaa4-154">A validação é específica do pacote.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-154">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="bbaa4-155"><dt>**\_saída de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-155"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="bbaa4-156">Permitir que uma credencial de cliente local Prepare um token de saída.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-156">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="bbaa4-157"><dt>**SECPKG \_ Política de processo de credenciais \_ \_ \_ apenas**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-157"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="bbaa4-158">A função processa a política de servidor e retorna **s \_ e \_ nenhuma \_ credencial**, indicando que o aplicativo deve solicitar credenciais.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-158">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="bbaa4-159">Esse valor só tem suporte pela [*delegação restrita*](../secgloss/s-gly.md)de Negotiate.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-159">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="bbaa4-160">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-160">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="bbaa4-161">*pvLogonID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-161">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-162">Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-162">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="bbaa4-163">Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-163">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="bbaa4-164">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-164">This parameter can be **NULL**.</span></span>

<span data-ttu-id="bbaa4-165">Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-165">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-166">*pAuthData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-166">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-167">Um ponteiro para dados específicos do pacote.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-167">A pointer to package-specific data.</span></span> <span data-ttu-id="bbaa4-168">Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-168">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="bbaa4-169">Para usar credenciais fornecidas, passe uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que inclui essas credenciais nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-169">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="bbaa4-170">O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-170">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="bbaa4-171">Ao usar o SSP de resumo, esse parâmetro é um ponteiro para uma estrutura de identidade de autenticação do Winnt da SEC que contém informações de autenticação a serem usadas para localizar as credenciais. [**\_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)</span><span class="sxs-lookup"><span data-stu-id="bbaa4-171">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

<span data-ttu-id="bbaa4-172">Ao usar o SSP do Schannel, especifique uma estrutura de [**\_ credenciais Schannel**](/windows/win32/api/schannel/ns-schannel-schannel_cred) que indica o protocolo a ser usado e as configurações para vários recursos de canal personalizáveis.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-172">When using the Schannel SSP, specify an [**SCHANNEL\_CRED**](/windows/win32/api/schannel/ns-schannel-schannel_cred) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

<span data-ttu-id="bbaa4-173">Ao usar os pacotes NTLM ou Negotiate, os comprimentos máximos de caracteres para o nome de usuário, a senha e o domínio são 256, 256 e 15, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-173">When using the NTLM or Negotiate packages, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-174">*pGetKeyFn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-174">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-175">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-175">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-176">*pvGetKeyArgument* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-176">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-177">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-177">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-178">*phCredential* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-178">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-179">Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-179">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="bbaa4-180">*ptsExpiry* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-180">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbaa4-181">Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-181">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="bbaa4-182">O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-182">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bbaa4-183">O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-183">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="bbaa4-184">Esse parâmetro é definido como um tempo máximo de constante.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-184">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="bbaa4-185">Não há tempo de expiração para as credenciais ou s de [*contexto de segurança*](../secgloss/s-gly.md)Digest ou ao usar o SSP de resumo.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-185">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

<span data-ttu-id="bbaa4-186">Ao usar o SSP do Schannel, esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-186">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="bbaa4-187">Quando a credencial a ser usada para autenticação é um certificado, esse parâmetro recebe o tempo de expiração para esse certificado.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-187">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="bbaa4-188">Se nenhum certificado tiver sido fornecido, um valor de tempo máximo será retornado.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-188">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbaa4-189">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbaa4-189">Return value</span></span>

<span data-ttu-id="bbaa4-190">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-190">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="bbaa4-191">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-191">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="bbaa4-192">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bbaa4-192">Return code</span></span>                                                                                                 | <span data-ttu-id="bbaa4-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbaa4-193">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbaa4-194"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-194"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="bbaa4-195">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-195">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="bbaa4-196"><dt>**s \_ E \_ \_ erro interno**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-196"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="bbaa4-197">Ocorreu um erro que não foi mapeado para um código de erro SSPI.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-197">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="bbaa4-198"><dt>**s \_ E \_ sem \_ credenciais**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-198"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="bbaa4-199">Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bbaa4-199">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="bbaa4-200"><dt>**s \_ E \_ não \_ proprietário**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-200"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="bbaa4-201">O chamador da função não tem as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-201">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="bbaa4-202"><dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-202"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="bbaa4-203">O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-203">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="bbaa4-204"><dt>**s \_ E \_ credenciais desconhecidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-204"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="bbaa4-205">As credenciais fornecidas para o pacote não foram reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-205">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="bbaa4-206">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbaa4-206">Remarks</span></span>

<span data-ttu-id="bbaa4-207">A função **falha AcquireCredentialsHandle (geral)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-207">The **AcquireCredentialsHandle (General)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="bbaa4-208">Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-208">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="bbaa4-209">Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) e [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-209">This handle can be used in subsequent calls to the [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) and [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) functions.</span></span>

<span data-ttu-id="bbaa4-210">Em geral, **falha AcquireCredentialsHandle (geral)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-210">In general, **AcquireCredentialsHandle (General)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="bbaa4-211">No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-211">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="bbaa4-212">Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-212">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="bbaa4-213">Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-213">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="bbaa4-214">Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-214">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="bbaa4-215">Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="bbaa4-215">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="bbaa4-216">Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-216">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="bbaa4-217">Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.</span><span class="sxs-lookup"><span data-stu-id="bbaa4-217">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="bbaa4-218">Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="bbaa4-218">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbaa4-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbaa4-219">Requirements</span></span>



| <span data-ttu-id="bbaa4-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbaa4-220">Requirement</span></span> | <span data-ttu-id="bbaa4-221">Valor</span><span class="sxs-lookup"><span data-stu-id="bbaa4-221">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaa4-222">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbaa4-222">Minimum supported client</span></span><br/> | <span data-ttu-id="bbaa4-223">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-223">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bbaa4-224">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbaa4-224">Minimum supported server</span></span><br/> | <span data-ttu-id="bbaa4-225">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbaa4-225">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bbaa4-226">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbaa4-226">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbaa4-227"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-227"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="bbaa4-228">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbaa4-228">Library</span></span><br/>                  | <dl> <span data-ttu-id="bbaa4-229"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-229"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="bbaa4-230">DLL</span><span class="sxs-lookup"><span data-stu-id="bbaa4-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbaa4-231"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbaa4-231"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="bbaa4-232">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bbaa4-232">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bbaa4-233">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bbaa4-233">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bbaa4-234">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbaa4-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbaa4-235">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="bbaa4-235">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="bbaa4-236">**AcceptSecurityContext (geral)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-236">**AcceptSecurityContext (General)**</span></span>](acceptsecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="bbaa4-237">**InitializeSecurityContext (geral)**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-237">**InitializeSecurityContext (General)**</span></span>](initializesecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="bbaa4-238">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="bbaa4-238">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
