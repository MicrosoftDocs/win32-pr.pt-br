---
description: Recupera a senha da conta de serviço.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Função GetServiceAccountPassword (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767812"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="9c14e-103">Função GetServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="9c14e-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="9c14e-104">Recupera a senha da conta de serviço, disponível para os SSPs ( [*provedores de suporte de segurança*](/windows/desktop/SecGloss/s-gly) ), como o SSP do Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9c14e-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c14e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c14e-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="9c14e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c14e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c14e-107">*AccountName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-108">Nome da conta terminada com nulo da conta de conta de serviço gerenciado (gMSA) do grupo.</span><span class="sxs-lookup"><span data-stu-id="9c14e-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="9c14e-109">O nome de usuário pode ser uma das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="9c14e-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="9c14e-110">Nome da conta SAM do gMSA.</span><span class="sxs-lookup"><span data-stu-id="9c14e-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="9c14e-111">Nome de usuário em um FQDN (nome de domínio totalmente qualificado), como *DomainName \* **\\** _username_ ou **www.** _domínio_* do _. com \\_ \* _nome_.</span><span class="sxs-lookup"><span data-stu-id="9c14e-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="9c14e-112">O nome de usuário deve ser apenas um nome SAM.</span><span class="sxs-lookup"><span data-stu-id="9c14e-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="9c14e-113">O nome de domínio pode ser um nome DNS ou um nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="9c14e-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="9c14e-114">UPN (nome principal de usuário) implícito para a conta gMSA, por exemplo, *somename \* **@** _Domain_*_. com_\*, em que, de acordo com a definição de um UPN implícito, o *domínio \* \* *. com** é o nome DNS de domínio real.</span><span class="sxs-lookup"><span data-stu-id="9c14e-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="9c14e-115">*Nome_do_domínio* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-116">Nome de domínio opcional finalizado por nulo.</span><span class="sxs-lookup"><span data-stu-id="9c14e-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="9c14e-117">Isso será válido somente se o parâmetro *AccountName* for um nome de conta Sam.</span><span class="sxs-lookup"><span data-stu-id="9c14e-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="9c14e-118">O nome de domínio só pode ser um nome NetBIOS ou um FQDN (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="9c14e-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="9c14e-119">*CredFetch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-120">Um valor da enumeração [**de \_ busca de credenciais**](cred-fetch.md) que especifica como recuperar a credencial.</span><span class="sxs-lookup"><span data-stu-id="9c14e-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="9c14e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9c14e-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="9c14e-122">Significado</span><span class="sxs-lookup"><span data-stu-id="9c14e-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="9c14e-123"><dt>**CredFetchDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="9c14e-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="9c14e-124">O sistema operacional primeiro tenta recuperar a senha do cache local se não for o momento de buscar a senha.</span><span class="sxs-lookup"><span data-stu-id="9c14e-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="9c14e-125">Se for o momento de buscar a senha, o sistema operacional entrará em contato com o controlador de domínio, caso contrário, retornará qualquer senha armazenada em cache com um valor de status êxito.</span><span class="sxs-lookup"><span data-stu-id="9c14e-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="9c14e-126"><dt>**CredFetchDPAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="9c14e-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="9c14e-127">Retorna a credencial DPAPI local para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9c14e-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="9c14e-128">Os SSPs geralmente não exigem o uso desse valor.</span><span class="sxs-lookup"><span data-stu-id="9c14e-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="9c14e-129"><dt>**CredFetchForced**</dt></span><span class="sxs-lookup"><span data-stu-id="9c14e-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="9c14e-130">Força o sistema operacional a tentar ler a senha do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="9c14e-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="9c14e-131">Durante a hora de substituição da senha, a senha pode ter sido alterada no controlador de domínio e em outros hosts membros, mas o host membro do gMSA reconhece a senha como ainda válida.</span><span class="sxs-lookup"><span data-stu-id="9c14e-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="9c14e-132">Isso pode acontecer devido a problemas de distorção de relógio entre diferentes controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="9c14e-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="9c14e-133">Quando esse valor é especificado, o sistema operacional determina se pode haver uma possível alteração de senha devido à distorção do relógio e, nesse caso, recupera a senha.</span><span class="sxs-lookup"><span data-stu-id="9c14e-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="9c14e-134">Caso contrário, a credencial armazenada em cache será retornada.</span><span class="sxs-lookup"><span data-stu-id="9c14e-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="9c14e-135">Se não houver nenhuma credencial armazenada em cache, o sistema operacional tentará obter uma do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="9c14e-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c14e-136">*FileTimeExpiry* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-137">Na entrada, se esse valor for não nulo e não for um **FILETIME** zero, *FileTimeExpiry* conterá o tempo de expiração das credenciais da conta de serviço como conhecido para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9c14e-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="9c14e-138">Se o parâmetro *FileTimeExpiry* for o mesmo que uma das credenciais atuais, essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="9c14e-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="9c14e-139">Na saída, o parâmetro *FileTimeExpiry* contém o tempo de expiração da credencial que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="9c14e-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="9c14e-140">*CurrentPassword* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-141">A senha atual do gMSA.</span><span class="sxs-lookup"><span data-stu-id="9c14e-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="9c14e-142">*PreviousPassword* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-143">A senha anterior do gMSA.</span><span class="sxs-lookup"><span data-stu-id="9c14e-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="9c14e-144">*FileTimeCurrPwdValidForOutbound* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c14e-145">Indica o tempo após o qual a senha atual é válida para solicitações de saída.</span><span class="sxs-lookup"><span data-stu-id="9c14e-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="9c14e-146">O chamador deve comparar a hora atual com esse valor e usar a senha atual retornada somente se a hora atual for maior ou igual ao valor retornado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9c14e-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="9c14e-147">O uso desse parâmetro é projetado para chamadores que não têm repetição na lógica de saída, por exemplo, NTLM.</span><span class="sxs-lookup"><span data-stu-id="9c14e-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c14e-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c14e-148">Return value</span></span>

<span data-ttu-id="9c14e-149">Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.</span><span class="sxs-lookup"><span data-stu-id="9c14e-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="9c14e-150">Se a função falhar, o valor de retorno será um código NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="9c14e-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="9c14e-151">Para obter mais informações, consulte [valores de retorno da função de política LSA](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9c14e-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="9c14e-152">Você pode usar a função [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) para converter o código NtStatus em um código de erro do Windows.</span><span class="sxs-lookup"><span data-stu-id="9c14e-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="9c14e-153">Quando você terminar de usar os buffers retornados nos parâmetros *CurrentPassword* e *PreviousPassword* , libere-os chamando a função [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .</span><span class="sxs-lookup"><span data-stu-id="9c14e-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c14e-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c14e-154">Remarks</span></span>

<span data-ttu-id="9c14e-155">A função **GetServiceAccountPassword** pode ser chamada nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="9c14e-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="9c14e-156">Nas funções de logon do SSP (provedores de suporte de segurança), o SSP deve detectar que a senha da conta de serviço \_ \_ está sendo usada para fazer logon na entidade e verificar se o chamador tem privilégio TCB ou é um serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="9c14e-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="9c14e-157">Em seguida, o SSP deve permitir que o processo de logon continue obtendo a credencial mais recente chamando a função **GetServiceAccountPassword** com o valor **CredFetchDefault** na enumeração de [**\_ busca de cred**](cred-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="9c14e-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="9c14e-158">De SSPs em suas chamadas [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) e [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="9c14e-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="9c14e-159">Os SSPs devem detectar que a \_ senha da conta de serviço \_ está sendo usada para essas chamadas e, se a chamada for para credenciais não primárias, o SSP deverá garantir que o chamador tenha o privilégio TCB ou seja um serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="9c14e-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="9c14e-160">Em seguida, o SSP deve chamar a função **GetServiceAccountPassword** com o valor **CredFetchDefault** na enumeração de [**\_ busca de cred**](cred-fetch.md) e prosseguir com a chamada.</span><span class="sxs-lookup"><span data-stu-id="9c14e-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="9c14e-161">Se as chamadas **InitializeSecurityContext** e **AcceptSecurityContext** falharem, o SSP deverá usar o *FileTimeExpiry* recuperado da chamada anterior para **GetServiceAccountPassword** e usá-lo como entrada para chamar **GetServiceAccountPassword** novamente usando o valor **CredFetchForced** na enumeração **de \_ busca de credenciais** .</span><span class="sxs-lookup"><span data-stu-id="9c14e-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="9c14e-162">Se uma nova credencial gMSA estiver disponível, a segunda chamada terá sucesso com novas credenciais, e o SSP deverá tentar novamente com as novas credenciais.</span><span class="sxs-lookup"><span data-stu-id="9c14e-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c14e-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c14e-163">Requirements</span></span>



| <span data-ttu-id="9c14e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c14e-164">Requirement</span></span> | <span data-ttu-id="9c14e-165">Valor</span><span class="sxs-lookup"><span data-stu-id="9c14e-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9c14e-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c14e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="9c14e-167">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9c14e-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c14e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="9c14e-169">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9c14e-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c14e-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c14e-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c14e-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

