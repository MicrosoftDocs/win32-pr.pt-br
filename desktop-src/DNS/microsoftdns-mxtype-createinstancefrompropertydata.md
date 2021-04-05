---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MXType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de troca de mensagens (MR).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MXType
- MicrosoftDNS_MXType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085613"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="66a2f-106">Método CreateInstanceFromPropertyData da \_ classe MXType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="66a2f-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="66a2f-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de troca de mensagens (Mr).</span><span class="sxs-lookup"><span data-stu-id="66a2f-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a2f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66a2f-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="66a2f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66a2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a2f-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="66a2f-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="66a2f-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="66a2f-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="66a2f-117">Class of the RR.</span></span> <span data-ttu-id="66a2f-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="66a2f-118">Default value is 1.</span></span> <span data-ttu-id="66a2f-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="66a2f-119">The following values are valid.</span></span>



| <span data-ttu-id="66a2f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66a2f-120">Value</span></span>                                                                                                | <span data-ttu-id="66a2f-121">Significado</span><span class="sxs-lookup"><span data-stu-id="66a2f-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="66a2f-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="66a2f-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="66a2f-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="66a2f-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="66a2f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="66a2f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="66a2f-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="66a2f-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="66a2f-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="66a2f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="66a2f-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="66a2f-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="66a2f-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="66a2f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="66a2f-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="66a2f-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="66a2f-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="66a2f-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-132">*Preferência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-133">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="66a2f-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="66a2f-134">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="66a2f-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-135">*MailExchange* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-136">FQDN que especifica um host que está disposto a atuar como uma troca de email para o nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="66a2f-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="66a2f-137">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2f-138">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="66a2f-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a2f-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66a2f-139">Return value</span></span>

<span data-ttu-id="66a2f-140">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="66a2f-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a2f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a2f-141">Requirements</span></span>



| <span data-ttu-id="66a2f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a2f-142">Requirement</span></span> | <span data-ttu-id="66a2f-143">Valor</span><span class="sxs-lookup"><span data-stu-id="66a2f-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a2f-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a2f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="66a2f-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="66a2f-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="66a2f-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a2f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="66a2f-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66a2f-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66a2f-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="66a2f-148">Namespace</span></span><br/>                | <span data-ttu-id="66a2f-149">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="66a2f-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="66a2f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="66a2f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66a2f-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66a2f-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a2f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a2f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a2f-153">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="66a2f-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="66a2f-154">**Método Modify da classe MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="66a2f-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="66a2f-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="66a2f-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





