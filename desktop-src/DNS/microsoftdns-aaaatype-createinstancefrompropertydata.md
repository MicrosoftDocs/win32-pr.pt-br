---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_AAAAType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de endereço IPv6 (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9232506b52795521300e827701f685e351d8ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499376"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="8f780-106">Método CreateInstanceFromPropertyData da \_ classe aaaatype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8f780-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="8f780-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de endereço IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="8f780-107">The **CreateInstanceFromPropertyData** method instantiates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f780-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f780-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8f780-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f780-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f780-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f780-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="8f780-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8f780-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f780-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="8f780-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8f780-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f780-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="8f780-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8f780-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f780-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="8f780-117">Class of the RR.</span></span> <span data-ttu-id="8f780-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="8f780-118">Default value is 1.</span></span> <span data-ttu-id="8f780-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="8f780-119">The following values are valid.</span></span>



| <span data-ttu-id="8f780-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8f780-120">Value</span></span>                                                                                                | <span data-ttu-id="8f780-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8f780-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8f780-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8f780-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8f780-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="8f780-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8f780-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8f780-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8f780-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8f780-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8f780-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8f780-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8f780-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="8f780-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8f780-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="8f780-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8f780-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="8f780-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8f780-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f780-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="8f780-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8f780-132">*IPv6Address* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f780-132">*IPv6Address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-133">Endereço IPv6 para o host.</span><span class="sxs-lookup"><span data-stu-id="8f780-133">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="8f780-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8f780-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8f780-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="8f780-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f780-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f780-136">Return value</span></span>

<span data-ttu-id="8f780-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f780-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f780-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f780-138">Requirements</span></span>



| <span data-ttu-id="8f780-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f780-139">Requirement</span></span> | <span data-ttu-id="8f780-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8f780-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f780-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f780-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8f780-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f780-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8f780-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f780-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8f780-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f780-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8f780-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f780-145">Namespace</span></span><br/>                | <span data-ttu-id="8f780-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="8f780-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8f780-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8f780-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f780-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f780-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f780-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f780-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f780-150">**MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="8f780-150">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="8f780-151">**Método Modify da classe MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="8f780-151">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="8f780-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8f780-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





