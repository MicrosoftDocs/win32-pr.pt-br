---
description: A função LogonUserExExW tenta fazer logon de um usuário no computador local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Função LogonUserExExW (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011525"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="b814e-103">Função LogonUserExExW</span><span class="sxs-lookup"><span data-stu-id="b814e-103">LogonUserExExW function</span></span>

<span data-ttu-id="b814e-104">A função **LogonUserExExW** tenta fazer logon de um usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="b814e-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="b814e-105">O computador local é o computador do qual **LogonUserExExW** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="b814e-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="b814e-106">Você não pode usar o **LogonUserExExW** para fazer logon em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b814e-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="b814e-107">Especifique o usuário usando um nome de usuário e um domínio e [*autentique*](../secgloss/a-gly.md) o usuário usando uma senha de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="b814e-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="b814e-108">Se a função for realizada com sucesso, ela receberá um identificador para um token que representa o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b814e-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="b814e-109">Você pode usar esse identificador de token para representar o usuário especificado ou, na maioria dos casos, para criar um [*processo*](../secgloss/p-gly.md) que é executado no contexto do usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="b814e-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="b814e-110">Essa função é semelhante à função [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , exceto pelo fato de que ela usa o parâmetro adicional, *pTokenGroups*, que é um conjunto de um ou mais SIDs ( [*identificadores de segurança*](../secgloss/s-gly.md) ) que são adicionados ao token retornado ao chamador quando o logon é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b814e-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="b814e-111">Essa função não é declarada em um cabeçalho público e não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="b814e-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="b814e-112">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b814e-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b814e-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b814e-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="b814e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b814e-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b814e-115">*lpszUsername* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b814e-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="b814e-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="b814e-117">Esse é o nome da conta de usuário para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="b814e-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="b814e-118">Se você usar o formato UPN ( [*nome principal do usuário*](../secgloss/u-gly.md) ), o parâmetro *LpszDomain* deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b814e-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-119">*lpszDomain* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-120">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do domínio ou do servidor cujo banco de dados de conta contém a conta *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="b814e-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="b814e-121">Se esse parâmetro for **nulo**, o nome de usuário deverá ser especificado no formato UPN.</span><span class="sxs-lookup"><span data-stu-id="b814e-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="b814e-122">Se esse parâmetro for ".", a função validará a conta usando apenas o banco de dados de conta local.</span><span class="sxs-lookup"><span data-stu-id="b814e-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-123">*lpszPassword* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-124">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a senha de texto não criptografado para a conta de usuário especificada por *lpszUsername*.</span><span class="sxs-lookup"><span data-stu-id="b814e-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="b814e-125">Quando você terminar de usar a senha, limpe a senha da memória chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b814e-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="b814e-126">Para obter mais informações sobre como proteger senhas, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="b814e-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="b814e-127">*dwLogonType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b814e-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-128">O tipo de operação de logon a ser executada.</span><span class="sxs-lookup"><span data-stu-id="b814e-128">The type of logon operation to perform.</span></span> <span data-ttu-id="b814e-129">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b814e-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b814e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b814e-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="b814e-131">Significado</span><span class="sxs-lookup"><span data-stu-id="b814e-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="b814e-132"><dt>**LOGON32 \_ LOGON \_ interativo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="b814e-133">Esse tipo de logon destina-se a usuários que irão usar o computador interativamente, como um usuário conectado por um servidor de [*terminal*](../secgloss/t-gly.md) , um shell remoto ou um processo semelhante.</span><span class="sxs-lookup"><span data-stu-id="b814e-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="b814e-134">Esse tipo de logon tem as despesas adicionais de armazenar em cache informações de logon para operações desconectadas; Portanto, não é apropriado para alguns aplicativos cliente/servidor, como um servidor de email.</span><span class="sxs-lookup"><span data-stu-id="b814e-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="b814e-135"><dt>**LOGON32 \_ \_Rede de logon**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="b814e-136">Esse tipo de logon destina-se a servidores de alto desempenho para autenticar senhas de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="b814e-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="b814e-137">A função **LogonUserExExW** não armazena em cache as credenciais para esse tipo de logon.</span><span class="sxs-lookup"><span data-stu-id="b814e-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="b814e-138"><dt>**LOGON32 \_ \_Lote de logon**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="b814e-139">Esse tipo de logon destina-se a servidores de lote, em que processos podem ser executados em nome de um usuário sem sua intervenção direta.</span><span class="sxs-lookup"><span data-stu-id="b814e-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="b814e-140">Esse tipo também é para servidores de desempenho mais alto que processam muitas tentativas de autenticação de texto sem formatação por vez, como servidores Web ou de email.</span><span class="sxs-lookup"><span data-stu-id="b814e-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="b814e-141">A função **LogonUserExExW** não armazena em cache as credenciais para esse tipo de logon.</span><span class="sxs-lookup"><span data-stu-id="b814e-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="b814e-142"><dt>**LOGON32 \_ \_Serviço de logon**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="b814e-143">Indica um logon de tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="b814e-143">Indicates a service-type logon.</span></span> <span data-ttu-id="b814e-144">A conta fornecida deve ter o privilégio de serviço habilitado.</span><span class="sxs-lookup"><span data-stu-id="b814e-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="b814e-145"><dt>**LOGON32 \_ \_Desbloqueio de logon**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="b814e-146">Esse tipo de logon destina-se a DLLs de [*Gina*](../secgloss/g-gly.md) que fazem logon de usuários que serão interativamente usando o computador.</span><span class="sxs-lookup"><span data-stu-id="b814e-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="b814e-147">Esse tipo de logon pode gerar um registro de auditoria exclusivo que mostra quando a estação de trabalho foi desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="b814e-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="b814e-148"><dt>**LOGON32 \_ \_ \_ Texto puro da rede de logon**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="b814e-149">Esse tipo de logon preserva o nome e a senha no [*pacote de autenticação*](../secgloss/a-gly.md), o que permite que o servidor faça conexões com outros servidores de rede enquanto representa o cliente.</span><span class="sxs-lookup"><span data-stu-id="b814e-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="b814e-150">Um servidor pode aceitar credenciais de texto não criptografado de um cliente, chamar **LogonUserExExW**, verificar se o usuário pode acessar o sistema pela rede e ainda se comunicar com outros servidores.</span><span class="sxs-lookup"><span data-stu-id="b814e-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="b814e-151"><dt>**LOGON32 \_ \_Novas \_ credenciais de logon**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="b814e-152">Esse tipo de logon permite que o chamador clone seu token atual e especifique novas credenciais para conexões de saída.</span><span class="sxs-lookup"><span data-stu-id="b814e-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="b814e-153">A nova sessão de logon tem o mesmo identificador local, mas usa credenciais diferentes para outras conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="b814e-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="b814e-154">Esse tipo de logon tem suporte apenas pelo provedor de logon do **LOGON32 \_ Provider \_ WINNT50** .</span><span class="sxs-lookup"><span data-stu-id="b814e-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="b814e-155">*dwLogonProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b814e-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-156">O provedor de logon.</span><span class="sxs-lookup"><span data-stu-id="b814e-156">The logon provider.</span></span> <span data-ttu-id="b814e-157">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b814e-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b814e-158">Valor</span><span class="sxs-lookup"><span data-stu-id="b814e-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="b814e-159">Significado</span><span class="sxs-lookup"><span data-stu-id="b814e-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="b814e-160"><dt>**\_Padrão do provedor LOGON32 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="b814e-161">Use o provedor de logon padrão para o sistema.</span><span class="sxs-lookup"><span data-stu-id="b814e-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="b814e-162">O [*provedor de segurança*](../secgloss/s-gly.md) padrão é NTLM.</span><span class="sxs-lookup"><span data-stu-id="b814e-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="b814e-163"><dt>**\_Provedor LOGON32 \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="b814e-164">Use o provedor de logon Negotiate.</span><span class="sxs-lookup"><span data-stu-id="b814e-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="b814e-165"><dt>**\_Provedor LOGON32 \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="b814e-166">Use o provedor de logon NTLM.</span><span class="sxs-lookup"><span data-stu-id="b814e-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="b814e-167">*pTokenGroups* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-168">Um ponteiro para uma estrutura de [**\_ grupos de token**](/windows/win32/api/winnt/ns-winnt-token_groups) que especifica uma lista de SIDs de grupo que são adicionados ao token que essa função recebe após o logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b814e-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="b814e-169">Todos os SIDs adicionados ao token também afetam a expansão do grupo.</span><span class="sxs-lookup"><span data-stu-id="b814e-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="b814e-170">Por exemplo, se os SIDs adicionados forem membros de grupos locais, esses grupos também serão adicionados ao token de acesso recebido.</span><span class="sxs-lookup"><span data-stu-id="b814e-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="b814e-171">Se esse parâmetro não for **nulo**, o chamador dessa função deverá ter o privilégio **de \_ \_ privilégio do se TCB** concedido e habilitado.</span><span class="sxs-lookup"><span data-stu-id="b814e-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-172">*phToken* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-173">Um ponteiro para uma variável de identificador que recebe um identificador para um token que representa o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="b814e-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="b814e-174">Você pode usar o identificador retornado em chamadas para a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .</span><span class="sxs-lookup"><span data-stu-id="b814e-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="b814e-175">Na maioria dos casos, o identificador retornado é um [*token primário*](../secgloss/p-gly.md) que você pode usar em chamadas para a função [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="b814e-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="b814e-176">No entanto, se você especificar o sinalizador de rede de logon do LOGON32 \_ \_ , **LogonUserExExW** retornará um [*token de representação*](../secgloss/i-gly.md) que você não pode usar no **CreateProcessAsUser** , a menos que chame [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token de representação em um token primário.</span><span class="sxs-lookup"><span data-stu-id="b814e-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="b814e-177">Quando você não precisar mais desse identificador, feche-o chamando a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="b814e-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-178">*ppLogonSid* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-179">Um ponteiro para um ponteiro para um SID que recebe o SID do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b814e-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="b814e-180">Quando você terminar de usar o SID, libere-o chamando a função [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="b814e-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-181">*ppProfileBuffer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-182">Um ponteiro para um ponteiro que recebe o endereço de um buffer que contém o perfil do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b814e-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-183">*pdwProfileLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-184">Um ponteiro para um **DWORD** que recebe o comprimento do buffer de perfil.</span><span class="sxs-lookup"><span data-stu-id="b814e-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b814e-185">*pQuotaLimits* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b814e-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b814e-186">Um ponteiro para uma estrutura de [**\_ limites de cota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) que recebe informações sobre as cotas para o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b814e-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b814e-187">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b814e-187">Return value</span></span>

<span data-ttu-id="b814e-188">Se a função for realizada com sucesso, a função retornará diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b814e-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="b814e-189">Se a função falhar, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b814e-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="b814e-190">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b814e-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b814e-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="b814e-191">Remarks</span></span>

<span data-ttu-id="b814e-192">O tipo de logon de **\_ \_ rede de logon do LOGON32** é mais rápido, mas tem as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="b814e-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="b814e-193">A função retorna um [*token de representação*](../secgloss/i-gly.md), não um token primário.</span><span class="sxs-lookup"><span data-stu-id="b814e-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="b814e-194">Você não pode usar esse token diretamente na função [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="b814e-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="b814e-195">No entanto, você pode chamar a função [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token em um token primário e, em seguida, usá-lo em **CreateProcessAsUser**.</span><span class="sxs-lookup"><span data-stu-id="b814e-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="b814e-196">Se você converter o token em um token primário e usá-lo no [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar um processo, o novo processo não poderá acessar outros recursos de rede, como servidores remotos ou impressoras, por meio do redirecionador.</span><span class="sxs-lookup"><span data-stu-id="b814e-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="b814e-197">Uma exceção é que, se o recurso de rede não tiver acesso controlado, o novo processo poderá acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="b814e-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="b814e-198">A conta especificada por *lpszUsername* deve ter os direitos de conta necessários.</span><span class="sxs-lookup"><span data-stu-id="b814e-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="b814e-199">Por exemplo, para fazer logon em um usuário com o sinalizador **\_ \_ interativo de logon do LOGON32** , o usuário (ou um grupo ao qual o usuário pertence) deve ter a conta de **\_ \_ \_ nome de logon interativo do se** .</span><span class="sxs-lookup"><span data-stu-id="b814e-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="b814e-200">Para obter uma lista dos direitos de conta que afetam as várias operações de logon, consulte [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="b814e-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="b814e-201">Um usuário será considerado conectado se pelo menos um token existir.</span><span class="sxs-lookup"><span data-stu-id="b814e-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="b814e-202">Se você chamar [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e, em seguida, fechar o token, o usuário ainda estará conectado até que o processo (e todos os processos filho) tenha terminado.</span><span class="sxs-lookup"><span data-stu-id="b814e-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="b814e-203">Se o parâmetro opcional *pTokenGroups* for fornecido, o LSA não adicionará o SID local ou o Sid de logon automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b814e-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="b814e-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b814e-204">Requirements</span></span>



| <span data-ttu-id="b814e-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="b814e-205">Requirement</span></span> | <span data-ttu-id="b814e-206">Valor</span><span class="sxs-lookup"><span data-stu-id="b814e-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b814e-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b814e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="b814e-208">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b814e-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="b814e-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b814e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="b814e-210">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b814e-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="b814e-211">Versão</span><span class="sxs-lookup"><span data-stu-id="b814e-211">Version</span></span><br/>                  | <span data-ttu-id="b814e-212">O LogonUserExExW também está disponível no Windows Server 2003 ou no Windows XPwith a versão de distribuição geral.</span><span class="sxs-lookup"><span data-stu-id="b814e-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="b814e-213">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b814e-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="b814e-214"><dt>Winbasep. h</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="b814e-215">DLL</span><span class="sxs-lookup"><span data-stu-id="b814e-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b814e-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b814e-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b814e-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="b814e-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b814e-218">Controle de acesso de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="b814e-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="b814e-219">Funções de controle de acesso de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="b814e-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="b814e-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="b814e-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="b814e-221">**CreateProcessAsUser**</span><span class="sxs-lookup"><span data-stu-id="b814e-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="b814e-222">**DuplicateTokenEx**</span><span class="sxs-lookup"><span data-stu-id="b814e-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="b814e-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="b814e-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="b814e-224">**LogonUserEx**</span><span class="sxs-lookup"><span data-stu-id="b814e-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="b814e-225">**limites de cota \_**</span><span class="sxs-lookup"><span data-stu-id="b814e-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
