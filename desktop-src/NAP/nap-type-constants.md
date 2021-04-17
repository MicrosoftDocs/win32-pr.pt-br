---
title: Constantes de tipo NAP (NapTypes. h)
description: As constantes de NAP a seguir são definidas.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766249"
---
# <a name="nap-type-constants"></a><span data-ttu-id="103f0-103">Constantes de tipo NAP</span><span class="sxs-lookup"><span data-stu-id="103f0-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="103f0-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="103f0-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="103f0-105">As constantes de NAP a seguir são definidas.</span><span class="sxs-lookup"><span data-stu-id="103f0-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="103f0-106">As constantes de NAP a seguir são definidas em NapTypes. h:</span><span class="sxs-lookup"><span data-stu-id="103f0-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="103f0-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-108">0x64</span><span class="sxs-lookup"><span data-stu-id="103f0-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="103f0-109">O número máximo de objetos TLV (tipo-tamanho-valor) [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associados a um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="103f0-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="103f0-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="103f0-112">O tamanho máximo, em bytes, de um objeto [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associado a um pacote de [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh)(declaração de integridade).</span><span class="sxs-lookup"><span data-stu-id="103f0-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-114">0xC</span><span class="sxs-lookup"><span data-stu-id="103f0-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="103f0-115">O tamanho mínimo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="103f0-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="103f0-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="103f0-118">O tamanho máximo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="103f0-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="103f0-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-120">maxSoHAttributeSize/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="103f0-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="103f0-121">O número máximo de valores DWORD associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="103f0-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="103f0-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-123">maxSoHAttributeSize/0x4</span><span class="sxs-lookup"><span data-stu-id="103f0-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="103f0-124">O número máximo de endereços IPv4 associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="103f0-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="103f0-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-126">maxSoHAttributeSize/0x10</span><span class="sxs-lookup"><span data-stu-id="103f0-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="103f0-127">O número máximo de endereços IPv6 associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="103f0-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span><span class="sxs-lookup"><span data-stu-id="103f0-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-129">0x400</span><span class="sxs-lookup"><span data-stu-id="103f0-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="103f0-130">O comprimento máximo de uma cadeia de caracteres especificada pela estrutura de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="103f0-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span><span class="sxs-lookup"><span data-stu-id="103f0-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-132">(maxStringLength + 1) \* sizeof (WCHAR)</span><span class="sxs-lookup"><span data-stu-id="103f0-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="103f0-133">O comprimento máximo, em bytes, de uma cadeia de caracteres especificada pela estrutura de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="103f0-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-135">0x14</span><span class="sxs-lookup"><span data-stu-id="103f0-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="103f0-136">O número máximo de entidades de integridade do sistema, como SHVs e SHAs.</span><span class="sxs-lookup"><span data-stu-id="103f0-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-138">\[intervalo (0, maxSystemHealthEntityCount)\]</span><span class="sxs-lookup"><span data-stu-id="103f0-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="103f0-139">O intervalo de valores possíveis para o número de entidades de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="103f0-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-141">0x14</span><span class="sxs-lookup"><span data-stu-id="103f0-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="103f0-142">O número máximo de entidades de imposição, como QECs.</span><span class="sxs-lookup"><span data-stu-id="103f0-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-144">\[intervalo (0, maxEnforcerCount)\]</span><span class="sxs-lookup"><span data-stu-id="103f0-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="103f0-145">O intervalo de valores possíveis para o número de entidades de imposição.</span><span class="sxs-lookup"><span data-stu-id="103f0-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="103f0-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="103f0-148">O tamanho máximo, em bytes, de uma estrutura [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="103f0-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span><span class="sxs-lookup"><span data-stu-id="103f0-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-150">0x14</span><span class="sxs-lookup"><span data-stu-id="103f0-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="103f0-151">O número máximo de objetos [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) associados a uma entidade de imposição.</span><span class="sxs-lookup"><span data-stu-id="103f0-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span><span class="sxs-lookup"><span data-stu-id="103f0-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="103f0-154">O número máximo de conexões SoH em cache para todas as entidades de integridade do sistema e imposição.</span><span class="sxs-lookup"><span data-stu-id="103f0-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="103f0-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-156">0x1</span><span class="sxs-lookup"><span data-stu-id="103f0-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="103f0-157">Especifica que um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)é devido a uma nova solicitação, não a uma solicitação armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="103f0-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="103f0-158">Esse sinalizador é usado pelo agente NAP em um objeto [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="103f0-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span><span class="sxs-lookup"><span data-stu-id="103f0-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-160">0x1</span><span class="sxs-lookup"><span data-stu-id="103f0-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="103f0-161">Especifica que a correção é necessária.</span><span class="sxs-lookup"><span data-stu-id="103f0-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="103f0-162">Esse sinalizador é usado por um SHA.</span><span class="sxs-lookup"><span data-stu-id="103f0-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span><span class="sxs-lookup"><span data-stu-id="103f0-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-164">0x5</span><span class="sxs-lookup"><span data-stu-id="103f0-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="103f0-165">O número de categorias de falha contidas em uma estrutura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="103f0-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span><span class="sxs-lookup"><span data-stu-id="103f0-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-167">0x1</span><span class="sxs-lookup"><span data-stu-id="103f0-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="103f0-168">O componente é um cliente de imposição de quarentena (QEC) que envia um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) em banda durante a autenticação de conexão.</span><span class="sxs-lookup"><span data-stu-id="103f0-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="103f0-169">Esse valor não é usado por SHAs e SHVs.</span><span class="sxs-lookup"><span data-stu-id="103f0-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span><span class="sxs-lookup"><span data-stu-id="103f0-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-171">0x2</span><span class="sxs-lookup"><span data-stu-id="103f0-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="103f0-172">O componente é um QEC que implementa o [**INapCertRelyingParty**](inapcertrelyingparty.md) e deve interagir com o HCS (servidor de certificado de integridade) para obter um certificado de integridade.</span><span class="sxs-lookup"><span data-stu-id="103f0-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="103f0-173">Esse valor não é usado por SHAs e SHVs.</span><span class="sxs-lookup"><span data-stu-id="103f0-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="103f0-174">As constantes de NAP a seguir são definidas em NapEnforcementClient. h.</span><span class="sxs-lookup"><span data-stu-id="103f0-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="103f0-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="103f0-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="103f0-177">O tamanho máximo padrão, em bytes, de um pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="103f0-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="103f0-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="103f0-180">O tamanho máximo possível, em bytes, de um pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="103f0-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="103f0-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="103f0-183">O menor tamanho máximo possível, em bytes, de um pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="103f0-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="103f0-184">O tamanho real do pacote SoH pode ser menor que **minProtocolMaxSize**.</span><span class="sxs-lookup"><span data-stu-id="103f0-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="103f0-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="103f0-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103f0-186">intervalo (minProtocolMaxSize, maxProtocolMaxSize)</span><span class="sxs-lookup"><span data-stu-id="103f0-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="103f0-187">O intervalo de valores possíveis para o tamanho máximo de um pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="103f0-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="103f0-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="103f0-188">Requirements</span></span>



| <span data-ttu-id="103f0-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="103f0-189">Requirement</span></span> | <span data-ttu-id="103f0-190">Valor</span><span class="sxs-lookup"><span data-stu-id="103f0-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103f0-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103f0-191">Minimum supported client</span></span><br/> | <span data-ttu-id="103f0-192">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="103f0-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="103f0-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103f0-193">Minimum supported server</span></span><br/> | <span data-ttu-id="103f0-194">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="103f0-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="103f0-195">parâmetro</span><span class="sxs-lookup"><span data-stu-id="103f0-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="103f0-196"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="103f0-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103f0-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="103f0-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103f0-198">**Constantes de NAP**</span><span class="sxs-lookup"><span data-stu-id="103f0-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





