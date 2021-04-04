---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_AType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de endereço (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AType
- MicrosoftDNS_AType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085567"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="4a4b5-106">Método CreateInstanceFromPropertyData da \_ classe AType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4a4b5-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="4a4b5-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de endereço (A).</span><span class="sxs-lookup"><span data-stu-id="4a4b5-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4b5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a4b5-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4a4b5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a4b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4b5-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-111">FQDN (nome de domínio totalmente qualificado) ou endereço IP do servidor DNS que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4a4b5-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4a4b5-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-115">FQDN do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="4a4b5-116">Não use o nome NetBIOS do proprietário.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="4a4b5-117">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-118">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-118">Class of the RR.</span></span> <span data-ttu-id="4a4b5-119">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-119">Default value is 1.</span></span> <span data-ttu-id="4a4b5-120">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-120">The following values are valid.</span></span>



| <span data-ttu-id="4a4b5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4a4b5-121">Value</span></span>                                                                                                | <span data-ttu-id="4a4b5-122">Significado</span><span class="sxs-lookup"><span data-stu-id="4a4b5-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4a4b5-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b5-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4a4b5-124">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="4a4b5-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4a4b5-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b5-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4a4b5-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4a4b5-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4a4b5-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b5-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4a4b5-128">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="4a4b5-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4a4b5-129"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b5-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4a4b5-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4a4b5-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4a4b5-131">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-132">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4a4b5-133">*IPAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-134">Cadeia de caracteres que representa o endereço IP do host.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="4a4b5-135">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4b5-136">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4b5-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a4b5-137">Return value</span></span>

<span data-ttu-id="4a4b5-138">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a4b5-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4b5-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a4b5-139">Requirements</span></span>



| <span data-ttu-id="4a4b5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a4b5-140">Requirement</span></span> | <span data-ttu-id="4a4b5-141">Valor</span><span class="sxs-lookup"><span data-stu-id="4a4b5-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4b5-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a4b5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4b5-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4a4b5-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4a4b5-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a4b5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4b5-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a4b5-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a4b5-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a4b5-146">Namespace</span></span><br/>                | <span data-ttu-id="4a4b5-147">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="4a4b5-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4a4b5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="4a4b5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a4b5-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b5-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a4b5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a4b5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4b5-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4a4b5-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="4a4b5-152">**Método Modify da classe MicrosoftDNS \_ AType**</span><span class="sxs-lookup"><span data-stu-id="4a4b5-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





