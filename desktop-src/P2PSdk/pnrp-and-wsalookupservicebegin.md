---
description: O PNRP usa a função WSALookupServiceBegin para iniciar o processo que permite que um aplicativo faça o seguinte.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP e WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105753114"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="b5498-103">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="b5498-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="b5498-104">O PNRP usa a função [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar o processo que permite que um aplicativo faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b5498-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="b5498-105">Resolvendo um nome</span><span class="sxs-lookup"><span data-stu-id="b5498-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="b5498-106">Enumerando nuvens de rede</span><span class="sxs-lookup"><span data-stu-id="b5498-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="b5498-107">Os clientes que tentam executar uma das funções usam as funções [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** e **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="b5498-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="b5498-108">Usando [**WSANSPIoctl**](winsock-nsp-reference-links.md), o serviço de pesquisa pode ser usado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b5498-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="b5498-109">Para obter informações sobre como usar as funções de serviço de pesquisa de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="b5498-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="b5498-110">O processo para trabalhar com nomes de pares é diferente de trabalhar com nuvens.</span><span class="sxs-lookup"><span data-stu-id="b5498-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="b5498-111">Cada processo é descrito separadamente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b5498-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="b5498-112">Resolvendo um nome</span><span class="sxs-lookup"><span data-stu-id="b5498-112">Resolving a Name</span></span>

<span data-ttu-id="b5498-113">Um aplicativo usa [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obter o endereço IP, a porta e o protocolo para um serviço de mesmo nível registrado em outro computador.</span><span class="sxs-lookup"><span data-stu-id="b5498-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="b5498-114">A função **WSALookupServiceBegin** é usada para iniciar o processo de resolução de nomes e configurar os parâmetros e as restrições.</span><span class="sxs-lookup"><span data-stu-id="b5498-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="b5498-115">Um identificador é retornado e deve ser usado ao chamar **WSALookupServiceNext** e **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="b5498-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="b5498-116">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="b5498-116">lpqsRestrictions</span></span>

<span data-ttu-id="b5498-117">Ao resolver um nome de par, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRestrictions* referencia deve conter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b5498-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b5498-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b5498-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-119">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b5498-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="b5498-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-121">Especifica um nome de par a ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="b5498-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="b5498-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-123">Deve ser **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="b5498-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="b5498-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-125">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="b5498-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-127">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="b5498-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-129">Deve ser **ns \_ pnrpname** ou **ns \_ All**.</span><span class="sxs-lookup"><span data-stu-id="b5498-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="b5498-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-131">Deve ser o **\_ provedor NS \_ pnrpname** ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5498-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="b5498-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-133">Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5498-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="b5498-134">Se esse valor for **nulo** ou uma cadeia de caracteres vazia, a nuvem padrão, "global \_ ", será usada.</span><span class="sxs-lookup"><span data-stu-id="b5498-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="b5498-135">Caso contrário, ele deve apontar para um nome de nuvem válido.</span><span class="sxs-lookup"><span data-stu-id="b5498-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="b5498-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-137">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="b5498-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-139">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="b5498-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-141">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="b5498-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-143">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="b5498-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-145">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="b5498-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-147">Deve ser um ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5498-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="b5498-148">Se for **NULL**, serão usados valores padrão.</span><span class="sxs-lookup"><span data-stu-id="b5498-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="b5498-149">Se estiver definido, **lpBlob** apontará para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) e parâmetros específicos na estrutura **PNRPINFO** deverão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="b5498-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="b5498-150">Para obter mais informações, consulte as descrições a seguir para a estrutura PNRPINFO.</span><span class="sxs-lookup"><span data-stu-id="b5498-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="b5498-151">Estrutura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="b5498-151">PNRPINFO Structure</span></span>

<span data-ttu-id="b5498-152">Se o membro **lpBlob** da estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) for definido, os seguintes membros da estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) deverão ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b5498-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="b5498-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b5498-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-154">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b5498-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="b5498-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-156">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="b5498-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-158">Especifica o número solicitado de resoluções.</span><span class="sxs-lookup"><span data-stu-id="b5498-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="b5498-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-160">Especifica o período de tempo limite solicitado para aguardar respostas.</span><span class="sxs-lookup"><span data-stu-id="b5498-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="b5498-161">O padrão é 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="b5498-161">The default is 30 seconds.</span></span> <span data-ttu-id="b5498-162">O máximo é de 600 segundos (10 minutos).</span><span class="sxs-lookup"><span data-stu-id="b5498-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="b5498-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-164">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="b5498-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-166">Deve ser um dos valores permitidos.</span><span class="sxs-lookup"><span data-stu-id="b5498-166">Must be one of the allowed values.</span></span> <span data-ttu-id="b5498-167">O padrão é **PNRP \_ resolve \_ o \_ \_ nome de \_ \_ par de \_ processo não atual**.</span><span class="sxs-lookup"><span data-stu-id="b5498-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="b5498-168">Os valores válidos são especificados [**por \_ \_ critérios de resolução PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span><span class="sxs-lookup"><span data-stu-id="b5498-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b5498-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-170">Deve ser zero (0) ou a **\_ dica PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="b5498-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="b5498-171">O padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="b5498-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-173">Especifica o endereço IP para a dica.</span><span class="sxs-lookup"><span data-stu-id="b5498-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="b5498-174">A dica é usada ao tentar localizar o nome de par mais próximo.</span><span class="sxs-lookup"><span data-stu-id="b5498-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="b5498-175">O formato da dica é um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="b5498-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="b5498-176">Se **saHint** não for especificado ao localizar o nome de par mais próximo, será usado, em vez disso, um endereço IPv6 do computador local.</span><span class="sxs-lookup"><span data-stu-id="b5498-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="b5498-177">Esse membro será ignorado se o **dwFlags** não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="b5498-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**Nome do seu**</span><span class="sxs-lookup"><span data-stu-id="b5498-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-179">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="b5498-180">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="b5498-180">dwControlFlags</span></span>

<span data-ttu-id="b5498-181">Os seguintes \_ sinalizadores de retorno Lup \_ \* são suportados pelo PNRP:</span><span class="sxs-lookup"><span data-stu-id="b5498-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="b5498-182">Valor</span><span class="sxs-lookup"><span data-stu-id="b5498-182">Value</span></span>                | <span data-ttu-id="b5498-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5498-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="b5498-184">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="b5498-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="b5498-185">Retorna um nome e um contexto.</span><span class="sxs-lookup"><span data-stu-id="b5498-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="b5498-186">\_Comentário de retorno do Lup \_</span><span class="sxs-lookup"><span data-stu-id="b5498-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="b5498-187">Retorna um comentário associado a um nome.</span><span class="sxs-lookup"><span data-stu-id="b5498-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="b5498-188">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="b5498-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="b5498-189">Retorna um endereço associado a um nome.</span><span class="sxs-lookup"><span data-stu-id="b5498-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="b5498-190">Enumerando nuvens de rede</span><span class="sxs-lookup"><span data-stu-id="b5498-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="b5498-191">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="b5498-191">lpqsRestrictions</span></span>

<span data-ttu-id="b5498-192">Ao enumerar nuvens, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRestrictions* referencia deve conter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b5498-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b5498-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b5498-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-194">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b5498-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="b5498-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-196">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5498-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="b5498-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-198">Deve ser **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="b5498-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="b5498-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-200">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="b5498-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-202">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="b5498-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-204">Deve ser **ns \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="b5498-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="b5498-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-206">Deve ser o **\_ provedor NS \_ PNRPCLOUD** ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="b5498-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-208">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="b5498-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-210">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="b5498-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-212">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="b5498-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-214">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="b5498-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-216">Reservado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5498-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="b5498-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-218">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b5498-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="b5498-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-220">Ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) .</span><span class="sxs-lookup"><span data-stu-id="b5498-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="b5498-221">Se **lpBlob** for **NULL**, todas as nuvens serão enumeradas.</span><span class="sxs-lookup"><span data-stu-id="b5498-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="b5498-222">Estrutura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="b5498-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="b5498-223">Ao enumerar nuvens, os seguintes membros da estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) devem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b5498-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="b5498-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b5498-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-225">Especifica o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b5498-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nuvem**</span><span class="sxs-lookup"><span data-stu-id="b5498-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-227">Aponta para uma estrutura que especifica os critérios que você pode usar para filtrar os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b5498-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="b5498-228">O membro **Cloud. Scope** pode ser **\_ \_ um escopo PNRP**, **\_ \_ escopo global PNRP**, **\_ \_ \_ escopo local do site PNRP** ou **\_ \_ \_ escopo local do link do PNRP**.</span><span class="sxs-lookup"><span data-stu-id="b5498-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="b5498-229">Se **o \_ escopo \_ PNRP** for especificado, todas as nuvens serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="b5498-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="b5498-230">Caso contrário, somente nuvens que correspondam à **nuvem. Scope** serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="b5498-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5498-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**encloudstate**</span><span class="sxs-lookup"><span data-stu-id="b5498-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="b5498-232">Reservado, deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="b5498-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="b5498-233">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="b5498-233">dwControlFlags</span></span>

<span data-ttu-id="b5498-234">Os seguintes \_ sinalizadores de retorno Lup \_ \* são suportados pelo PNRP:</span><span class="sxs-lookup"><span data-stu-id="b5498-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="b5498-235">Valor</span><span class="sxs-lookup"><span data-stu-id="b5498-235">Value</span></span>             | <span data-ttu-id="b5498-236">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5498-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b5498-237">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="b5498-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="b5498-238">Retorna um nome e um contexto.</span><span class="sxs-lookup"><span data-stu-id="b5498-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="b5498-239">\_blob de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="b5498-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="b5498-240">Retorna o [blob](pnrp-and-blob.md) associado a essa nuvem.</span><span class="sxs-lookup"><span data-stu-id="b5498-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5498-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5498-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5498-242">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="b5498-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="b5498-243">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="b5498-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="b5498-244">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="b5498-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="b5498-245">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="b5498-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="b5498-246">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="b5498-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="b5498-247">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="b5498-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="b5498-248">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="b5498-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="b5498-249">Códigos de erro NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="b5498-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



