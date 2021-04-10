---
title: Método Modify da classe MicrosoftDNS_SOAType
description: O método Modify atualiza um registro de recurso de início de autoridade (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008987"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="1f69d-106">Método Modify da classe MicrosoftDNS \_ SOAType</span><span class="sxs-lookup"><span data-stu-id="1f69d-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="1f69d-107">O método **Modify** atualiza um registro de recurso de início de autoridade (SOA).</span><span class="sxs-lookup"><span data-stu-id="1f69d-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f69d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f69d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="1f69d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f69d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f69d-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="1f69d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-112">*SerialNumber* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-113">O número de série SOA que representa o número de vezes que a zona foi atualizada, usada pelos [*servidores secundários*](s-gly.md) para determinar se a transferência de zona é necessária.</span><span class="sxs-lookup"><span data-stu-id="1f69d-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-114">*PrimaryServer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-115">Nome do servidor primário.</span><span class="sxs-lookup"><span data-stu-id="1f69d-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-116">*ResponsibleParty* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-117">Endereço da caixa de correio da parte responsável, na forma de alias. Domain, como xyz.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1f69d-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="1f69d-118">Observe o uso de um período em vez de um símbolo de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="1f69d-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-119">*RefreshInterval* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-120">Tempo, em segundos, antes que a zona que contém esse registro deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f69d-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-121">*RetryDelay* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-122">Tempo, em segundos, o servidor DNS deve atrasar entre as tentativas de resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="1f69d-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-123">*ExpireLimit* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-124">Tempo, em segundos, que os servidores secundários devem aguardar por uma resposta do servidor primário antes de descartar suas cópias do arquivo de zona como inválidas.</span><span class="sxs-lookup"><span data-stu-id="1f69d-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-125">*MinimumTTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-126">Tempo de vida útil, em segundos, aplicado aos registros de recursos na zona que não especificam seu próprio TTL.</span><span class="sxs-lookup"><span data-stu-id="1f69d-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="1f69d-127">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1f69d-128">Referência ao objeto modificado</span><span class="sxs-lookup"><span data-stu-id="1f69d-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f69d-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f69d-129">Return value</span></span>

<span data-ttu-id="1f69d-130">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1f69d-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f69d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f69d-131">Remarks</span></span>

<span data-ttu-id="1f69d-132">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="1f69d-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f69d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f69d-133">Requirements</span></span>



| <span data-ttu-id="1f69d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f69d-134">Requirement</span></span> | <span data-ttu-id="1f69d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1f69d-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f69d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f69d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f69d-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1f69d-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1f69d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f69d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f69d-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f69d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1f69d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f69d-140">Namespace</span></span><br/>                | <span data-ttu-id="1f69d-141">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="1f69d-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1f69d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1f69d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f69d-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f69d-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f69d-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f69d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f69d-145">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="1f69d-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="1f69d-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1f69d-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





