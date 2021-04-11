---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_X25Type
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de X. 25 (X25).
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009515"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="66d99-106">Método CreateInstanceFromPropertyData da \_ classe X25Type MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="66d99-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="66d99-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="66d99-107">The **CreateInstanceFromPropertyData** method instantiates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d99-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66d99-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="66d99-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66d99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d99-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66d99-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="66d99-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="66d99-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66d99-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="66d99-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="66d99-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66d99-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="66d99-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="66d99-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66d99-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="66d99-117">Class of the RR.</span></span> <span data-ttu-id="66d99-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="66d99-118">Default value is 1.</span></span> <span data-ttu-id="66d99-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="66d99-119">The following values are valid.</span></span>



| <span data-ttu-id="66d99-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66d99-120">Value</span></span>                                                                                                | <span data-ttu-id="66d99-121">Significado</span><span class="sxs-lookup"><span data-stu-id="66d99-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="66d99-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="66d99-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="66d99-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="66d99-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="66d99-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="66d99-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="66d99-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="66d99-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="66d99-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="66d99-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="66d99-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="66d99-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="66d99-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="66d99-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="66d99-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="66d99-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="66d99-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66d99-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="66d99-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="66d99-132">*PSDNAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66d99-132">*PSDNAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-133">Endereço PSDN do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="66d99-133">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="66d99-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="66d99-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="66d99-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="66d99-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d99-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66d99-136">Return value</span></span>

<span data-ttu-id="66d99-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="66d99-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d99-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d99-138">Requirements</span></span>



| <span data-ttu-id="66d99-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d99-139">Requirement</span></span> | <span data-ttu-id="66d99-140">Valor</span><span class="sxs-lookup"><span data-stu-id="66d99-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d99-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d99-141">Minimum supported client</span></span><br/> | <span data-ttu-id="66d99-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="66d99-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="66d99-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d99-143">Minimum supported server</span></span><br/> | <span data-ttu-id="66d99-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66d99-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66d99-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="66d99-145">Namespace</span></span><br/>                | <span data-ttu-id="66d99-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="66d99-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="66d99-147">MOF</span><span class="sxs-lookup"><span data-stu-id="66d99-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66d99-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66d99-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d99-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="66d99-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d99-150">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="66d99-150">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="66d99-151">**Método Modify da classe MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="66d99-151">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="66d99-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="66d99-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





