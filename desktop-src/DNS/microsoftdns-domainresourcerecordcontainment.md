---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: A \_ classe MicrosoftDNS DomainResourceRecordContainment é usada para confinamento de RR; cada instância do \_ domínio MicrosoftDNS pode conter várias instâncias da \_ classe MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment de classe de DNS
- MicrosoftDNS_DomainResourceRecordContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455159"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="52f7d-105">\_Classe MicrosoftDNS DomainResourceRecordContainment</span><span class="sxs-lookup"><span data-stu-id="52f7d-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="52f7d-106">A classe **MicrosoftDNS \_ DomainResourceRecordContainment** é usada para confinamento de RR; cada instância [**do \_ domínio MicrosoftDNS**](microsoftdns-domain.md) pode conter várias instâncias da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="52f7d-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="52f7d-107">Cada instância da classe **MicrosoftDNS \_ ResourceRecord** pertence a uma única instância da classe de **\_ domínio MicrosoftDNS** e é definida para ser fraca para essa instância.</span><span class="sxs-lookup"><span data-stu-id="52f7d-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="52f7d-108">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="52f7d-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f7d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52f7d-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="52f7d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="52f7d-110">Members</span></span>

<span data-ttu-id="52f7d-111">A classe **MicrosoftDNS \_ DomainResourceRecordContainment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="52f7d-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="52f7d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52f7d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52f7d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52f7d-113">Properties</span></span>

<span data-ttu-id="52f7d-114">A classe **MicrosoftDNS \_ DomainResourceRecordContainment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="52f7d-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52f7d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="52f7d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f7d-116">Tipo de dados **: \_ domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="52f7d-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="52f7d-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52f7d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52f7d-118">Qualificadores: chave, substituição ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="52f7d-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="52f7d-119">Descrição: a zona, o cache, o RootHints ou o domínio que contém diretamente o registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="52f7d-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="52f7d-120">Herdado do \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="52f7d-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="52f7d-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="52f7d-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f7d-122">Tipo de dados: **MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="52f7d-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="52f7d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52f7d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52f7d-124">Qualificadores: chave, substituição ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="52f7d-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="52f7d-125">Descrição: o registro de recurso contido em um domínio, zona, cache ou RootHints.</span><span class="sxs-lookup"><span data-stu-id="52f7d-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="52f7d-126">Herdado do \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="52f7d-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52f7d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f7d-127">Requirements</span></span>



| <span data-ttu-id="52f7d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f7d-128">Requirement</span></span> | <span data-ttu-id="52f7d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="52f7d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52f7d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f7d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="52f7d-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="52f7d-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="52f7d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f7d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="52f7d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52f7d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="52f7d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="52f7d-134">Namespace</span></span><br/>                | <span data-ttu-id="52f7d-135">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="52f7d-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="52f7d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="52f7d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52f7d-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52f7d-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f7d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f7d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f7d-139">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="52f7d-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="52f7d-140">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="52f7d-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="52f7d-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="52f7d-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





