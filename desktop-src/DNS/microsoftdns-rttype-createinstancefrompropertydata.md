---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_RTType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de rota por meio de (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_RTType
- MicrosoftDNS_RTType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499429"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="46cd8-106">Método CreateInstanceFromPropertyData da \_ classe RTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="46cd8-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="46cd8-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de rota por meio de (RT).</span><span class="sxs-lookup"><span data-stu-id="46cd8-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cd8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46cd8-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="46cd8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46cd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cd8-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="46cd8-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="46cd8-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="46cd8-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="46cd8-117">Class of the RR.</span></span> <span data-ttu-id="46cd8-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="46cd8-118">Default value is 1.</span></span> <span data-ttu-id="46cd8-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="46cd8-119">The following values are valid.</span></span>



| <span data-ttu-id="46cd8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="46cd8-120">Value</span></span>                                                                                                | <span data-ttu-id="46cd8-121">Significado</span><span class="sxs-lookup"><span data-stu-id="46cd8-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="46cd8-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd8-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="46cd8-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="46cd8-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="46cd8-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd8-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="46cd8-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="46cd8-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="46cd8-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd8-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="46cd8-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="46cd8-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="46cd8-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd8-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="46cd8-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="46cd8-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="46cd8-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="46cd8-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-132">*Preferência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-133">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="46cd8-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="46cd8-134">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="46cd8-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-135">*IntermediateHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-136">FQDN que especifica um host para servir como intermediário para atingir o host especificado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="46cd8-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="46cd8-137">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd8-138">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="46cd8-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cd8-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46cd8-139">Return value</span></span>

<span data-ttu-id="46cd8-140">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="46cd8-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46cd8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cd8-141">Requirements</span></span>



| <span data-ttu-id="46cd8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cd8-142">Requirement</span></span> | <span data-ttu-id="46cd8-143">Valor</span><span class="sxs-lookup"><span data-stu-id="46cd8-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46cd8-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cd8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="46cd8-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="46cd8-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="46cd8-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cd8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="46cd8-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46cd8-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46cd8-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="46cd8-148">Namespace</span></span><br/>                | <span data-ttu-id="46cd8-149">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="46cd8-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="46cd8-150">MOF</span><span class="sxs-lookup"><span data-stu-id="46cd8-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46cd8-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46cd8-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cd8-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="46cd8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cd8-153">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="46cd8-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="46cd8-154">**Método Modify da classe MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="46cd8-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="46cd8-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="46cd8-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





