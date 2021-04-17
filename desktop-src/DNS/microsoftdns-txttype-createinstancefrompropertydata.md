---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_TXTType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de texto (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749873"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="7178a-106">Método CreateInstanceFromPropertyData da \_ classe TXTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="7178a-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="7178a-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="7178a-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7178a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7178a-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7178a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7178a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7178a-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7178a-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="7178a-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7178a-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7178a-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="7178a-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7178a-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7178a-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="7178a-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="7178a-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7178a-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="7178a-117">Class of the RR.</span></span> <span data-ttu-id="7178a-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="7178a-118">Default value is 1.</span></span> <span data-ttu-id="7178a-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="7178a-119">The following values are valid.</span></span>



| <span data-ttu-id="7178a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7178a-120">Value</span></span>                                                                                                | <span data-ttu-id="7178a-121">Significado</span><span class="sxs-lookup"><span data-stu-id="7178a-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="7178a-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7178a-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7178a-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="7178a-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="7178a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7178a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7178a-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="7178a-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="7178a-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7178a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7178a-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="7178a-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="7178a-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="7178a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7178a-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="7178a-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7178a-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7178a-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="7178a-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7178a-132">*DescriptiveText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7178a-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-133">Texto descritivo, a semântica que depende do domínio do proprietário.</span><span class="sxs-lookup"><span data-stu-id="7178a-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="7178a-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="7178a-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7178a-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="7178a-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7178a-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7178a-136">Return value</span></span>

<span data-ttu-id="7178a-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7178a-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7178a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7178a-138">Requirements</span></span>



| <span data-ttu-id="7178a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7178a-139">Requirement</span></span> | <span data-ttu-id="7178a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7178a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7178a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7178a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7178a-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7178a-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7178a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7178a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7178a-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7178a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7178a-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="7178a-145">Namespace</span></span><br/>                | <span data-ttu-id="7178a-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="7178a-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7178a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7178a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7178a-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7178a-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7178a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="7178a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7178a-150">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="7178a-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="7178a-151">**Método Modify da classe MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="7178a-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="7178a-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7178a-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





