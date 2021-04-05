---
description: O espaço de endereço virtual para um processo é o conjunto de endereços de memória virtual que ele pode usar. O espaço de endereço para cada processo é privado e não pode ser acessado por outros processos, a menos que ele seja compartilhado.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espaço de endereço virtual (gerenciamento de memória)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921064"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="b2228-104">Espaço de endereço virtual (gerenciamento de memória)</span><span class="sxs-lookup"><span data-stu-id="b2228-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="b2228-105">O espaço de endereço virtual para um processo é o conjunto de endereços de memória virtual que ele pode usar.</span><span class="sxs-lookup"><span data-stu-id="b2228-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="b2228-106">O espaço de endereço para cada processo é privado e não pode ser acessado por outros processos, a menos que ele seja compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b2228-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="b2228-107">Um endereço virtual não representa o local físico real de um objeto na memória; em vez disso, o sistema mantém uma *tabela de página* para cada processo, que é uma estrutura de dados interna usada para converter endereços virtuais em seus endereços físicos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b2228-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="b2228-108">Cada vez que um thread faz referência a um endereço, o sistema converte o endereço virtual em um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="b2228-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="b2228-109">O espaço de endereço virtual para o Windows de 32 bits é de 4 gigabytes (GB) de tamanho e dividido em duas partições: uma para uso pelo processo e a outra reservada para uso pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b2228-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="b2228-110">Para obter mais informações sobre o espaço de endereço virtual no Windows de 64 bits, consulte [espaço de endereço virtual no Windows de 64 bits](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="b2228-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="b2228-111">Para obter mais informações sobre memória virtual, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b2228-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="b2228-112">Espaço de endereço virtual e armazenamento físico</span><span class="sxs-lookup"><span data-stu-id="b2228-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="b2228-113">Conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="b2228-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="b2228-114">Estado da página</span><span class="sxs-lookup"><span data-stu-id="b2228-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="b2228-115">Escopo da memória alocada</span><span class="sxs-lookup"><span data-stu-id="b2228-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="b2228-116">Prevenção de execução de dados</span><span class="sxs-lookup"><span data-stu-id="b2228-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="b2228-117">Proteção de memória</span><span class="sxs-lookup"><span data-stu-id="b2228-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="b2228-118">Limites de memória para versões do Windows</span><span class="sxs-lookup"><span data-stu-id="b2228-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="b2228-119">Espaço de endereço virtual padrão para o Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="b2228-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="b2228-120">A tabela a seguir mostra o intervalo de memória padrão para cada partição.</span><span class="sxs-lookup"><span data-stu-id="b2228-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="b2228-121">Intervalo de memória</span><span class="sxs-lookup"><span data-stu-id="b2228-121">Memory range</span></span>                             | <span data-ttu-id="b2228-122">Uso</span><span class="sxs-lookup"><span data-stu-id="b2228-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="b2228-123">2 GB baixos (0x00000000 a 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="b2228-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="b2228-124">Usado pelo processo.</span><span class="sxs-lookup"><span data-stu-id="b2228-124">Used by the process.</span></span> |
| <span data-ttu-id="b2228-125">Alto GB (0x80000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="b2228-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="b2228-126">Usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b2228-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="b2228-127">Espaço de endereço virtual para Windows de 32 bits com 4GT</span><span class="sxs-lookup"><span data-stu-id="b2228-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="b2228-128">Se o [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) estiver habilitado, o intervalo de memória para cada partição será o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b2228-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="b2228-129">Intervalo de memória</span><span class="sxs-lookup"><span data-stu-id="b2228-129">Memory range</span></span>                             | <span data-ttu-id="b2228-130">Uso</span><span class="sxs-lookup"><span data-stu-id="b2228-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="b2228-131">3GB baixos (0x00000000 a 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="b2228-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="b2228-132">Usado pelo processo.</span><span class="sxs-lookup"><span data-stu-id="b2228-132">Used by the process.</span></span> |
| <span data-ttu-id="b2228-133">Alta 1GB (0xC0000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="b2228-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="b2228-134">Usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b2228-134">Used by the system.</span></span>  |



 

<span data-ttu-id="b2228-135">Depois que 4GT estiver habilitado, um processo que tem o sinalizador de [**\_ \_ \_ \_ reconhecimento de endereço grande de arquivo de imagem**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) definido em seu cabeçalho de imagem terá acesso a 1 GB de memória adicional acima dos 2 GB baixos.</span><span class="sxs-lookup"><span data-stu-id="b2228-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="b2228-136">Ajustando o espaço de endereço virtual para o Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="b2228-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="b2228-137">Você pode usar o comando a seguir para definir uma opção de entrada de inicialização que configura o tamanho da partição que está disponível para uso pelo processo para um valor entre 2048 (2 GB) e 3072 (3 GB):</span><span class="sxs-lookup"><span data-stu-id="b2228-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="b2228-138">[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **IncreaseUserVa** *megabytes*</span><span class="sxs-lookup"><span data-stu-id="b2228-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="b2228-139">Depois que a opção de entrada de inicialização é definida, o intervalo de memória para cada partição é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b2228-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="b2228-140">Intervalo de memória</span><span class="sxs-lookup"><span data-stu-id="b2228-140">Memory range</span></span>                            | <span data-ttu-id="b2228-141">Uso</span><span class="sxs-lookup"><span data-stu-id="b2228-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="b2228-142">Baixa (0x00000000 a *megabytes*)</span><span class="sxs-lookup"><span data-stu-id="b2228-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="b2228-143">Usado pelo processo.</span><span class="sxs-lookup"><span data-stu-id="b2228-143">Used by the process.</span></span> |
| <span data-ttu-id="b2228-144">Alta (*megabytes*+ 1 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="b2228-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="b2228-145">Usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b2228-145">Used by the system.</span></span>  |



 

<span data-ttu-id="b2228-146">**Windows Server 2003:** Defina a opção **/USERVA** em boot.ini como um valor entre 2048 e 3072.</span><span class="sxs-lookup"><span data-stu-id="b2228-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
