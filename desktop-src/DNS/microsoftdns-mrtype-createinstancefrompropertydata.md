---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MRType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso Sr (renomeação da caixa de correio).
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MRType
- MicrosoftDNS_MRType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f41478d4ff59ff7999f6f3b052f203aeda78803
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824434"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="83214-106">Método CreateInstanceFromPropertyData da \_ classe MRType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="83214-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="83214-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso Sr (renomeação da caixa de correio).</span><span class="sxs-lookup"><span data-stu-id="83214-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="83214-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83214-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="83214-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83214-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83214-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83214-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="83214-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="83214-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83214-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="83214-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="83214-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83214-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="83214-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="83214-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="83214-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="83214-117">Class of the RR.</span></span> <span data-ttu-id="83214-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="83214-118">Default value is 1.</span></span> <span data-ttu-id="83214-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="83214-119">The following values are valid.</span></span>



| <span data-ttu-id="83214-120">Valor</span><span class="sxs-lookup"><span data-stu-id="83214-120">Value</span></span>                                                                                                | <span data-ttu-id="83214-121">Significado</span><span class="sxs-lookup"><span data-stu-id="83214-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="83214-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="83214-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="83214-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="83214-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="83214-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="83214-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="83214-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="83214-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="83214-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="83214-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="83214-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="83214-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="83214-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="83214-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="83214-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="83214-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="83214-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="83214-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="83214-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="83214-132">*MRMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83214-132">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-133">FQDN que especifica uma caixa de correio que é a renomeação correta da caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="83214-133">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="83214-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="83214-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="83214-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="83214-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83214-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83214-136">Return value</span></span>

<span data-ttu-id="83214-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="83214-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="83214-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83214-138">Requirements</span></span>



| <span data-ttu-id="83214-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="83214-139">Requirement</span></span> | <span data-ttu-id="83214-140">Valor</span><span class="sxs-lookup"><span data-stu-id="83214-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83214-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83214-141">Minimum supported client</span></span><br/> | <span data-ttu-id="83214-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83214-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="83214-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83214-143">Minimum supported server</span></span><br/> | <span data-ttu-id="83214-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83214-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83214-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="83214-145">Namespace</span></span><br/>                | <span data-ttu-id="83214-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="83214-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="83214-147">MOF</span><span class="sxs-lookup"><span data-stu-id="83214-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83214-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83214-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83214-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="83214-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83214-150">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="83214-150">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="83214-151">**Método Modify da classe MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="83214-151">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="83214-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="83214-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





