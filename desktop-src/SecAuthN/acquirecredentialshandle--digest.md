---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando o Digest.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: Função falha AcquireCredentialsHandle (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170951"
---
# <a name="acquirecredentialshandle-digest-function"></a><span data-ttu-id="ba48d-103">Função falha AcquireCredentialsHandle (Digest)</span><span class="sxs-lookup"><span data-stu-id="ba48d-103">AcquireCredentialsHandle (Digest) function</span></span>

<span data-ttu-id="ba48d-104">A função **falha AcquireCredentialsHandle (Digest)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ba48d-104">The **AcquireCredentialsHandle (Digest)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="ba48d-105">Esse identificador é exigido pelas funções [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="ba48d-105">This handle is required by the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span> <span data-ttu-id="ba48d-106">Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="ba48d-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="ba48d-107">Isso não é um "logon na rede" e não implica a coleta de credenciais.</span><span class="sxs-lookup"><span data-stu-id="ba48d-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ba48d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba48d-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ba48d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba48d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba48d-110">*pszPrincipal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="ba48d-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="ba48d-112">Ao usar o SSP de resumo, esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ba48d-112">When using the Digest SSP, this parameter is optional.</span></span>

> [!Note]  
> <span data-ttu-id="ba48d-113">Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ba48d-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="ba48d-114">Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="ba48d-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="ba48d-115">*pszPackage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="ba48d-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="ba48d-117">Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="ba48d-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="ba48d-118">Depois que um contexto é estabelecido, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) pode ser chamado com *ULATTRIBUTE* definido como \_ SECPKG \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.</span><span class="sxs-lookup"><span data-stu-id="ba48d-118">After a context is established, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="ba48d-119">Ao usar o SSP de resumo, defina esse parâmetro como WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="ba48d-119">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-120">*fCredentialUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-121">Um sinalizador que indica como essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="ba48d-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="ba48d-122">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba48d-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ba48d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ba48d-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="ba48d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="ba48d-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="ba48d-125"><dt>**\_entrada de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="ba48d-126">Valide uma credencial de servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="ba48d-126">Validate an incoming server credential.</span></span> <span data-ttu-id="ba48d-127">As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) ou [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ba48d-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) or [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) is called.</span></span> <span data-ttu-id="ba48d-128">Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ .</span><span class="sxs-lookup"><span data-stu-id="ba48d-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="ba48d-129">A validação é específica do pacote.</span><span class="sxs-lookup"><span data-stu-id="ba48d-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="ba48d-130"><dt>**\_saída de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="ba48d-131">Permitir que uma credencial de cliente local Prepare um token de saída.</span><span class="sxs-lookup"><span data-stu-id="ba48d-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="ba48d-132">*pvLogonID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-132">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-133">Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="ba48d-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="ba48d-134">Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede.</span><span class="sxs-lookup"><span data-stu-id="ba48d-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="ba48d-135">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ba48d-135">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-136">*pAuthData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-136">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-137">Um ponteiro para dados específicos do pacote.</span><span class="sxs-lookup"><span data-stu-id="ba48d-137">A pointer to package-specific data.</span></span> <span data-ttu-id="ba48d-138">Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="ba48d-138">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="ba48d-139">Para usar credenciais fornecidas, passe uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que inclui essas credenciais nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba48d-139">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="ba48d-140">O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="ba48d-140">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="ba48d-141">Ao usar o SSP de resumo, esse parâmetro é um ponteiro para uma estrutura de identidade de autenticação do Winnt da SEC que contém informações de autenticação a serem usadas para localizar as credenciais. [**\_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)</span><span class="sxs-lookup"><span data-stu-id="ba48d-141">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-142">*pGetKeyFn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-143">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ba48d-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-144">*pvGetKeyArgument* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-145">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ba48d-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-146">*phCredential* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-147">Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="ba48d-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="ba48d-148">*ptsExpiry* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48d-149">Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram.</span><span class="sxs-lookup"><span data-stu-id="ba48d-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="ba48d-150">O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ba48d-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="ba48d-151">O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.</span><span class="sxs-lookup"><span data-stu-id="ba48d-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="ba48d-152">Esse parâmetro é definido como um tempo máximo de constante.</span><span class="sxs-lookup"><span data-stu-id="ba48d-152">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="ba48d-153">Não há tempo de expiração para as credenciais ou s de [*contexto de segurança*](../secgloss/s-gly.md)Digest ou ao usar o SSP de resumo.</span><span class="sxs-lookup"><span data-stu-id="ba48d-153">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba48d-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba48d-154">Return value</span></span>

<span data-ttu-id="ba48d-155">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba48d-155">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="ba48d-156">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="ba48d-156">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="ba48d-157">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba48d-157">Return code</span></span>                                                                                                 | <span data-ttu-id="ba48d-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba48d-158">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba48d-159"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-159"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="ba48d-160">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ba48d-160">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="ba48d-161"><dt>**s \_ E \_ \_ erro interno**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-161"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="ba48d-162">Ocorreu um erro que não foi mapeado para um código de erro SSPI.</span><span class="sxs-lookup"><span data-stu-id="ba48d-162">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="ba48d-163"><dt>**s \_ E \_ sem \_ credenciais**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-163"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="ba48d-164">Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ba48d-164">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="ba48d-165"><dt>**s \_ E \_ não \_ proprietário**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-165"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="ba48d-166">O chamador da função não tem as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="ba48d-166">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="ba48d-167"><dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-167"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="ba48d-168">O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.</span><span class="sxs-lookup"><span data-stu-id="ba48d-168">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="ba48d-169"><dt>**s \_ E \_ credenciais desconhecidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-169"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="ba48d-170">As credenciais fornecidas para o pacote não foram reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="ba48d-170">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ba48d-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba48d-171">Remarks</span></span>

<span data-ttu-id="ba48d-172">A função **falha AcquireCredentialsHandle (Digest)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="ba48d-172">The **AcquireCredentialsHandle (Digest)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="ba48d-173">Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="ba48d-173">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="ba48d-174">Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="ba48d-174">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span>

<span data-ttu-id="ba48d-175">Em geral, **falha AcquireCredentialsHandle (Digest)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="ba48d-175">In general, **AcquireCredentialsHandle (Digest)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="ba48d-176">No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="ba48d-176">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="ba48d-177">Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="ba48d-177">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="ba48d-178">Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="ba48d-178">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="ba48d-179">Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ba48d-179">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="ba48d-180">Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="ba48d-180">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="ba48d-181">Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ba48d-181">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="ba48d-182">Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.</span><span class="sxs-lookup"><span data-stu-id="ba48d-182">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="ba48d-183">Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="ba48d-183">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba48d-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba48d-184">Requirements</span></span>



| <span data-ttu-id="ba48d-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba48d-185">Requirement</span></span> | <span data-ttu-id="ba48d-186">Valor</span><span class="sxs-lookup"><span data-stu-id="ba48d-186">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba48d-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba48d-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ba48d-188">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-188">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ba48d-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba48d-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ba48d-190">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba48d-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ba48d-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba48d-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba48d-192"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-192"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="ba48d-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba48d-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba48d-194"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-194"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="ba48d-195">DLL</span><span class="sxs-lookup"><span data-stu-id="ba48d-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba48d-196"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba48d-196"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="ba48d-197">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ba48d-197">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba48d-198">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ba48d-198">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ba48d-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba48d-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba48d-200">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="ba48d-200">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="ba48d-201">**AcceptSecurityContext (resumo)**</span><span class="sxs-lookup"><span data-stu-id="ba48d-201">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="ba48d-202">**InitializeSecurityContext (resumo)**</span><span class="sxs-lookup"><span data-stu-id="ba48d-202">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="ba48d-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="ba48d-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
