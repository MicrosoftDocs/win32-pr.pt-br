---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança que esteja usando Kerberos.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: Função falha AcquireCredentialsHandle (Kerberos) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812417"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="5675e-103">Função falha AcquireCredentialsHandle (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="5675e-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="5675e-104">A função **falha AcquireCredentialsHandle (Kerberos)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5675e-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5675e-105">Esse identificador é exigido pelas funções [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) e [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="5675e-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="5675e-106">Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="5675e-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="5675e-107">Isso não é um "logon na rede" e não implica a coleta de credenciais.</span><span class="sxs-lookup"><span data-stu-id="5675e-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5675e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5675e-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5675e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5675e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5675e-110">*pszPrincipal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="5675e-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="5675e-112">Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5675e-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="5675e-113">Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="5675e-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="5675e-114">*pszPackage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="5675e-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="5675e-116">Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="5675e-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="5675e-117">Depois que um contexto é estabelecido, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) pode ser chamado com *ULATTRIBUTE* definido como \_ SECPKG \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.</span><span class="sxs-lookup"><span data-stu-id="5675e-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="5675e-118">*fCredentialUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-119">Um sinalizador que indica como essas credenciais serão usadas.</span><span class="sxs-lookup"><span data-stu-id="5675e-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="5675e-120">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5675e-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5675e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5675e-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="5675e-122">Significado</span><span class="sxs-lookup"><span data-stu-id="5675e-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="5675e-123"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="5675e-124">Valide uma credencial de entrada ou use uma credencial local para preparar um token de saída.</span><span class="sxs-lookup"><span data-stu-id="5675e-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="5675e-125">Esse sinalizador habilita ambos os outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="5675e-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="5675e-126"><dt>**\_entrada de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="5675e-127">Valide uma credencial de servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="5675e-127">Validate an incoming server credential.</span></span> <span data-ttu-id="5675e-128">As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) ou [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="5675e-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="5675e-129">Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ .</span><span class="sxs-lookup"><span data-stu-id="5675e-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="5675e-130">A validação é específica do pacote.</span><span class="sxs-lookup"><span data-stu-id="5675e-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="5675e-131"><dt>**\_saída de credenciais SECPKG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="5675e-132">Permitir que uma credencial de cliente local Prepare um token de saída.</span><span class="sxs-lookup"><span data-stu-id="5675e-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5675e-133">*pvLogonID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-134">Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="5675e-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="5675e-135">Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede.</span><span class="sxs-lookup"><span data-stu-id="5675e-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="5675e-136">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5675e-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5675e-137">*pAuthData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-138">Um ponteiro para dados específicos do pacote.</span><span class="sxs-lookup"><span data-stu-id="5675e-138">A pointer to package-specific data.</span></span> <span data-ttu-id="5675e-139">Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="5675e-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="5675e-140">Para usar credenciais fornecidas, passe uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que inclui essas credenciais nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5675e-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="5675e-141">O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="5675e-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="5675e-142">*pGetKeyFn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-143">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5675e-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5675e-144">*pvGetKeyArgument* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5675e-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-145">Esse parâmetro não é usado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5675e-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5675e-146">*phCredential* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5675e-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-147">Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="5675e-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="5675e-148">*ptsExpiry* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5675e-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5675e-149">Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram.</span><span class="sxs-lookup"><span data-stu-id="5675e-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="5675e-150">O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5675e-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5675e-151">O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.</span><span class="sxs-lookup"><span data-stu-id="5675e-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5675e-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5675e-152">Return value</span></span>

<span data-ttu-id="5675e-153">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5675e-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="5675e-154">Se a função falhar, ela retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="5675e-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="5675e-155">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5675e-155">Return code</span></span>                                                                                                 | <span data-ttu-id="5675e-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="5675e-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5675e-157"><dt>**s \_ E \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="5675e-158">Não há memória suficiente disponível para concluir a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5675e-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="5675e-159"><dt>**s \_ E \_ \_ erro interno**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="5675e-160">Ocorreu um erro que não foi mapeado para um código de erro SSPI.</span><span class="sxs-lookup"><span data-stu-id="5675e-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="5675e-161"><dt>**s \_ E \_ sem \_ credenciais**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="5675e-162">Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5675e-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="5675e-163"><dt>**s \_ E \_ não \_ proprietário**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="5675e-164">O chamador da função não tem as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="5675e-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="5675e-165"><dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="5675e-166">O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.</span><span class="sxs-lookup"><span data-stu-id="5675e-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5675e-167"><dt>**s \_ E \_ credenciais desconhecidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="5675e-168">As credenciais fornecidas para o pacote não foram reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="5675e-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5675e-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="5675e-169">Remarks</span></span>

<span data-ttu-id="5675e-170">A função **falha AcquireCredentialsHandle (Kerberos)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica.</span><span class="sxs-lookup"><span data-stu-id="5675e-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="5675e-171">Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="5675e-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="5675e-172">Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) e [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="5675e-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="5675e-173">Em geral, o **falha AcquireCredentialsHandle (Kerberos)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="5675e-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="5675e-174">No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="5675e-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="5675e-175">Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="5675e-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="5675e-176">Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="5675e-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="5675e-177">Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5675e-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="5675e-178">Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="5675e-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="5675e-179">Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5675e-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="5675e-180">Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.</span><span class="sxs-lookup"><span data-stu-id="5675e-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="5675e-181">Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="5675e-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5675e-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5675e-182">Requirements</span></span>



| <span data-ttu-id="5675e-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="5675e-183">Requirement</span></span> | <span data-ttu-id="5675e-184">Valor</span><span class="sxs-lookup"><span data-stu-id="5675e-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5675e-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5675e-185">Minimum supported client</span></span><br/> | <span data-ttu-id="5675e-186">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5675e-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5675e-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5675e-187">Minimum supported server</span></span><br/> | <span data-ttu-id="5675e-188">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5675e-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5675e-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5675e-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="5675e-190"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="5675e-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5675e-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="5675e-192"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="5675e-193">DLL</span><span class="sxs-lookup"><span data-stu-id="5675e-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5675e-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5675e-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="5675e-195">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5675e-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5675e-196">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5675e-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5675e-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="5675e-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5675e-198">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="5675e-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="5675e-199">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="5675e-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="5675e-200">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="5675e-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="5675e-201">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="5675e-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
