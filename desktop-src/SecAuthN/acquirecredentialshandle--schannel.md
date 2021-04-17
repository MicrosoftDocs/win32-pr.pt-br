---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando Schannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: Função falha AcquireCredentialsHandle (Schannel) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5b7de49e76cf5b09611790a12826f1a13fc38e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798309"
---
# <a name="acquirecredentialshandle-schannel-function"></a><span data-ttu-id="cc2c9-103">Função falha AcquireCredentialsHandle (Schannel)</span><span class="sxs-lookup"><span data-stu-id="cc2c9-103">AcquireCredentialsHandle (Schannel) function</span></span>

<span data-ttu-id="cc2c9-104">A função **falha AcquireCredentialsHandle (Schannel)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c9-104">The **AcquireCredentialsHandle (Schannel)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc2c9-105">Esse identificador é exigido pelas funções [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) e [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-105">This handle is required by the [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) and [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) functions.</span></span> <span data-ttu-id="cc2c9-106">Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="cc2c9-107">Isso não é um "logon na rede" e não implica a coleta de credenciais.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cc2c9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc2c9-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="cc2c9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc2c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc2c9-110">*pszPrincipal* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-110">*pszPrincipal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="cc2c9-112">Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-112">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="cc2c9-113">Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="cc2c9-114">Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="cc2c9-115">*pszPackage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="cc2c9-117">Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="cc2c9-118">Depois que um contexto é estabelecido, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) pode ser chamado com *ULATTRIBUTE* definido como \_ SECPKG \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-118">After a context is established, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="cc2c9-119">Ao usar o SSP do Schannel, defina esse parâmetro como UNISP \_ nome.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-119">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-120">*fCredentialUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-121">Um sinalizador que indica como essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="cc2c9-122">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cc2c9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cc2c9-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="cc2c9-124">Significado</span><span class="sxs-lookup"><span data-stu-id="cc2c9-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="cc2c9-125"><dt>**\_entrada de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="cc2c9-126">Valide uma credencial de servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-126">Validate an incoming server credential.</span></span> <span data-ttu-id="cc2c9-127">As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) ou [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) or [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) is called.</span></span> <span data-ttu-id="cc2c9-128">Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="cc2c9-129">A validação é específica do pacote.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="cc2c9-130"><dt>**\_saída de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="cc2c9-131">Permitir que uma credencial de cliente local Prepare um token de saída.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="cc2c9-132">*pvLogonID* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-132">*pvLogonID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-133">Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="cc2c9-134">Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="cc2c9-135">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-135">This parameter can be **NULL**.</span></span>

<span data-ttu-id="cc2c9-136">Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-136">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-137">*pAuthData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-137">*pAuthData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-138">Um ponteiro para dados específicos do pacote.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-138">A pointer to package-specific data.</span></span> <span data-ttu-id="cc2c9-139">Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="cc2c9-140">Para usar credenciais fornecidas, passe uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que inclui essas credenciais nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="cc2c9-141">O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="cc2c9-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="cc2c9-142">Ao usar o SSP do Schannel, especifique uma estrutura de [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) que indique o protocolo a ser usado e as configurações para vários recursos de canal personalizáveis.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-142">When using the Schannel SSP, specify an [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-143">*pGetKeyFn* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-143">*pGetKeyFn* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-144">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-145">*pvGetKeyArgument* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-145">*pvGetKeyArgument* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-146">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-147">*phCredential* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-148">Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="cc2c9-149">*ptsExpiry* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-149">*ptsExpiry* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2c9-150">Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="cc2c9-151">O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c9-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc2c9-152">O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="cc2c9-153">Ao usar o SSP do Schannel, esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-153">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="cc2c9-154">Quando a credencial a ser usada para autenticação é um certificado, esse parâmetro recebe o tempo de expiração para esse certificado.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-154">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="cc2c9-155">Se nenhum certificado tiver sido fornecido, um valor de tempo máximo será retornado.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-155">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc2c9-156">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc2c9-156">Return value</span></span>

<span data-ttu-id="cc2c9-157">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-157">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="cc2c9-158">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-158">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="cc2c9-159">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc2c9-159">Return code</span></span>                                                                                                 | <span data-ttu-id="cc2c9-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc2c9-160">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc2c9-161"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-161"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc2c9-162">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-162">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="cc2c9-163"><dt>**s \_ E \_ \_ erro interno**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-163"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="cc2c9-164">Ocorreu um erro que não foi mapeado para um código de erro SSPI.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-164">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="cc2c9-165"><dt>**s \_ E \_ sem \_ credenciais**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-165"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="cc2c9-166">Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c9-166">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="cc2c9-167"><dt>**s \_ E \_ não \_ proprietário**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-167"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="cc2c9-168">O chamador da função não tem as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-168">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="cc2c9-169"><dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-169"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="cc2c9-170">O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-170">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="cc2c9-171"><dt>**s \_ E \_ credenciais desconhecidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-171"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="cc2c9-172">As credenciais fornecidas para o pacote não foram reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-172">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="cc2c9-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc2c9-173">Remarks</span></span>

<span data-ttu-id="cc2c9-174">A função **falha AcquireCredentialsHandle (Schannel)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-174">The **AcquireCredentialsHandle (Schannel)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc2c9-175">Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-175">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="cc2c9-176">Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) e [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-176">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) and [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) functions.</span></span>

<span data-ttu-id="cc2c9-177">Em geral, o **falha AcquireCredentialsHandle (Schannel)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-177">In general, **AcquireCredentialsHandle (Schannel)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="cc2c9-178">No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-178">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="cc2c9-179">Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-179">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="cc2c9-180">Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-180">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="cc2c9-181">Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-181">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="cc2c9-182">Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="cc2c9-182">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="cc2c9-183">Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-183">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="cc2c9-184">Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.</span><span class="sxs-lookup"><span data-stu-id="cc2c9-184">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="cc2c9-185">Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="cc2c9-185">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2c9-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2c9-186">Requirements</span></span>



| <span data-ttu-id="cc2c9-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2c9-187">Requirement</span></span> | <span data-ttu-id="cc2c9-188">Valor</span><span class="sxs-lookup"><span data-stu-id="cc2c9-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2c9-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc2c9-189">Minimum supported client</span></span><br/> | <span data-ttu-id="cc2c9-190">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-190">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cc2c9-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc2c9-191">Minimum supported server</span></span><br/> | <span data-ttu-id="cc2c9-192">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc2c9-192">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="cc2c9-193">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc2c9-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc2c9-194"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-194"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="cc2c9-195">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc2c9-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc2c9-196"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-196"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="cc2c9-197">DLL</span><span class="sxs-lookup"><span data-stu-id="cc2c9-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc2c9-198"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc2c9-198"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="cc2c9-199">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cc2c9-199">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cc2c9-200">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cc2c9-200">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cc2c9-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc2c9-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2c9-202">**AcceptSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="cc2c9-202">**AcceptSecurityContext (Schannel)**</span></span>](acceptsecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="cc2c9-203">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="cc2c9-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[<span data-ttu-id="cc2c9-204">**InitializeSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="cc2c9-204">**InitializeSecurityContext (Schannel)**</span></span>](initializesecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="cc2c9-205">**SCH_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="cc2c9-205">**SCH_CREDENTIALS**</span></span>](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[<span data-ttu-id="cc2c9-206">**Funções SSPI**</span><span class="sxs-lookup"><span data-stu-id="cc2c9-206">**SSPI Functions**</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
