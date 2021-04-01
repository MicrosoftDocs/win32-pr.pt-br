---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Cada instância da \_ classe WMI de associação de servidor MicrosoftDNS pode conter várias instâncias da \_ classe de domínio MicrosoftDNS.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment de classe de DNS
- MicrosoftDNS_ServerDomainContainment de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644341"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="80740-105">\_Classe MicrosoftDNS ServerDomainContainment</span><span class="sxs-lookup"><span data-stu-id="80740-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="80740-106">Cada instância da classe WMI de associação de [**\_ servidor MicrosoftDNS**](microsoftdns-server.md) pode conter várias instâncias da classe de [**\_ domínio MicrosoftDNS**](microsoftdns-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="80740-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="80740-107">Cada instância da classe **de \_ domínio MicrosoftDNS** pertence a uma única instância da classe **de \_ servidor MicrosoftDNS** e é definida para ser fraca para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="80740-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="80740-108">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="80740-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80740-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80740-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="80740-110">Membros</span><span class="sxs-lookup"><span data-stu-id="80740-110">Members</span></span>

<span data-ttu-id="80740-111">A classe **MicrosoftDNS \_ ServerDomainContainment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80740-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="80740-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80740-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80740-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80740-113">Properties</span></span>

<span data-ttu-id="80740-114">A classe **MicrosoftDNS \_ ServerDomainContainment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80740-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80740-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="80740-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80740-116">Tipo de dados **: \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="80740-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="80740-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80740-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80740-118">Qualificadores: Key, Override ("GroupComponent"), min (1), Max (1)</span><span class="sxs-lookup"><span data-stu-id="80740-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="80740-119">Descrição: o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="80740-119">Description: The DNS Server.</span></span>

<span data-ttu-id="80740-120">Herdado **do \_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="80740-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="80740-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="80740-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80740-122">Tipo de dados **: \_ domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="80740-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="80740-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80740-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80740-124">Qualificadores: chave, substituição ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="80740-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="80740-125">Descrição: um domínio, zona, cache ou RootHints gerenciado pelo servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="80740-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="80740-126">Herdado **do \_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="80740-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80740-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="80740-127">Remarks</span></span>

<span data-ttu-id="80740-128">A classe **MicrosoftDNS \_ ServerDomainContainment** é derivada da classe **de \_ componente CIM** .</span><span class="sxs-lookup"><span data-stu-id="80740-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="80740-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80740-129">Requirements</span></span>



| <span data-ttu-id="80740-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="80740-130">Requirement</span></span> | <span data-ttu-id="80740-131">Valor</span><span class="sxs-lookup"><span data-stu-id="80740-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80740-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80740-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80740-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="80740-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="80740-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80740-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80740-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="80740-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80740-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="80740-136">Namespace</span></span><br/>                | <span data-ttu-id="80740-137">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="80740-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="80740-138">MOF</span><span class="sxs-lookup"><span data-stu-id="80740-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80740-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80740-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80740-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="80740-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80740-141">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="80740-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="80740-142">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="80740-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="80740-143">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="80740-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





