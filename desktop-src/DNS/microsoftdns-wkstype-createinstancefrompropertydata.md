---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_WKSType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de serviços de Well-Known (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824553"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="790db-106">Método CreateInstanceFromPropertyData da \_ classe WKSType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="790db-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="790db-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de serviços de Well-Known (WKS).</span><span class="sxs-lookup"><span data-stu-id="790db-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="790db-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="790db-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="790db-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="790db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790db-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790db-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="790db-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="790db-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790db-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="790db-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="790db-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790db-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="790db-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="790db-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="790db-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="790db-117">Class of the RR.</span></span> <span data-ttu-id="790db-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="790db-118">Default value is 1.</span></span> <span data-ttu-id="790db-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="790db-119">The following values are valid.</span></span>



| <span data-ttu-id="790db-120">Valor</span><span class="sxs-lookup"><span data-stu-id="790db-120">Value</span></span>                                                                                                | <span data-ttu-id="790db-121">Significado</span><span class="sxs-lookup"><span data-stu-id="790db-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="790db-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="790db-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="790db-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="790db-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="790db-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="790db-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="790db-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="790db-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="790db-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="790db-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="790db-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="790db-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="790db-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="790db-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="790db-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="790db-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="790db-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="790db-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="790db-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="790db-132">*InternetAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790db-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-133">Endereço IP da Internet para o proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="790db-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="790db-134">*IPProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="790db-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-135">Cadeia de caracteres que representa o protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="790db-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="790db-136">Os valores válidos são UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="790db-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="790db-137">*Serviços* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="790db-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-138">Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (serviço bem conhecido).</span><span class="sxs-lookup"><span data-stu-id="790db-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="790db-139">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="790db-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="790db-140">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="790db-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790db-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="790db-141">Return value</span></span>

<span data-ttu-id="790db-142">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="790db-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="790db-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="790db-143">Requirements</span></span>



| <span data-ttu-id="790db-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="790db-144">Requirement</span></span> | <span data-ttu-id="790db-145">Valor</span><span class="sxs-lookup"><span data-stu-id="790db-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="790db-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="790db-146">Minimum supported client</span></span><br/> | <span data-ttu-id="790db-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="790db-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="790db-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="790db-148">Minimum supported server</span></span><br/> | <span data-ttu-id="790db-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="790db-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="790db-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="790db-150">Namespace</span></span><br/>                | <span data-ttu-id="790db-151">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="790db-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="790db-152">MOF</span><span class="sxs-lookup"><span data-stu-id="790db-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="790db-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="790db-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="790db-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="790db-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790db-155">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="790db-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="790db-156">**Método Modify da classe MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="790db-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="790db-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="790db-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





