---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_NXTType
description: O método CreateInstanceFromPropertyData instancia um próximo registro de recurso (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455415"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="ca320-106">Método CreateInstanceFromPropertyData da \_ classe NXTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ca320-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="ca320-107">O método **CreateInstanceFromPropertyData** instancia um próximo registro de recurso (NXT).</span><span class="sxs-lookup"><span data-stu-id="ca320-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca320-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca320-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ca320-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca320-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca320-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca320-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="ca320-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca320-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="ca320-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca320-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="ca320-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ca320-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="ca320-117">Class of the RR.</span></span> <span data-ttu-id="ca320-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ca320-118">Default value is 1.</span></span> <span data-ttu-id="ca320-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="ca320-119">The following values are valid.</span></span>



| <span data-ttu-id="ca320-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ca320-120">Value</span></span>                                                                                                | <span data-ttu-id="ca320-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ca320-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ca320-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ca320-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ca320-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="ca320-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ca320-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ca320-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ca320-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ca320-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ca320-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="ca320-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ca320-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="ca320-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ca320-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ca320-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ca320-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ca320-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ca320-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ca320-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="ca320-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-132">*NextDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca320-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-133">Próximo nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="ca320-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-134">*Tipos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca320-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-135">Lista separada por espaços dos mnemônicos do tipo RR para o nome do proprietário do registro de recurso NXT.</span><span class="sxs-lookup"><span data-stu-id="ca320-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="ca320-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ca320-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ca320-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ca320-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca320-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca320-138">Return value</span></span>

<span data-ttu-id="ca320-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ca320-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca320-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca320-140">Requirements</span></span>



| <span data-ttu-id="ca320-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca320-141">Requirement</span></span> | <span data-ttu-id="ca320-142">Valor</span><span class="sxs-lookup"><span data-stu-id="ca320-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca320-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca320-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ca320-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ca320-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ca320-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca320-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ca320-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca320-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ca320-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca320-147">Namespace</span></span><br/>                | <span data-ttu-id="ca320-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ca320-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ca320-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ca320-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca320-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca320-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca320-151">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ca320-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca320-152">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="ca320-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="ca320-153">**Método Modify da classe MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="ca320-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="ca320-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ca320-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





