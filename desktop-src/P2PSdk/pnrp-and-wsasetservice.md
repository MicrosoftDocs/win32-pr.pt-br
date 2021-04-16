---
description: O PNRP usa a função WSASetService para registrar ou remover nomes de par.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP e WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754133"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="d5c50-103">PNRP e WSASetService</span><span class="sxs-lookup"><span data-stu-id="d5c50-103">PNRP and WSASetService</span></span>

<span data-ttu-id="d5c50-104">O PNRP usa a função [**WSASetService**](winsock-nsp-reference-links.md) para registrar ou remover [nomes de par](peer-names.md).</span><span class="sxs-lookup"><span data-stu-id="d5c50-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="d5c50-105">Registrando um nome</span><span class="sxs-lookup"><span data-stu-id="d5c50-105">Registering a Name</span></span>

<span data-ttu-id="d5c50-106">O registro inclui um nome de par e um conjunto de pontos de extremidade onde um serviço pode ser contatado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="d5c50-107">Um registro é específico para uma nuvem PNRP.</span><span class="sxs-lookup"><span data-stu-id="d5c50-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="d5c50-108">Depois que um par é registrado, há um atraso entre o registro e a propagação das informações de registro para outros nós.</span><span class="sxs-lookup"><span data-stu-id="d5c50-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="d5c50-109">Durante esse tempo, outros nós podem não ser capazes de resolver um par registrado recentemente.</span><span class="sxs-lookup"><span data-stu-id="d5c50-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="d5c50-110">O registro do serviço não é persistente.</span><span class="sxs-lookup"><span data-stu-id="d5c50-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="d5c50-111">Se um processo de cliente que registra um nome de par sair ou chamar [**WSACleanup**](winsock-nsp-reference-links.md), o nome do par será cancelado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="d5c50-112">Se um nome de par especificado já estiver registrado na mesma nuvem pelo processo atual, ele será substituído pelos novos valores de registro.</span><span class="sxs-lookup"><span data-stu-id="d5c50-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="d5c50-113">Ao registrar um nome de par, os seguintes valores de parâmetro devem ser indicados:</span><span class="sxs-lookup"><span data-stu-id="d5c50-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="d5c50-114">o parâmetro *essOperation* deve ter um valor **de \_ registro RNRSERVICE**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="d5c50-115">o parâmetro *dwControlFlags* deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="d5c50-116">Ao registrar um nome de par, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) referenciada pelo parâmetro *lpqsRegInfo* deve conter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d5c50-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d5c50-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="d5c50-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-118">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="d5c50-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="d5c50-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-120">Especifica um nome de par a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-120">Specifies a peer name to register.</span></span> <span data-ttu-id="d5c50-121">Se o [nome do par](peer-names.md) não for seguro, a identidade será opcional.</span><span class="sxs-lookup"><span data-stu-id="d5c50-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="d5c50-122">Se a identidade for especificada como **nula**, o PNRP usará a identidade local do computador — por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5c50-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="d5c50-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-124">Deve ser SVCID \_ pnrpname.</span><span class="sxs-lookup"><span data-stu-id="d5c50-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="d5c50-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-126">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-126">Ignored.</span></span> <span data-ttu-id="d5c50-127">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="d5c50-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-129">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-129">Ignored.</span></span> <span data-ttu-id="d5c50-130">No entanto, a cadeia de caracteres ainda precisa ter menos de 40 caracteres, incluindo o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d5c50-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="d5c50-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-132">Deve ser **ns \_ pnrpname** ou **ns \_ All**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="d5c50-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-134">Deve ser o **\_ provedor NS \_ pnrpname** ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="d5c50-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-136">Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="d5c50-137">Se esse valor for **nulo** ou uma cadeia de caracteres vazia, a nuvem padrão, "global", será usada.</span><span class="sxs-lookup"><span data-stu-id="d5c50-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="d5c50-138">Caso contrário, ele deve apontar para um nome de nuvem válido.</span><span class="sxs-lookup"><span data-stu-id="d5c50-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="d5c50-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-140">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-140">Ignored.</span></span> <span data-ttu-id="d5c50-141">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="d5c50-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-143">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-143">Ignored.</span></span> <span data-ttu-id="d5c50-144">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="d5c50-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-146">Especifica o número de endereços registrados por um serviço.</span><span class="sxs-lookup"><span data-stu-id="d5c50-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="d5c50-147">O número máximo de endereços que podem ser registrados para um único nome é 10.</span><span class="sxs-lookup"><span data-stu-id="d5c50-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5c50-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-149">Ponteiro para uma lista de endereços a serem registrados.</span><span class="sxs-lookup"><span data-stu-id="d5c50-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="d5c50-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-151">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-151">Ignored.</span></span> <span data-ttu-id="d5c50-152">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="d5c50-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-154">Ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="d5c50-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="d5c50-155">Parâmetros específicos na estrutura **PNRPINFO** devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d5c50-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="d5c50-156">Para obter mais informações, consulte a seção de estrutura **PNRPINFO** a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5c50-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="d5c50-157">Estrutura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="d5c50-157">PNRPINFO Structure</span></span>

<span data-ttu-id="d5c50-158">Se o membro **lpBlob** da estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) for definido, os seguintes membros da estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) deverão ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d5c50-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="d5c50-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="d5c50-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-160">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="d5c50-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="d5c50-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-162">Especifica a identidade do nome de par que é criado usando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="d5c50-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="d5c50-163">Se um nome de par não for seguro, a identidade será opcional.</span><span class="sxs-lookup"><span data-stu-id="d5c50-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="d5c50-164">Se a identidade for especificada como **nula**, o PNRP usará a identidade local do computador — por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5c50-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="d5c50-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-166">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-166">Ignored.</span></span> <span data-ttu-id="d5c50-167">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="d5c50-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-169">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-169">Ignored.</span></span> <span data-ttu-id="d5c50-170">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="d5c50-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-172">Especifica o número de segundos entre as operações de atualização.</span><span class="sxs-lookup"><span data-stu-id="d5c50-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="d5c50-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-174">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-174">Ignored.</span></span> <span data-ttu-id="d5c50-175">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d5c50-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-177">Deve ser zero (0) ou a **\_ dica PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="d5c50-178">O padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-178">The default is zero (0).</span></span> <span data-ttu-id="d5c50-179">Isso significa que a parte local do serviço da ID PNRP é criada usando o endereço IP em **saHint**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="d5c50-180">Caso contrário, o local do serviço é criado usando o primeiro endereço IP na primeira entrada IPv6 do membro **lpcsaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="d5c50-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="d5c50-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-182">Especifica o endereço IPv6 para a dica.</span><span class="sxs-lookup"><span data-stu-id="d5c50-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**Nome do seu**</span><span class="sxs-lookup"><span data-stu-id="d5c50-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-184">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-184">Ignored.</span></span> <span data-ttu-id="d5c50-185">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="d5c50-186">Cancelando o registro de um nome de par</span><span class="sxs-lookup"><span data-stu-id="d5c50-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="d5c50-187">A lista a seguir identifica as informações importantes sobre o cancelamento do registro de um nome de par.</span><span class="sxs-lookup"><span data-stu-id="d5c50-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="d5c50-188">Somente um aplicativo que registra um nome de par pode cancelar seu registro.</span><span class="sxs-lookup"><span data-stu-id="d5c50-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="d5c50-189">Um nome de par será cancelado automaticamente se [**WSACleanup**](winsock-nsp-reference-links.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="d5c50-190">O PNRP sempre remove o registro do nome do serviço inteiro.</span><span class="sxs-lookup"><span data-stu-id="d5c50-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="d5c50-191">Ele não permite a remoção de endereços individuais.</span><span class="sxs-lookup"><span data-stu-id="d5c50-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="d5c50-192">Ao cancelar o registro de um nome, o parâmetro *essOperation* deve ter um valor de **RNRSERVICE \_ delete**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="d5c50-193">O PNRP não oferece suporte ao valor **RNRSERVICE \_ cancelamento de registro**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="d5c50-194">O parâmetro *dwControlFlags* deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="d5c50-195">Ao cancelar o registro de um nome, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRegInfo* referencia deve conter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d5c50-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d5c50-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="d5c50-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-197">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="d5c50-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="d5c50-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-199">Especifica um nome de par para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="d5c50-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="d5c50-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-201">Deve ser **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="d5c50-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-203">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-203">Ignored.</span></span> <span data-ttu-id="d5c50-204">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="d5c50-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-206">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-206">Ignored.</span></span> <span data-ttu-id="d5c50-207">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="d5c50-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-209">Deve ser **ns \_ pnrpname** ou **ns \_ All**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="d5c50-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-211">Deve ser o **\_ provedor NS \_ pnrpname** ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="d5c50-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-213">Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="d5c50-214">Se esse valor for **nulo** ou uma cadeia de caracteres vazia, a nuvem padrão, "global", será usada.</span><span class="sxs-lookup"><span data-stu-id="d5c50-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="d5c50-215">Caso contrário, ele deve apontar para um nome de nuvem válido.</span><span class="sxs-lookup"><span data-stu-id="d5c50-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="d5c50-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-217">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-217">Ignored.</span></span> <span data-ttu-id="d5c50-218">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="d5c50-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-220">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-220">Ignored.</span></span> <span data-ttu-id="d5c50-221">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="d5c50-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-223">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-223">Ignored.</span></span> <span data-ttu-id="d5c50-224">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5c50-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-226">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-226">Ignored.</span></span> <span data-ttu-id="d5c50-227">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5c50-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="d5c50-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-229">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c50-229">Ignored.</span></span> <span data-ttu-id="d5c50-230">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5c50-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d5c50-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="d5c50-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="d5c50-232">Ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="d5c50-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="d5c50-233">O membro **lpszIdentity** da estrutura **lpBlob** identifica o nome da identidade que é usada para registrar um nome de par.</span><span class="sxs-lookup"><span data-stu-id="d5c50-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="d5c50-234">Os membros restantes devem ser definidos com os mesmos valores que são usados ao registrar um nome.</span><span class="sxs-lookup"><span data-stu-id="d5c50-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d5c50-235">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5c50-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c50-236">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="d5c50-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="d5c50-237">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="d5c50-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="d5c50-238">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="d5c50-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="d5c50-239">Códigos de erro NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="d5c50-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="d5c50-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="d5c50-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="d5c50-241">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="d5c50-241">**WSASetService**</span></span>
</dt> </dl>

 

 



