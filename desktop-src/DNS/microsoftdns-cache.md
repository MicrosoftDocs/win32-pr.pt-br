---
title: Classe MicrosoftDNS_Cache
description: A \_ classe de cache MicrosoftDNS descreve um cache existente em um servidor DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache de classe de DNS
- MicrosoftDNS_Cache de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009378"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="5866b-105">\_Classe de cache MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5866b-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="5866b-106">A classe de **\_ cache MicrosoftDNS** descreve um cache existente em um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="5866b-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="5866b-107">Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.</span><span class="sxs-lookup"><span data-stu-id="5866b-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="5866b-108">A classe de **\_ cache MicrosoftDNS** é um contêiner para os registros de recursos armazenados em cache pelo servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="5866b-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="5866b-109">Não confunda isso com um arquivo de cache que contém dicas de raiz.</span><span class="sxs-lookup"><span data-stu-id="5866b-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="5866b-110">Cada instância do **\_ cache MicrosoftDNS** de classe deve ser atribuída a exatamente um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="5866b-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="5866b-111">Ele pode ser associado a várias instâncias do [**\_ domínio MicrosoftDNS**](microsoftdns-domain.md) ou [**classes \_ MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="5866b-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="5866b-112">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5866b-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5866b-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5866b-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="5866b-114">Membros</span><span class="sxs-lookup"><span data-stu-id="5866b-114">Members</span></span>

<span data-ttu-id="5866b-115">A classe de **\_ cache MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5866b-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="5866b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5866b-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5866b-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="5866b-117">Methods</span></span>

<span data-ttu-id="5866b-118">A classe de **\_ cache MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5866b-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="5866b-119">Método</span><span class="sxs-lookup"><span data-stu-id="5866b-119">Method</span></span>                   | <span data-ttu-id="5866b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5866b-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5866b-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="5866b-121">**ClearCache**</span></span>           | <span data-ttu-id="5866b-122">Limpa o cache do servidor DNS dos registros de recursos.</span><span class="sxs-lookup"><span data-stu-id="5866b-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="5866b-123">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="5866b-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="5866b-124">**Getdistinguiname**</span><span class="sxs-lookup"><span data-stu-id="5866b-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="5866b-125">Recupera o nome distinto da zona.</span><span class="sxs-lookup"><span data-stu-id="5866b-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="5866b-126">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="5866b-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="5866b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5866b-127">Requirements</span></span>



| <span data-ttu-id="5866b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5866b-128">Requirement</span></span> | <span data-ttu-id="5866b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5866b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5866b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5866b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5866b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5866b-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5866b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5866b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5866b-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5866b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5866b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5866b-134">Namespace</span></span><br/>                | <span data-ttu-id="5866b-135">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="5866b-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5866b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5866b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5866b-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5866b-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5866b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5866b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5866b-139">**\_Domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5866b-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="5866b-140">**Método ClearCache da classe de \_ cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5866b-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="5866b-141">**Método getdistinguiname da classe de \_ cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5866b-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





