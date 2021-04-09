---
title: Classe MicrosoftDNS_Domain
description: A \_ classe de domínio MicrosoftDNS representa um domínio em uma hierarquia de DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain de classe de DNS
- MicrosoftDNS_Domain de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085565"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="384ce-105">\_Classe de domínio MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="384ce-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="384ce-106">A classe de **\_ domínio MicrosoftDNS** representa um domínio em uma hierarquia de DNS.</span><span class="sxs-lookup"><span data-stu-id="384ce-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="384ce-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="384ce-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="384ce-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="384ce-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="384ce-109">Membros</span><span class="sxs-lookup"><span data-stu-id="384ce-109">Members</span></span>

<span data-ttu-id="384ce-110">A classe de **\_ domínio MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="384ce-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="384ce-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="384ce-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="384ce-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="384ce-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="384ce-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="384ce-113">Methods</span></span>

<span data-ttu-id="384ce-114">A classe de **\_ domínio MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="384ce-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="384ce-115">Método</span><span class="sxs-lookup"><span data-stu-id="384ce-115">Method</span></span>                   | <span data-ttu-id="384ce-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="384ce-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="384ce-117">**Getdistinguiname**</span><span class="sxs-lookup"><span data-stu-id="384ce-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="384ce-118">Obtém o nome distinto do DS para a zona.</span><span class="sxs-lookup"><span data-stu-id="384ce-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="384ce-119">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="384ce-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="384ce-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="384ce-120">Properties</span></span>

<span data-ttu-id="384ce-121">A classe de **\_ domínio MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="384ce-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="384ce-122">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="384ce-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="384ce-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="384ce-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="384ce-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="384ce-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="384ce-125">Nome do contêiner do domínio, que pode ser uma zona, um cache ou um RootHints.</span><span class="sxs-lookup"><span data-stu-id="384ce-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="384ce-126">Nos casos em que o contêiner é uma zona (uma instância da classe de [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), essa propriedade contém o FQDN da zona.</span><span class="sxs-lookup"><span data-stu-id="384ce-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="384ce-127">Quando o contêiner é a zona raiz, a cadeia de caracteres \\ \\ deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="384ce-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="384ce-128">Nos casos em que o contêiner é o cache DNS dos registros de recursos (uma instância da classe de [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), essa propriedade é definida como a cadeia de caracteres \\ . Cache \\ .</span><span class="sxs-lookup"><span data-stu-id="384ce-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="384ce-129">Se o contêiner for RootHints (uma instância da classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), essa propriedade deverá ser definida como \\ .. RootHints \\ .</span><span class="sxs-lookup"><span data-stu-id="384ce-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="384ce-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="384ce-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="384ce-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="384ce-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="384ce-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="384ce-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="384ce-133">FQDN ou endereço IP do servidor DNS que contém o domínio.</span><span class="sxs-lookup"><span data-stu-id="384ce-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="384ce-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="384ce-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="384ce-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="384ce-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="384ce-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="384ce-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="384ce-137">FQDN do domínio.</span><span class="sxs-lookup"><span data-stu-id="384ce-137">FQDN of the domain.</span></span>

<span data-ttu-id="384ce-138">Para instâncias do cache DNS ou RootHints, as cadeias de caracteres \\ .. Cache \\ e \\ .. RootHints \\ deve ser usado, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="384ce-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="384ce-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="384ce-139">Requirements</span></span>



| <span data-ttu-id="384ce-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="384ce-140">Requirement</span></span> | <span data-ttu-id="384ce-141">Valor</span><span class="sxs-lookup"><span data-stu-id="384ce-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="384ce-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="384ce-142">Minimum supported client</span></span><br/> | <span data-ttu-id="384ce-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="384ce-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="384ce-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="384ce-144">Minimum supported server</span></span><br/> | <span data-ttu-id="384ce-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="384ce-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="384ce-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="384ce-146">Namespace</span></span><br/>                | <span data-ttu-id="384ce-147">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="384ce-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="384ce-148">MOF</span><span class="sxs-lookup"><span data-stu-id="384ce-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="384ce-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="384ce-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="384ce-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="384ce-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="384ce-151">**Método getdistinguiname da classe de \_ domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="384ce-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





