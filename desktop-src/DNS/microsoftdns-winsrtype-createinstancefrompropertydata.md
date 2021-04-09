---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_WINSRType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de pesquisa inversa WINS (WINSr).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085906"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="ecdd3-106">Método CreateInstanceFromPropertyData da \_ classe WINSRType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ecdd3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="ecdd3-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de pesquisa inversa WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="ecdd3-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecdd3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecdd3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ecdd3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecdd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecdd3-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-117">Class of the RR.</span></span> <span data-ttu-id="ecdd3-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-118">Default value is 1.</span></span> <span data-ttu-id="ecdd3-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-119">The following values are valid.</span></span>



| <span data-ttu-id="ecdd3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ecdd3-120">Value</span></span>                                                                                                | <span data-ttu-id="ecdd3-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ecdd3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ecdd3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ecdd3-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="ecdd3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ecdd3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ecdd3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ecdd3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ecdd3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ecdd3-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="ecdd3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ecdd3-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ecdd3-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ecdd3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ecdd3-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-132">*MappingFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-133">Sinalizador de mapeamento WINSr que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ecdd3-134">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-135">*LookupTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-136">Tempo limite, em segundos, para um servidor DNS usando a pesquisa inversa do WINS.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-137">*CacheTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-138">Tempo, em segundos, um servidor DNS usando a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-139">*ResultDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-140">Nome de domínio a ser anexado aos nomes NetBIOS retornados.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="ecdd3-141">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ecdd3-142">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecdd3-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecdd3-143">Return value</span></span>

<span data-ttu-id="ecdd3-144">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ecdd3-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecdd3-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecdd3-145">Requirements</span></span>



| <span data-ttu-id="ecdd3-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecdd3-146">Requirement</span></span> | <span data-ttu-id="ecdd3-147">Valor</span><span class="sxs-lookup"><span data-stu-id="ecdd3-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdd3-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecdd3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ecdd3-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ecdd3-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ecdd3-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecdd3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ecdd3-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecdd3-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ecdd3-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ecdd3-152">Namespace</span></span><br/>                | <span data-ttu-id="ecdd3-153">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ecdd3-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ecdd3-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ecdd3-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecdd3-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd3-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecdd3-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecdd3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecdd3-157">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="ecdd3-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="ecdd3-158">**Método Modify da classe MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="ecdd3-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ecdd3-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ecdd3-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





