---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_CNAMEType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de nome canônico (CNAME).
ms.assetid: b5a5e14a-fb30-4cdf-90d0-7ef446350ac6
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceb65a76002651e98dd8751e0a5c0c56aca3e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918453"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="2a02a-106">Método CreateInstanceFromPropertyData da \_ classe cnametype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2a02a-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="2a02a-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de nome CANÔNICO (CNAME).</span><span class="sxs-lookup"><span data-stu-id="2a02a-107">The **CreateInstanceFromPropertyData** method instantiates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a02a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a02a-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2a02a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a02a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a02a-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="2a02a-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="2a02a-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="2a02a-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="2a02a-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="2a02a-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="2a02a-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="2a02a-117">Class of the RR.</span></span> <span data-ttu-id="2a02a-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="2a02a-118">Default value is 1.</span></span> <span data-ttu-id="2a02a-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="2a02a-119">The following values are valid.</span></span>



| <span data-ttu-id="2a02a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2a02a-120">Value</span></span>                                                                                                | <span data-ttu-id="2a02a-121">Significado</span><span class="sxs-lookup"><span data-stu-id="2a02a-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="2a02a-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2a02a-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2a02a-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="2a02a-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="2a02a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2a02a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2a02a-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="2a02a-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="2a02a-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2a02a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2a02a-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="2a02a-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="2a02a-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="2a02a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2a02a-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="2a02a-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="2a02a-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="2a02a-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2a02a-132">*Primárioname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-132">*PrimaryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-133">Nome principal do RR CNAME.</span><span class="sxs-lookup"><span data-stu-id="2a02a-133">Primary name of the CNAME RR.</span></span>

</dd> <dt>

<span data-ttu-id="2a02a-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2a02a-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="2a02a-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a02a-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a02a-136">Return value</span></span>

<span data-ttu-id="2a02a-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2a02a-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a02a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a02a-138">Requirements</span></span>



| <span data-ttu-id="2a02a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a02a-139">Requirement</span></span> | <span data-ttu-id="2a02a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2a02a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a02a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a02a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2a02a-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2a02a-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2a02a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a02a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2a02a-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a02a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2a02a-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a02a-145">Namespace</span></span><br/>                | <span data-ttu-id="2a02a-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="2a02a-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2a02a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2a02a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a02a-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a02a-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a02a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a02a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a02a-150">**\_Cnametype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2a02a-150">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="2a02a-151">**Método Modify da classe MicrosoftDNS \_ cnametype**</span><span class="sxs-lookup"><span data-stu-id="2a02a-151">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="2a02a-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2a02a-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





