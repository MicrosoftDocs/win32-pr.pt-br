---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_PTRType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de ponteiro (PTR).
ms.assetid: ff8beaca-fa0d-4294-8dab-3aa62baa3fe3
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6123b503fff1548b7fee3f643920b49ebacf636c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085527"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="d0c21-106">Método CreateInstanceFromPropertyData da \_ classe PTRType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d0c21-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="d0c21-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="d0c21-107">The **CreateInstanceFromPropertyData** method instantiates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c21-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0c21-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d0c21-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0c21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c21-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="d0c21-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0c21-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="d0c21-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0c21-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="d0c21-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0c21-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="d0c21-117">Class of the RR.</span></span> <span data-ttu-id="d0c21-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="d0c21-118">Default value is 1.</span></span> <span data-ttu-id="d0c21-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="d0c21-119">The following values are valid.</span></span>



| <span data-ttu-id="d0c21-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d0c21-120">Value</span></span>                                                                                                | <span data-ttu-id="d0c21-121">Significado</span><span class="sxs-lookup"><span data-stu-id="d0c21-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d0c21-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c21-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d0c21-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="d0c21-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d0c21-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c21-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d0c21-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="d0c21-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d0c21-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c21-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d0c21-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="d0c21-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d0c21-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c21-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d0c21-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="d0c21-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d0c21-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="d0c21-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d0c21-132">*PTRDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-132">*PTRDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-133">Cadeia de caracteres que representa o endereço de nome de domínio do registro PTR.</span><span class="sxs-lookup"><span data-stu-id="d0c21-133">String representing the domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="d0c21-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d0c21-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="d0c21-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c21-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0c21-136">Return value</span></span>

<span data-ttu-id="d0c21-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d0c21-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c21-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0c21-138">Requirements</span></span>



| <span data-ttu-id="d0c21-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0c21-139">Requirement</span></span> | <span data-ttu-id="d0c21-140">Valor</span><span class="sxs-lookup"><span data-stu-id="d0c21-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c21-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0c21-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c21-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d0c21-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d0c21-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0c21-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c21-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d0c21-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0c21-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c21-145">Namespace</span></span><br/>                | <span data-ttu-id="d0c21-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="d0c21-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d0c21-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d0c21-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0c21-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0c21-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c21-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0c21-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c21-150">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="d0c21-150">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="d0c21-151">**Método Modify da classe MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="d0c21-151">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="d0c21-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d0c21-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





