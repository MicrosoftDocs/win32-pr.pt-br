---
description: O PNRP usa a função WSALookupServiceNext para fazer a correspondência de consultas especificadas em uma chamada anterior para WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768450"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="984ea-103">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="984ea-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="984ea-104">O PNRP usa a função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para fazer a correspondência de consultas especificadas em uma chamada anterior para **WSALookupServiceBegin**.</span><span class="sxs-lookup"><span data-stu-id="984ea-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="984ea-105">Os resultados da função **WSALookupServiceNext** são determinados pelas configurações na estrutura **WSAQUERYSET** passada na chamada de função **WSALookupServiceBegin** inicial.</span><span class="sxs-lookup"><span data-stu-id="984ea-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="984ea-106">Essa função é usada para executar as duas funções a seguir:</span><span class="sxs-lookup"><span data-stu-id="984ea-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="984ea-107">Resolvendo um nome de par para uma lista de endereços</span><span class="sxs-lookup"><span data-stu-id="984ea-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="984ea-108">Enumerando nuvens de rede</span><span class="sxs-lookup"><span data-stu-id="984ea-108">Enumerating network clouds</span></span>

<span data-ttu-id="984ea-109">Usando [**WSANSPIoctl**](winsock-nsp-reference-links.md), o serviço de pesquisa pode ser usado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="984ea-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="984ea-110">Para obter informações sobre como usar as funções de serviço de pesquisa de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="984ea-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="984ea-111">A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) é bloqueada mesmo se **WSANSPIoctl** for chamado.</span><span class="sxs-lookup"><span data-stu-id="984ea-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="984ea-112">Antes de chamar **WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.</span><span class="sxs-lookup"><span data-stu-id="984ea-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="984ea-113">Resolvendo um nome de par para uma lista de endereços</span><span class="sxs-lookup"><span data-stu-id="984ea-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="984ea-114">Ao resolver um nome de par para uma lista de endereços, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retornada no parâmetro *lpqsResults* contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="984ea-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="984ea-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="984ea-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-116">Retorna o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="984ea-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="984ea-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-118">Retorna um nome de par — **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="984ea-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="984ea-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-120">Retorna **SVCID \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="984ea-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="984ea-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-122">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="984ea-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-124">Retorna um comentário — se **Lup \_ retornar o \_ Comentário**, **Lup \_ retornará \_ All** ou **NULL** será especificado.</span><span class="sxs-lookup"><span data-stu-id="984ea-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="984ea-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-126">Retorna o **ns \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="984ea-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="984ea-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-128">Retorna **o \_ provedor NS \_ pnrpname**.</span><span class="sxs-lookup"><span data-stu-id="984ea-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="984ea-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-130">Retorna o nome da nuvem **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="984ea-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="984ea-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-132">Retorna zero (0).</span><span class="sxs-lookup"><span data-stu-id="984ea-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="984ea-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="984ea-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-134">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="984ea-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-136">Retorna o número de entradas na matriz de \_ informações de CSADDR se **Lup \_ retornar \_ addr**, **Lup \_ retornar \_ todos** ou **NULL** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="984ea-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="984ea-137">Esse valor e as informações em **lpcsaBuffer** são os principais bits de informações retornados nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="984ea-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="984ea-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-139">Retorna um ponteiro para uma matriz de \_ estruturas de informações CSADDR se **Lup \_ retornar \_ addr**, **Lup \_ retornar \_ todos** ou **NULL** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="984ea-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="984ea-140">Esse buffer e o valor em **dwNumberOfCsAddrs** são os principais bits de informações retornados nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="984ea-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="984ea-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-142">Retorna zero (0).</span><span class="sxs-lookup"><span data-stu-id="984ea-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="984ea-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="984ea-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-144">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="984ea-145">Enumerando nuvens de rede</span><span class="sxs-lookup"><span data-stu-id="984ea-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="984ea-146">Ao enumerar nuvens, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retornada no parâmetro *lpqsResults* contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="984ea-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="984ea-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="984ea-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-148">Retorna o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="984ea-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="984ea-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-150">Retorna um nome de nuvem — **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.</span><span class="sxs-lookup"><span data-stu-id="984ea-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="984ea-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-152">Retorna **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="984ea-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="984ea-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-154">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="984ea-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-156">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="984ea-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-158">Retorna **ns \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="984ea-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="984ea-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-160">Retorna **\_ \_ PNRPCLOUD do provedor NS**.</span><span class="sxs-lookup"><span data-stu-id="984ea-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="984ea-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-162">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="984ea-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-164">Retorna zero (0).</span><span class="sxs-lookup"><span data-stu-id="984ea-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="984ea-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="984ea-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-166">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="984ea-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-168">Retorna zero (0).</span><span class="sxs-lookup"><span data-stu-id="984ea-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="984ea-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="984ea-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-170">Retorna **NULL**.</span><span class="sxs-lookup"><span data-stu-id="984ea-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="984ea-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-172">Retorna zero (0).</span><span class="sxs-lookup"><span data-stu-id="984ea-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="984ea-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="984ea-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-174">Retorna um ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) – se **Lup \_ retornar \_ blob**, **Lup \_ retornará \_ All** ou **null** será especificado.</span><span class="sxs-lookup"><span data-stu-id="984ea-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="984ea-175">Estrutura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="984ea-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="984ea-176">Ao enumerar nomes de nuvem, os seguintes valores são retornados na estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="984ea-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="984ea-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="984ea-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-178">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="984ea-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nuvem**</span><span class="sxs-lookup"><span data-stu-id="984ea-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-180">O valor real da nuvem.</span><span class="sxs-lookup"><span data-stu-id="984ea-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**encloudstate**</span><span class="sxs-lookup"><span data-stu-id="984ea-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-182">O estado atual de uma nuvem.</span><span class="sxs-lookup"><span data-stu-id="984ea-182">The current state of a cloud.</span></span> <span data-ttu-id="984ea-183">[**PNRP \_ \_Estado da nuvem**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) especifica os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="984ea-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="984ea-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span><span class="sxs-lookup"><span data-stu-id="984ea-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="984ea-185">Indica que um nome de nuvem é válido em uma rede ou somente válido em um computador atual.</span><span class="sxs-lookup"><span data-stu-id="984ea-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="984ea-186">[**PNRP \_ \_Sinalizadores de nuvem**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) especifica os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="984ea-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="984ea-187">Alguns nomes de nuvem são válidos em qualquer computador na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="984ea-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="984ea-188">Outros nomes de nuvem são válidos somente em um computador atual e podem ser válidos somente por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="984ea-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="984ea-189">Se **enCloudFlags** for definido como **\_ nome de nuvem PNRP \_ \_ local,** o nome só será válido localmente.</span><span class="sxs-lookup"><span data-stu-id="984ea-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="984ea-190">Se **enCloudFlags** não for definido, o nome da nuvem poderá ser transferido para outros computadores.</span><span class="sxs-lookup"><span data-stu-id="984ea-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="984ea-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="984ea-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="984ea-192">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="984ea-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="984ea-193">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="984ea-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="984ea-194">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="984ea-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="984ea-195">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="984ea-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="984ea-196">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="984ea-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="984ea-197">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="984ea-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="984ea-198">Códigos de erro NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="984ea-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="984ea-199">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="984ea-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



