---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_SRVType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de serviço (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645120"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="1ee65-106">Método CreateInstanceFromPropertyData da \_ classe SRVType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="1ee65-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="1ee65-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="1ee65-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee65-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ee65-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="1ee65-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ee65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee65-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="1ee65-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="1ee65-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="1ee65-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="1ee65-117">Class of the RR.</span></span> <span data-ttu-id="1ee65-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="1ee65-118">Default value is 1.</span></span> <span data-ttu-id="1ee65-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="1ee65-119">The following values are valid.</span></span>



| <span data-ttu-id="1ee65-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee65-120">Value</span></span>                                                                                                | <span data-ttu-id="1ee65-121">Significado</span><span class="sxs-lookup"><span data-stu-id="1ee65-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1ee65-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee65-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1ee65-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="1ee65-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="1ee65-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee65-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1ee65-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="1ee65-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="1ee65-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee65-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1ee65-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="1ee65-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="1ee65-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee65-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1ee65-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="1ee65-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="1ee65-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="1ee65-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-132">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-133">Prioridade do host de destino especificado no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="1ee65-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="1ee65-134">Números inferiores implicam prioridades mais altas.</span><span class="sxs-lookup"><span data-stu-id="1ee65-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-135">*Peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-136">Peso do host de destino.</span><span class="sxs-lookup"><span data-stu-id="1ee65-136">Weight of the target host.</span></span> <span data-ttu-id="1ee65-137">Isso é útil ao selecionar entre os hosts que têm a mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="1ee65-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="1ee65-138">As chances de usar esse host devem ser proporcionais ao seu peso.</span><span class="sxs-lookup"><span data-stu-id="1ee65-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-139">*Porta* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-140">Porta usada no host de destino de um serviço de protocolo.</span><span class="sxs-lookup"><span data-stu-id="1ee65-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-141">*SRVDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-142">FQDN do host de destino.</span><span class="sxs-lookup"><span data-stu-id="1ee65-142">FQDN of the target host.</span></span> <span data-ttu-id="1ee65-143">Um destino de \\ . \\ significa que o serviço está decididamente não disponível neste domínio.</span><span class="sxs-lookup"><span data-stu-id="1ee65-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="1ee65-144">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee65-145">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="1ee65-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee65-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ee65-146">Return value</span></span>

<span data-ttu-id="1ee65-147">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1ee65-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee65-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee65-148">Requirements</span></span>



| <span data-ttu-id="1ee65-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee65-149">Requirement</span></span> | <span data-ttu-id="1ee65-150">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee65-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee65-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee65-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee65-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1ee65-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1ee65-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee65-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee65-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee65-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1ee65-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ee65-155">Namespace</span></span><br/>                | <span data-ttu-id="1ee65-156">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="1ee65-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1ee65-157">MOF</span><span class="sxs-lookup"><span data-stu-id="1ee65-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ee65-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ee65-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee65-159">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ee65-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee65-160">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="1ee65-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="1ee65-161">**Método Modify da classe MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="1ee65-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="1ee65-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1ee65-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





