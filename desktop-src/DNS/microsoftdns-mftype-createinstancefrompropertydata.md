---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MFType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso do agente de encaminhamento de mensagens para o domínio (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MFType
- MicrosoftDNS_MFType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918425"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="8be1b-106">Método CreateInstanceFromPropertyData da \_ classe MFType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8be1b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="8be1b-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso do agente de encaminhamento de mensagens para o domínio (MF).</span><span class="sxs-lookup"><span data-stu-id="8be1b-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be1b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8be1b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8be1b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8be1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be1b-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="8be1b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8be1b-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="8be1b-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8be1b-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="8be1b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8be1b-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="8be1b-117">Class of the RR.</span></span> <span data-ttu-id="8be1b-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="8be1b-118">Default value is 1.</span></span> <span data-ttu-id="8be1b-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="8be1b-119">The following values are valid.</span></span>



| <span data-ttu-id="8be1b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8be1b-120">Value</span></span>                                                                                                | <span data-ttu-id="8be1b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8be1b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8be1b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8be1b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8be1b-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="8be1b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8be1b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8be1b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8be1b-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8be1b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8be1b-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8be1b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8be1b-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="8be1b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8be1b-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="8be1b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8be1b-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="8be1b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8be1b-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="8be1b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8be1b-132">*MFHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-133">Nome do host que fornece o agente de encaminhamento de email.</span><span class="sxs-lookup"><span data-stu-id="8be1b-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="8be1b-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8be1b-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="8be1b-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be1b-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8be1b-136">Return value</span></span>

<span data-ttu-id="8be1b-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8be1b-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be1b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be1b-138">Requirements</span></span>



| <span data-ttu-id="8be1b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be1b-139">Requirement</span></span> | <span data-ttu-id="8be1b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8be1b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8be1b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be1b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8be1b-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8be1b-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8be1b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be1b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8be1b-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8be1b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8be1b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="8be1b-145">Namespace</span></span><br/>                | <span data-ttu-id="8be1b-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="8be1b-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8be1b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8be1b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8be1b-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8be1b-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be1b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8be1b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be1b-150">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="8be1b-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="8be1b-151">**Método Modify da classe MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="8be1b-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="8be1b-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8be1b-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





