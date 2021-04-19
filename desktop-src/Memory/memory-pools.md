---
description: 'O Gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não paginável e pool paginável.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pools de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810158"
---
# <a name="memory-pools"></a><span data-ttu-id="259c7-103">Pools de memória</span><span class="sxs-lookup"><span data-stu-id="259c7-103">Memory Pools</span></span>

<span data-ttu-id="259c7-104">O Gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não paginável e pool paginável.</span><span class="sxs-lookup"><span data-stu-id="259c7-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="259c7-105">Ambos os pools de memória estão localizados na região do espaço de endereço reservado para o sistema e mapeados para o espaço de endereço virtual de cada processo.</span><span class="sxs-lookup"><span data-stu-id="259c7-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="259c7-106">O pool não paginável consiste em endereços de memória virtual que têm garantia de residir na memória física, contanto que os objetos kernel correspondentes sejam alocados.</span><span class="sxs-lookup"><span data-stu-id="259c7-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="259c7-107">O pool paginável consiste em memória virtual que pode ser paginada dentro e fora do sistema.</span><span class="sxs-lookup"><span data-stu-id="259c7-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="259c7-108">Para melhorar o desempenho, os sistemas com um único processador têm três pools paginável, e sistemas multiprocessadores têm cinco pools paginados.</span><span class="sxs-lookup"><span data-stu-id="259c7-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="259c7-109">Os identificadores de [objetos kernel](../sysinfo/kernel-objects.md) são armazenados no pool paginável, de modo que o número de identificadores que você pode criar é baseado na memória disponível.</span><span class="sxs-lookup"><span data-stu-id="259c7-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="259c7-110">O sistema registra os limites e os valores atuais para seu pool não paginável, pool paginável e uso do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="259c7-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="259c7-111">Para obter mais informações, consulte [informações de desempenho da memória](memory-performance-information.md).</span><span class="sxs-lookup"><span data-stu-id="259c7-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
