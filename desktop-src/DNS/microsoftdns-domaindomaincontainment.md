---
title: Classe MicrosoftDNS_DomainDomainContainment
description: A \_ classe MicrosoftDNS DomainDomainContainment é usada para contenção de domínio; Os domínios DNS podem conter outros domínios DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment de classe de DNS
- MicrosoftDNS_DomainDomainContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009613"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="07b21-105">\_Classe MicrosoftDNS DomainDomainContainment</span><span class="sxs-lookup"><span data-stu-id="07b21-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="07b21-106">A classe **MicrosoftDNS \_ DomainDomainContainment** é usada para contenção de domínio; Os domínios DNS podem conter outros domínios DNS.</span><span class="sxs-lookup"><span data-stu-id="07b21-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="07b21-107">Cada instância da classe [**de \_ domínio MicrosoftDNS**](microsoftdns-domain.md) pode conter várias outras instâncias do **\_ domínio MicrosoftDNS**.</span><span class="sxs-lookup"><span data-stu-id="07b21-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="07b21-108">Uma instância de um objeto de **\_ domínio MicrosoftDNS** está diretamente contida em no máximo um **\_ domínio MicrosoftDNS** de nível superior.</span><span class="sxs-lookup"><span data-stu-id="07b21-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="07b21-109">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="07b21-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b21-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07b21-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="07b21-111">Membros</span><span class="sxs-lookup"><span data-stu-id="07b21-111">Members</span></span>

<span data-ttu-id="07b21-112">A classe **MicrosoftDNS \_ DomainDomainContainment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="07b21-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="07b21-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07b21-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07b21-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07b21-114">Properties</span></span>

<span data-ttu-id="07b21-115">A classe **MicrosoftDNS \_ DomainDomainContainment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="07b21-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07b21-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="07b21-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b21-117">Tipo de dados **: \_ domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="07b21-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="07b21-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07b21-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b21-119">Qualificadores: Key, Max (1), Override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="07b21-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="07b21-120">Descrição: um domínio, zona, cache ou RootHints de nível superior.</span><span class="sxs-lookup"><span data-stu-id="07b21-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="07b21-121">Herdado do \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="07b21-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="07b21-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="07b21-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b21-123">Tipo de dados **: \_ domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="07b21-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="07b21-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07b21-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b21-125">Qualificadores: chave, substituição ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="07b21-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="07b21-126">Descrição: o domínio contido por um domínio de nível superior, zona, cache ou RootHints.</span><span class="sxs-lookup"><span data-stu-id="07b21-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="07b21-127">Herdado do \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="07b21-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07b21-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b21-128">Requirements</span></span>



| <span data-ttu-id="07b21-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b21-129">Requirement</span></span> | <span data-ttu-id="07b21-130">Valor</span><span class="sxs-lookup"><span data-stu-id="07b21-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b21-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b21-131">Minimum supported client</span></span><br/> | <span data-ttu-id="07b21-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07b21-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07b21-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b21-133">Minimum supported server</span></span><br/> | <span data-ttu-id="07b21-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07b21-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="07b21-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="07b21-135">Namespace</span></span><br/>                | <span data-ttu-id="07b21-136">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="07b21-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="07b21-137">MOF</span><span class="sxs-lookup"><span data-stu-id="07b21-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07b21-138"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07b21-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b21-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="07b21-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b21-140">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="07b21-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="07b21-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="07b21-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="07b21-142">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="07b21-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





