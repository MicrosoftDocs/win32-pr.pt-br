---
title: Classe MicrosoftDNS_RootHints
description: A \_ classe MicrosoftDNS RootHints descreve o RootHints armazenado em um arquivo de cache em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints de classe de DNS
- MicrosoftDNS_RootHints de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085715"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="0e403-106">\_Classe MicrosoftDNS RootHints</span><span class="sxs-lookup"><span data-stu-id="0e403-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="0e403-107">A classe **MicrosoftDNS \_ RootHints** descreve o RootHints armazenado em um arquivo de cache em um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0e403-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="0e403-108">Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real.</span><span class="sxs-lookup"><span data-stu-id="0e403-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="0e403-109">**MicrosoftDNS \_ RootHints** é um contêiner para os registros de recursos armazenados pelo servidor DNS em um arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="0e403-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="0e403-110">Cada instância da classe **MicrosoftDNS \_ RootHints** deve ser atribuída a exatamente um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0e403-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="0e403-111">Ele pode ser associado a várias instâncias da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="0e403-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="0e403-112">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0e403-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e403-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e403-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="0e403-114">Membros</span><span class="sxs-lookup"><span data-stu-id="0e403-114">Members</span></span>

<span data-ttu-id="0e403-115">A classe **MicrosoftDNS \_ RootHints** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0e403-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="0e403-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="0e403-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e403-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="0e403-117">Methods</span></span>

<span data-ttu-id="0e403-118">A classe **MicrosoftDNS \_ RootHints** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0e403-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="0e403-119">Método</span><span class="sxs-lookup"><span data-stu-id="0e403-119">Method</span></span>                        | <span data-ttu-id="0e403-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e403-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e403-121">**Getdistinguiname**</span><span class="sxs-lookup"><span data-stu-id="0e403-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="0e403-122">Recupera o nome distinto da zona.</span><span class="sxs-lookup"><span data-stu-id="0e403-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="0e403-123">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="0e403-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="0e403-124">**WriteBackRootHintDatafile**</span><span class="sxs-lookup"><span data-stu-id="0e403-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="0e403-125">Grava o RootHints de volta no arquivo de cache DNS.</span><span class="sxs-lookup"><span data-stu-id="0e403-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="0e403-126">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="0e403-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0e403-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e403-127">Requirements</span></span>



| <span data-ttu-id="0e403-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e403-128">Requirement</span></span> | <span data-ttu-id="0e403-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0e403-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e403-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e403-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0e403-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0e403-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0e403-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e403-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0e403-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e403-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0e403-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e403-134">Namespace</span></span><br/>                | <span data-ttu-id="0e403-135">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="0e403-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0e403-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0e403-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e403-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e403-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e403-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0e403-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e403-139">**\_Domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0e403-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="0e403-140">**Método WriteBackRootHintDatafile da \_ classe RootHints MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0e403-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="0e403-141">**Método getdistinguiname da classe MicrosoftDNS \_ RootHints**</span><span class="sxs-lookup"><span data-stu-id="0e403-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





