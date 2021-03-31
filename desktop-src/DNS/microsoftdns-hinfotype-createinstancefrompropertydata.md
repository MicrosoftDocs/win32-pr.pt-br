---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_HINFOType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de informações de host (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645064"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="b0bf6-106">Método CreateInstanceFromPropertyData da \_ classe HINFOType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b0bf6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="b0bf6-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de informações de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="b0bf6-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bf6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0bf6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b0bf6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0bf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0bf6-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-117">Class of the RR.</span></span> <span data-ttu-id="b0bf6-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-118">Default value is 1.</span></span> <span data-ttu-id="b0bf6-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-119">The following values are valid.</span></span>



| <span data-ttu-id="b0bf6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b0bf6-120">Value</span></span>                                                                                                | <span data-ttu-id="b0bf6-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b0bf6-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="b0bf6-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf6-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b0bf6-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="b0bf6-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="b0bf6-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf6-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b0bf6-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="b0bf6-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="b0bf6-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf6-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b0bf6-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="b0bf6-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="b0bf6-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf6-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b0bf6-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="b0bf6-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b0bf6-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-132">*CPU* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-133">Tipo de CPU do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-134">*Sistema operacional* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-135">Sistema operacional do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="b0bf6-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bf6-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0bf6-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0bf6-138">Return value</span></span>

<span data-ttu-id="b0bf6-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b0bf6-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bf6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0bf6-140">Requirements</span></span>



| <span data-ttu-id="b0bf6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0bf6-141">Requirement</span></span> | <span data-ttu-id="b0bf6-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b0bf6-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bf6-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bf6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bf6-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b0bf6-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b0bf6-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bf6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bf6-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0bf6-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0bf6-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0bf6-147">Namespace</span></span><br/>                | <span data-ttu-id="b0bf6-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="b0bf6-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b0bf6-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b0bf6-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0bf6-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf6-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bf6-151">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0bf6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bf6-152">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="b0bf6-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="b0bf6-153">**Método Modify da classe MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="b0bf6-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="b0bf6-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b0bf6-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





