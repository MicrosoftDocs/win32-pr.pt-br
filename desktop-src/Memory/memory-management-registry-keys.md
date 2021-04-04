---
description: O espaço de endereço virtual do sistema (VA) em sistemas de 32 bits pode se esgotar devido à fragmentação. Várias chaves do registro podem ser usadas para configurar limites de memória em sistemas de 32 bits que apresentam esse problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Chaves do registro de gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837412"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="527f5-104">Chaves do registro de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="527f5-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="527f5-105">O espaço de endereço virtual do sistema (VA) em sistemas de 32 bits pode se esgotar devido à fragmentação.</span><span class="sxs-lookup"><span data-stu-id="527f5-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="527f5-106">Várias chaves do registro podem ser usadas para configurar limites de memória em sistemas de 32 bits que apresentam esse problema.</span><span class="sxs-lookup"><span data-stu-id="527f5-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="527f5-107">O espaço do sistema VA nos sistemas de 64 bits não está sujeito ao esgotamento por fragmentação; Portanto, essas chaves não têm nenhum efeito nos sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="527f5-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="527f5-108">Para sistemas de 32 bits, essas chaves do registro de gerenciamento de memória devem ser explicitamente criadas na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="527f5-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="527f5-109">**HKEY \_ \_** Gerenciamento de controle de \\  \\  \\  \\  \\ **memória** do Gerenciador de sessão de controle atual do sistema de máquina local</span><span class="sxs-lookup"><span data-stu-id="527f5-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="527f5-110">**Windows Server 2008 e Windows Vista:** Essas chaves do registro estão disponíveis em sistemas de 32 bits que começam com o Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="527f5-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="527f5-111">Para limites de espaço de endereço e memória padrão em sistemas de 32 bits e 64 bits, consulte [limites de memória para versões do Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="527f5-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="527f5-112">A tabela a seguir descreve as chaves do registro de gerenciamento de memória que podem ser usadas para configurar limites de memória em sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="527f5-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="527f5-113">Todas essas chaves têm um tipo REG \_ DWORD e valores possíveis que variam de 0 a 2.048 MB.</span><span class="sxs-lookup"><span data-stu-id="527f5-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="527f5-114">O padrão é 0, o que significa que nenhum limite é imposto.</span><span class="sxs-lookup"><span data-stu-id="527f5-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="527f5-115">Os valores são arredondados automaticamente para o próximo limite de alocação do sistema VA, que é de 2 MB em sistemas de 32 bits que têm a [extensão de endereço físico](physical-address-extension.md) (PAE) habilitada e 4 MB em sistemas de 32 bits que não têm a PAE habilitada.</span><span class="sxs-lookup"><span data-stu-id="527f5-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="527f5-116">Chave</span><span class="sxs-lookup"><span data-stu-id="527f5-116">Key</span></span>                   | <span data-ttu-id="527f5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="527f5-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="527f5-118">**NonPagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="527f5-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="527f5-119">Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo pool não paginável.</span><span class="sxs-lookup"><span data-stu-id="527f5-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="527f5-120">Em determinadas condições, esse limite pode ser excedido por uma pequena quantidade.</span><span class="sxs-lookup"><span data-stu-id="527f5-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="527f5-121">**PagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="527f5-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="527f5-122">Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo pool paginável.</span><span class="sxs-lookup"><span data-stu-id="527f5-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="527f5-123">**SessionSpaceLimit**</span><span class="sxs-lookup"><span data-stu-id="527f5-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="527f5-124">Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada por alocações de espaço de sessão.</span><span class="sxs-lookup"><span data-stu-id="527f5-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="527f5-125">**SystemCacheLimit**</span><span class="sxs-lookup"><span data-stu-id="527f5-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="527f5-126">Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada pelo cache do sistema.</span><span class="sxs-lookup"><span data-stu-id="527f5-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="527f5-127">Em determinadas condições, esse limite pode ser excedido por uma pequena quantidade.</span><span class="sxs-lookup"><span data-stu-id="527f5-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="527f5-128">**SystemPtesLimit**</span><span class="sxs-lookup"><span data-stu-id="527f5-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="527f5-129">Especifica a quantidade máxima de espaço de VA do sistema que pode ser usada por mapeamentos de e/s e outros recursos que consomem PTEs (entradas de tabela de página do sistema).</span><span class="sxs-lookup"><span data-stu-id="527f5-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="527f5-130">Determinar se o espaço do sistema VA está sendo esgotado requer o uso de um depurador de kernel.</span><span class="sxs-lookup"><span data-stu-id="527f5-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="527f5-131">Para obter mais informações, consulte [Ferramentas de depuração para Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="527f5-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



