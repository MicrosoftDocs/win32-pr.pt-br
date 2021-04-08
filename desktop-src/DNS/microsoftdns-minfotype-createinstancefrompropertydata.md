---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MINFOType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de informações de email (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008896"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="14d62-106">Método CreateInstanceFromPropertyData da \_ classe MINFOType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="14d62-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="14d62-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de informações de email (MINFO).</span><span class="sxs-lookup"><span data-stu-id="14d62-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d62-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14d62-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="14d62-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14d62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d62-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14d62-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="14d62-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14d62-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="14d62-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14d62-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="14d62-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="14d62-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="14d62-117">Class of the RR.</span></span> <span data-ttu-id="14d62-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="14d62-118">Default value is 1.</span></span> <span data-ttu-id="14d62-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="14d62-119">The following values are valid.</span></span>



| <span data-ttu-id="14d62-120">Valor</span><span class="sxs-lookup"><span data-stu-id="14d62-120">Value</span></span>                                                                                                | <span data-ttu-id="14d62-121">Significado</span><span class="sxs-lookup"><span data-stu-id="14d62-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="14d62-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="14d62-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="14d62-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="14d62-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="14d62-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="14d62-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="14d62-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="14d62-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="14d62-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="14d62-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="14d62-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="14d62-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="14d62-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="14d62-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="14d62-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-132">*ResponsibleMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14d62-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-133">FQDN que especifica uma caixa de correio responsável pela lista de endereçamento ou caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="14d62-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-134">*ErrorMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14d62-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-135">FQDN que especifica uma caixa de correio para receber mensagens de erro relacionadas à lista de endereçamento ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="14d62-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="14d62-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="14d62-137">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="14d62-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d62-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14d62-138">Return value</span></span>

<span data-ttu-id="14d62-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="14d62-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d62-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d62-140">Requirements</span></span>



| <span data-ttu-id="14d62-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d62-141">Requirement</span></span> | <span data-ttu-id="14d62-142">Valor</span><span class="sxs-lookup"><span data-stu-id="14d62-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d62-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14d62-143">Minimum supported client</span></span><br/> | <span data-ttu-id="14d62-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="14d62-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="14d62-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14d62-145">Minimum supported server</span></span><br/> | <span data-ttu-id="14d62-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14d62-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14d62-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="14d62-147">Namespace</span></span><br/>                | <span data-ttu-id="14d62-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="14d62-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="14d62-149">MOF</span><span class="sxs-lookup"><span data-stu-id="14d62-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14d62-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d62-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="14d62-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d62-152">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="14d62-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="14d62-153">**Método Modify da classe MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="14d62-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="14d62-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="14d62-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





