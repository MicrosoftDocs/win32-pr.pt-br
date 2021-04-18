---
description: O recurso de partições COM+ inclui um cache de partição. Esse cache armazena mapeamentos de usuário para partição e é projetado para evitar o acesso Active Directory repetitivo.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurando o cache de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771496"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="29723-104">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="29723-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="29723-105">O recurso de partições COM+ inclui um cache de partição.</span><span class="sxs-lookup"><span data-stu-id="29723-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="29723-106">Esse cache armazena mapeamentos de usuário para partição e é projetado para evitar o acesso Active Directory repetitivo.</span><span class="sxs-lookup"><span data-stu-id="29723-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="29723-107">Alterando o tamanho do cache</span><span class="sxs-lookup"><span data-stu-id="29723-107">Changing Cache Size</span></span>

<span data-ttu-id="29723-108">O cache de partição consiste em três tabelas, cujo tamanho pode ser modificado para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="29723-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="29723-109">Essas tabelas consistem no número de entradas de SID no cache, no número de entradas de UO no cache e no número de entradas de partição no cache.</span><span class="sxs-lookup"><span data-stu-id="29723-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="29723-110">Para alterar esses tamanhos de tabela, os administradores podem modificar os valores de uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="29723-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="29723-111">A chave do registro e seus valores são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="29723-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="29723-112">**HKLM \\ software \\ Microsoft \\ com3 \\ PartitionCache**</span><span class="sxs-lookup"><span data-stu-id="29723-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="29723-113">Valores da chave</span><span class="sxs-lookup"><span data-stu-id="29723-113">Key values</span></span>                         | <span data-ttu-id="29723-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="29723-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29723-115">**NumSidEntries**</span><span class="sxs-lookup"><span data-stu-id="29723-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="29723-116">Contém o valor de REG \_ DWORD para o número de entradas de Sid no cache (padrão = 512).</span><span class="sxs-lookup"><span data-stu-id="29723-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="29723-117">Esse valor deve ser definido como um valor maior que o número de identidades exclusivas que um computador servirá na janela de tempo de invalidação de cache.</span><span class="sxs-lookup"><span data-stu-id="29723-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="29723-118">**NumNameEntries**</span><span class="sxs-lookup"><span data-stu-id="29723-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="29723-119">Contém o valor de REG \_ DWORD para o número de entradas de nome de UO no cache (padrão = 64).</span><span class="sxs-lookup"><span data-stu-id="29723-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="29723-120">Esse valor deve ser definido como um valor maior que o número de nomes de UO exclusivos que um computador atenderá na janela de tempo de invalidação de cache.</span><span class="sxs-lookup"><span data-stu-id="29723-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="29723-121">**NumPartitionEntries**</span><span class="sxs-lookup"><span data-stu-id="29723-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="29723-122">Contém o valor de REG \_ DWORD para o número de entradas de partição no cache (padrão = 1024).</span><span class="sxs-lookup"><span data-stu-id="29723-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="29723-123">Na janela tempo de invalidação do cache, o valor DWORD deve ser definido como um número maior que o número de partições exclusivas que um computador atenderá.</span><span class="sxs-lookup"><span data-stu-id="29723-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="29723-124">Isso ocorre porque o contexto de um componente pode incluir uma ID de partição para uma partição que não reside nesse computador.</span><span class="sxs-lookup"><span data-stu-id="29723-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="29723-125">**EntryExpiration**</span><span class="sxs-lookup"><span data-stu-id="29723-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="29723-126">Contém o valor de REG \_ DWORD para a contagem de tiques (cada tique = ~ 7 minutos) até que uma entrada de cache se torne inválida (padrão = 4 (~ 28 minutos)).</span><span class="sxs-lookup"><span data-stu-id="29723-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="29723-127">Liberando o cache</span><span class="sxs-lookup"><span data-stu-id="29723-127">Flushing the Cache</span></span>

<span data-ttu-id="29723-128">Como o COM+ armazena em cache a partição padrão para os usuários, você talvez queira chamar esse método depois de alterar a partição padrão para um usuário na Active Directory.</span><span class="sxs-lookup"><span data-stu-id="29723-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="29723-129">Os administradores podem fazer isso programaticamente chamando o método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="29723-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29723-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29723-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29723-131">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="29723-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="29723-132">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="29723-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="29723-133">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="29723-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="29723-134">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="29723-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="29723-135">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="29723-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




