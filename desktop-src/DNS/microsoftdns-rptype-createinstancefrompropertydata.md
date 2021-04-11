---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_RPType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de pessoa responsável (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_RPType
- MicrosoftDNS_RPType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163596"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="09a5a-106">Método CreateInstanceFromPropertyData da \_ classe RPType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="09a5a-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="09a5a-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de pessoa responsável (RP).</span><span class="sxs-lookup"><span data-stu-id="09a5a-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a5a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09a5a-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="09a5a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09a5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a5a-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="09a5a-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="09a5a-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="09a5a-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="09a5a-117">Class of the RR.</span></span> <span data-ttu-id="09a5a-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="09a5a-118">Default value is 1.</span></span> <span data-ttu-id="09a5a-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="09a5a-119">The following values are valid.</span></span>



| <span data-ttu-id="09a5a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="09a5a-120">Value</span></span>                                                                                                | <span data-ttu-id="09a5a-121">Significado</span><span class="sxs-lookup"><span data-stu-id="09a5a-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="09a5a-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="09a5a-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="09a5a-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="09a5a-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="09a5a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="09a5a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="09a5a-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="09a5a-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="09a5a-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="09a5a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="09a5a-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="09a5a-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="09a5a-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="09a5a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="09a5a-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="09a5a-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="09a5a-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="09a5a-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-132">*RPMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-133">FQDN que especifica a caixa de correio da pessoa responsável.</span><span class="sxs-lookup"><span data-stu-id="09a5a-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-134">*TXTDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-135">FQDN para o qual os registros de recurso TXT existem.</span><span class="sxs-lookup"><span data-stu-id="09a5a-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="09a5a-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="09a5a-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="09a5a-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a5a-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09a5a-138">Return value</span></span>

<span data-ttu-id="09a5a-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="09a5a-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a5a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09a5a-140">Requirements</span></span>



| <span data-ttu-id="09a5a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a5a-141">Requirement</span></span> | <span data-ttu-id="09a5a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="09a5a-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09a5a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09a5a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="09a5a-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="09a5a-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="09a5a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09a5a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="09a5a-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09a5a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="09a5a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="09a5a-147">Namespace</span></span><br/>                | <span data-ttu-id="09a5a-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="09a5a-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="09a5a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="09a5a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09a5a-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09a5a-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a5a-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="09a5a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a5a-152">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="09a5a-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="09a5a-153">**Método Modify da classe MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="09a5a-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="09a5a-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="09a5a-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





