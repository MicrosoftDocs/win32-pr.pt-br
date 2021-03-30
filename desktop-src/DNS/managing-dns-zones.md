---
title: Gerenciando Zonas DNS
description: Uma zona DNS é um banco de dados de entradas de RR que corresponde a parte do espaço de nome hierárquico DNS. As zonas DNS são usadas para delinear quais servidores DNS são autoritativos para resolver consultas de resolução de nomes para uma determinada seção da hierarquia de DNS.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636543"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="1d8ca-104">Gerenciando Zonas DNS</span><span class="sxs-lookup"><span data-stu-id="1d8ca-104">Managing DNS Zones</span></span>

<span data-ttu-id="1d8ca-105">Uma zona DNS é um banco de dados de entradas de RR que corresponde a parte do espaço de nome hierárquico DNS.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="1d8ca-106">As zonas DNS são usadas para delinear quais servidores DNS são autoritativos para resolver consultas de resolução de nomes para uma determinada seção da hierarquia de DNS.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="1d8ca-107">Etapas de administração</span><span class="sxs-lookup"><span data-stu-id="1d8ca-107">Administration Steps</span></span>

<span data-ttu-id="1d8ca-108">O provedor WMI de DNS permite a administração de zonas DNS do próprio servidor DNS autoritativo ou de hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="1d8ca-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="1d8ca-109">As etapas gerais necessárias para administrar uma zona usando o provedor WMI de DNS são:</span><span class="sxs-lookup"><span data-stu-id="1d8ca-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="1d8ca-110">Conectando-se ao provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="1d8ca-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="1d8ca-111">Obtendo uma instância de zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-111">Getting a zone instance</span></span>
-   <span data-ttu-id="1d8ca-112">Listando ou modificando uma propriedade de zona ou usando um método</span><span class="sxs-lookup"><span data-stu-id="1d8ca-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="1d8ca-113">As seguintes tarefas estão vinculadas aos seus exemplos de script associados:</span><span class="sxs-lookup"><span data-stu-id="1d8ca-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="1d8ca-114">Criando uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="1d8ca-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-115">Modificando uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="1d8ca-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-116">Excluindo uma zona DNS</span><span class="sxs-lookup"><span data-stu-id="1d8ca-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-117">Adicionando um endereço IP de zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-118">Excluindo um endereço IP de zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-119">Pausando uma zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-120">Retomando uma zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-121">Atualizando uma zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-122">Recarregando uma zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="1d8ca-123">Atualizando uma zona</span><span class="sxs-lookup"><span data-stu-id="1d8ca-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




