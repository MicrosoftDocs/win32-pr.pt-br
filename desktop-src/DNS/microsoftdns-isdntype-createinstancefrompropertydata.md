---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_ISDNType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de ISDN.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499534"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="7b2f9-106">Método CreateInstanceFromPropertyData da \_ classe isdntype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="7b2f9-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="7b2f9-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de ISDN.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2f9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b2f9-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7b2f9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b2f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2f9-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-117">Class of the RR.</span></span> <span data-ttu-id="7b2f9-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-118">Default value is 1.</span></span> <span data-ttu-id="7b2f9-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-119">The following values are valid.</span></span>



| <span data-ttu-id="7b2f9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b2f9-120">Value</span></span>                                                                                                | <span data-ttu-id="7b2f9-121">Significado</span><span class="sxs-lookup"><span data-stu-id="7b2f9-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="7b2f9-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f9-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7b2f9-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="7b2f9-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="7b2f9-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f9-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7b2f9-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="7b2f9-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="7b2f9-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f9-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7b2f9-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="7b2f9-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="7b2f9-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f9-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7b2f9-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="7b2f9-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7b2f9-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-132">*ISDNNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-133">Número ISDN e DDI do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-134">*Subendereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-135">Subendereço do proprietário, se definido.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="7b2f9-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2f9-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2f9-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b2f9-138">Return value</span></span>

<span data-ttu-id="7b2f9-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7b2f9-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2f9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b2f9-140">Requirements</span></span>



| <span data-ttu-id="7b2f9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b2f9-141">Requirement</span></span> | <span data-ttu-id="7b2f9-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7b2f9-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2f9-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b2f9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7b2f9-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b2f9-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7b2f9-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b2f9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7b2f9-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b2f9-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b2f9-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b2f9-147">Namespace</span></span><br/>                | <span data-ttu-id="7b2f9-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="7b2f9-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7b2f9-149">MOF</span><span class="sxs-lookup"><span data-stu-id="7b2f9-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b2f9-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b2f9-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b2f9-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b2f9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2f9-152">**\_Isdntype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7b2f9-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="7b2f9-153">**Método Modify da \_ classe isdntype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7b2f9-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="7b2f9-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7b2f9-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





