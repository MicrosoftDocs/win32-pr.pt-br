---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MBType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de caixa de correio (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MBType
- MicrosoftDNS_MBType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824508"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="8d2f2-106">Método CreateInstanceFromPropertyData da \_ classe MBType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8d2f2-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="8d2f2-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de caixa de correio (MB).</span><span class="sxs-lookup"><span data-stu-id="8d2f2-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2f2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d2f2-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8d2f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d2f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d2f2-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8d2f2-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8d2f2-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8d2f2-116">*RecordClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-117">Optional.</span></span> <span data-ttu-id="8d2f2-118">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-118">Class of the RR.</span></span> <span data-ttu-id="8d2f2-119">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-119">Default value is 1.</span></span> <span data-ttu-id="8d2f2-120">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-120">The following values are valid.</span></span>



| <span data-ttu-id="8d2f2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8d2f2-121">Value</span></span>                                                                                                | <span data-ttu-id="8d2f2-122">Significado</span><span class="sxs-lookup"><span data-stu-id="8d2f2-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8d2f2-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8d2f2-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8d2f2-124">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="8d2f2-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8d2f2-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8d2f2-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8d2f2-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8d2f2-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8d2f2-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8d2f2-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8d2f2-128">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="8d2f2-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8d2f2-129"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="8d2f2-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8d2f2-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="8d2f2-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8d2f2-131">*TTL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-132">Optional.</span></span> <span data-ttu-id="8d2f2-133">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8d2f2-134">*MBHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-135">Nome do host da caixa de correio para o RR.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8d2f2-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2f2-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d2f2-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d2f2-138">Return value</span></span>

<span data-ttu-id="8d2f2-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8d2f2-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d2f2-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d2f2-140">Requirements</span></span>



| <span data-ttu-id="8d2f2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d2f2-141">Requirement</span></span> | <span data-ttu-id="8d2f2-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8d2f2-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d2f2-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d2f2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8d2f2-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8d2f2-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8d2f2-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d2f2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8d2f2-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d2f2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d2f2-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d2f2-147">Namespace</span></span><br/>                | <span data-ttu-id="8d2f2-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="8d2f2-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8d2f2-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8d2f2-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d2f2-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d2f2-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d2f2-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d2f2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2f2-152">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="8d2f2-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="8d2f2-153">**Método Modify da classe MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="8d2f2-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="8d2f2-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8d2f2-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





