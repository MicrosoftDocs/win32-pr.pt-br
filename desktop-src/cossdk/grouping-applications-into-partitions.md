---
description: Agrupando aplicativos em partições
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupando aplicativos em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778518"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="a6bc2-103">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="a6bc2-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="a6bc2-104">Ao decidir como agrupar aplicativos em partições, os administradores precisam estar cientes de determinadas regras e restrições, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="a6bc2-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="a6bc2-105">Um aplicativo pode ser instalado em uma ou mais partições.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="a6bc2-106">Somente uma instância de um determinado componente pode existir em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="a6bc2-107">Componentes públicos e privados</span><span class="sxs-lookup"><span data-stu-id="a6bc2-107">Public and Private Components</span></span>

<span data-ttu-id="a6bc2-108">Existem outras restrições ao decidir como agrupar aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="a6bc2-109">Essas restrições pertencem a componentes públicos versus privados em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="a6bc2-110">Os componentes do aplicativo geralmente podem ser públicos ou privados.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="a6bc2-111">No entanto, ao agrupar aplicativos em partições, os administradores devem estar cientes de algumas restrições em relação a componentes públicos e privados.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="a6bc2-112">A tabela a seguir lista essas restrições.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="a6bc2-113">Se um aplicativo for:</span><span class="sxs-lookup"><span data-stu-id="a6bc2-113">If an application is:</span></span>              | <span data-ttu-id="a6bc2-114">Em seguida, os componentes em uma partição podem ser:</span><span class="sxs-lookup"><span data-stu-id="a6bc2-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bc2-115">Um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="a6bc2-115">A server application</span></span><br/>    | <span data-ttu-id="a6bc2-116">Público e privado.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="a6bc2-117">Um aplicativo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6bc2-117">A library application</span></span><br/>   | <span data-ttu-id="a6bc2-118">Somente público.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-118">Public only.</span></span> <span data-ttu-id="a6bc2-119">Caso contrário, o aplicativo de chamadores poderia ter os mesmos componentes, o que criaria ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="a6bc2-120">Na partição global</span><span class="sxs-lookup"><span data-stu-id="a6bc2-120">In the global partition</span></span><br/> | <span data-ttu-id="a6bc2-121">Somente público.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-121">Public only.</span></span> <span data-ttu-id="a6bc2-122">Isso garante a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="a6bc2-123">IDs de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a6bc2-123">Application IDs</span></span>

<span data-ttu-id="a6bc2-124">Cada aplicativo COM+ instalado em um computador tem uma ID de aplicativo exclusiva.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="a6bc2-125">No entanto, os nomes de aplicativos só precisam ser exclusivos em uma única partição e não em todo o computador.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="a6bc2-126">A tabela a seguir mostra o que acontece com a ID do aplicativo quando um aplicativo é importado para uma partição ou exportada de uma partição.</span><span class="sxs-lookup"><span data-stu-id="a6bc2-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="a6bc2-127">Se um aplicativo for:</span><span class="sxs-lookup"><span data-stu-id="a6bc2-127">If an application is:</span></span>                                              | <span data-ttu-id="a6bc2-128">Em seguida, a ID do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="a6bc2-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="a6bc2-129">Importado para a partição global</span><span class="sxs-lookup"><span data-stu-id="a6bc2-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="a6bc2-130">Permanece o mesmo</span><span class="sxs-lookup"><span data-stu-id="a6bc2-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="a6bc2-131">Importado para uma partição que não seja a partição global</span><span class="sxs-lookup"><span data-stu-id="a6bc2-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="a6bc2-132">É alterado</span><span class="sxs-lookup"><span data-stu-id="a6bc2-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="a6bc2-133">Exportado</span><span class="sxs-lookup"><span data-stu-id="a6bc2-133">Exported</span></span><br/>                                                | <span data-ttu-id="a6bc2-134">Está incluído no arquivo exportado</span><span class="sxs-lookup"><span data-stu-id="a6bc2-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a6bc2-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6bc2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6bc2-136">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="a6bc2-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="a6bc2-137">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="a6bc2-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="a6bc2-138">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="a6bc2-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="a6bc2-139">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="a6bc2-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="a6bc2-140">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="a6bc2-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




