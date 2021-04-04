---
title: Classe MicrosoftDNS_SOAType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de início de autoridade (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType de classe de DNS
- MicrosoftDNS_SOAType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008986"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="a65cb-105">\_Classe MicrosoftDNS SOAType</span><span class="sxs-lookup"><span data-stu-id="a65cb-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="a65cb-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de início de autoridade (SOA).</span><span class="sxs-lookup"><span data-stu-id="a65cb-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="a65cb-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="a65cb-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65cb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65cb-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="a65cb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a65cb-109">Members</span></span>

<span data-ttu-id="a65cb-110">A classe **MicrosoftDNS \_ SOAType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a65cb-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="a65cb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a65cb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a65cb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a65cb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a65cb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a65cb-113">Methods</span></span>

<span data-ttu-id="a65cb-114">A classe **MicrosoftDNS \_ SOAType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a65cb-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="a65cb-115">Método</span><span class="sxs-lookup"><span data-stu-id="a65cb-115">Method</span></span>     | <span data-ttu-id="a65cb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65cb-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65cb-117">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="a65cb-117">**Modify**</span></span> | <span data-ttu-id="a65cb-118">Atualiza o TTL, o número de série da SOA, o servidor primário, a parte responsável, o intervalo de atualização, o atraso de repetição, o limite de expiração e o TTL mínimo (para a zona) para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="a65cb-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a65cb-119">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="a65cb-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a65cb-120">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="a65cb-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a65cb-121">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="a65cb-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a65cb-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a65cb-122">Properties</span></span>

<span data-ttu-id="a65cb-123">A classe **MicrosoftDNS \_ SOAType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a65cb-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a65cb-124">**ExpireLimit**</span><span class="sxs-lookup"><span data-stu-id="a65cb-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a65cb-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-127">Tempo, em segundos, antes que uma zona sem resposta não seja mais autoritativa.</span><span class="sxs-lookup"><span data-stu-id="a65cb-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-128">**MinimumTTL**</span><span class="sxs-lookup"><span data-stu-id="a65cb-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a65cb-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-131">Limite inferior no tempo, em segundos, que um servidor DNS ou um resolvedor de cache tem permissão para armazenar em cache qualquer registro de recurso da zona à qual esse registro pertence.</span><span class="sxs-lookup"><span data-stu-id="a65cb-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-132">**PrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="a65cb-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a65cb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-135">Servidor DNS autoritativo para a zona à qual o registro pertence.</span><span class="sxs-lookup"><span data-stu-id="a65cb-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-136">**Intervalo de atualização**</span><span class="sxs-lookup"><span data-stu-id="a65cb-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a65cb-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-139">Tempo, em segundos, antes que a zona que contém esse registro deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="a65cb-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-140">**ResponsibleParty**</span><span class="sxs-lookup"><span data-stu-id="a65cb-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a65cb-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-143">Nome da parte responsável da zona à qual o registro pertence.</span><span class="sxs-lookup"><span data-stu-id="a65cb-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="a65cb-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a65cb-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-147">Tempo, em segundos, antes de tentar novamente uma atualização com falha da zona à qual esse registro pertence.</span><span class="sxs-lookup"><span data-stu-id="a65cb-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a65cb-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a65cb-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65cb-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a65cb-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a65cb-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a65cb-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a65cb-151">Número de série do registro SOA.</span><span class="sxs-lookup"><span data-stu-id="a65cb-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a65cb-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65cb-152">Requirements</span></span>



| <span data-ttu-id="a65cb-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65cb-153">Requirement</span></span> | <span data-ttu-id="a65cb-154">Valor</span><span class="sxs-lookup"><span data-stu-id="a65cb-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65cb-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a65cb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a65cb-156">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a65cb-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a65cb-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a65cb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a65cb-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a65cb-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a65cb-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="a65cb-159">Namespace</span></span><br/>                | <span data-ttu-id="a65cb-160">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="a65cb-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a65cb-161">MOF</span><span class="sxs-lookup"><span data-stu-id="a65cb-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a65cb-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a65cb-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65cb-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="a65cb-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65cb-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a65cb-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="a65cb-165">**Método Modify da classe MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="a65cb-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





