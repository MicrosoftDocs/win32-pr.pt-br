---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MGType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de grupo de emails (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MGType
- MicrosoftDNS_MGType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085907"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="ee9ec-106">Método CreateInstanceFromPropertyData da \_ classe MGType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ee9ec-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="ee9ec-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de grupo de emails (mg).</span><span class="sxs-lookup"><span data-stu-id="ee9ec-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9ec-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee9ec-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ee9ec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee9ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee9ec-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ec-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ec-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ec-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-117">Class of the RR.</span></span> <span data-ttu-id="ee9ec-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-118">Default value is 1.</span></span> <span data-ttu-id="ee9ec-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-119">The following values are valid.</span></span>



| <span data-ttu-id="ee9ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ee9ec-120">Value</span></span>                                                                                                | <span data-ttu-id="ee9ec-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ee9ec-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ee9ec-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ec-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ee9ec-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="ee9ec-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ee9ec-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ec-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ee9ec-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ee9ec-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ee9ec-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ec-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ee9ec-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="ee9ec-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ee9ec-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ec-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ee9ec-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ee9ec-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ee9ec-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ec-132">*MGMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-133">FQDN que especifica uma caixa de correio que é membro do grupo de emails especificado pelo nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="ee9ec-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9ec-135">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee9ec-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee9ec-136">Return value</span></span>

<span data-ttu-id="ee9ec-137">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ee9ec-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee9ec-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee9ec-138">Requirements</span></span>



| <span data-ttu-id="ee9ec-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee9ec-139">Requirement</span></span> | <span data-ttu-id="ee9ec-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ee9ec-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9ec-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee9ec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9ec-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ee9ec-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ee9ec-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee9ec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9ec-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee9ec-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ee9ec-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee9ec-145">Namespace</span></span><br/>                | <span data-ttu-id="ee9ec-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ee9ec-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ee9ec-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ee9ec-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee9ec-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee9ec-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee9ec-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee9ec-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9ec-150">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="ee9ec-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="ee9ec-151">**Método Modify da classe MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="ee9ec-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ee9ec-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ee9ec-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





