---
description: A extensão de endereço físico (PAE) é um recurso de processador que permite que os processadores x86 acessem mais de 4 GB de memória física em versões compatíveis do Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Extensão de endereço físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011843"
---
# <a name="physical-address-extension"></a><span data-ttu-id="657e5-103">Extensão de endereço físico</span><span class="sxs-lookup"><span data-stu-id="657e5-103">Physical Address Extension</span></span>

<span data-ttu-id="657e5-104">A extensão de endereço físico (PAE) é um recurso de processador que permite que os processadores x86 acessem mais de 4 GB de memória física em versões compatíveis do Windows.</span><span class="sxs-lookup"><span data-stu-id="657e5-104">Physical Address Extension (PAE) is a processor feature that enables x86 processors to access more than 4 GB of physical memory on capable versions of Windows.</span></span> <span data-ttu-id="657e5-105">Determinadas versões de 32 bits do Windows Server em execução em sistemas baseados em x86 podem usar o PAE para acessar até 64 GB ou 128 GB de memória física, dependendo do tamanho do endereço físico do processador.</span><span class="sxs-lookup"><span data-stu-id="657e5-105">Certain 32-bit versions of Windows Server running on x86-based systems can use PAE to access up to 64 GB or 128 GB of physical memory, depending on the physical address size of the processor.</span></span> <span data-ttu-id="657e5-106">Para obter detalhes, consulte [limites de memória para versões do Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="657e5-106">For details, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="657e5-107">As arquiteturas de processador Intel Itanium e x64 podem acessar mais de 4 GB de memória física nativamente e, portanto, não fornecem o equivalente de PAE.</span><span class="sxs-lookup"><span data-stu-id="657e5-107">The Intel Itanium and x64 processor architectures can access more than 4 GB of physical memory natively and therefore do not provide the equivalent of PAE.</span></span> <span data-ttu-id="657e5-108">O PAE é usado somente pelas versões de 32 bits do Windows em execução em sistemas baseados em x86.</span><span class="sxs-lookup"><span data-stu-id="657e5-108">PAE is used only by 32-bit versions of Windows running on x86-based systems.</span></span>

<span data-ttu-id="657e5-109">Com o PAE, o sistema operacional passa da conversão de endereços linear de dois níveis para a conversão de endereços de três níveis.</span><span class="sxs-lookup"><span data-stu-id="657e5-109">With PAE, the operating system moves from two-level linear address translation to three-level address translation.</span></span> <span data-ttu-id="657e5-110">Em vez de um endereço linear que está sendo dividido em três campos separados para indexação em tabelas de memória, ele é dividido em quatro campos separados: um Telebit de 2 bits, um bitfields-bit de 2 9 bits e um campo de linhas de 12 bits que corresponde ao tamanho da página implementado pela arquitetura Intel (4 KB).</span><span class="sxs-lookup"><span data-stu-id="657e5-110">Instead of a linear address being split into three separate fields for indexing into memory tables, it is split into four separate fields: a 2-bit bitfield, two 9-bit bitfields, and a 12-bit bitfield that corresponds to the page size implemented by Intel architecture (4 KB).</span></span> <span data-ttu-id="657e5-111">O tamanho das PTEs (entradas de tabela de página) e PDEs (entradas de diretório de página) no modo PAE aumentou de 32 para 64 bits.</span><span class="sxs-lookup"><span data-stu-id="657e5-111">The size of page table entries (PTEs) and page directory entries (PDEs) in PAE mode is increased from 32 to 64 bits.</span></span> <span data-ttu-id="657e5-112">Os bits adicionais permitem que um sistema operacional PTE ou PDE referencie a memória física acima de 4 GB.</span><span class="sxs-lookup"><span data-stu-id="657e5-112">The additional bits allow an operating system PTE or PDE to reference physical memory above 4 GB.</span></span>

<span data-ttu-id="657e5-113">No Windows de 32 bits em execução em sistemas baseados em x64, o PAE também permite vários recursos avançados de sistema e processador, incluindo a DEP ( [prevenção de execução de dados](data-execution-prevention.md) ) habilitada para hardware, o [numa (acesso não uniforme à memória](../procthread/numa-support.md)) e a capacidade de adicionar memória a um sistema enquanto ele está em execução (adição de memória a quente).</span><span class="sxs-lookup"><span data-stu-id="657e5-113">In 32-bit Windows running on x64-based systems, PAE also enables several advanced system and processor features, including hardware-enabled [Data Execution Prevention](data-execution-prevention.md) (DEP), [non-uniform memory access (NUMA)](../procthread/numa-support.md), and the ability to add memory to a system while it is running (hot-add memory).</span></span>

<span data-ttu-id="657e5-114">O PAE não altera a quantidade de espaço de endereço virtual disponível para um processo.</span><span class="sxs-lookup"><span data-stu-id="657e5-114">PAE does not change the amount of virtual address space available to a process.</span></span> <span data-ttu-id="657e5-115">Cada processo em execução no Windows de 32 bits ainda está limitado a um espaço de endereço virtual de 4 GB.</span><span class="sxs-lookup"><span data-stu-id="657e5-115">Each process running in 32-bit Windows is still limited to a 4 GB virtual address space.</span></span>

## <a name="system-support-for-pae"></a><span data-ttu-id="657e5-116">Suporte do sistema para PAE</span><span class="sxs-lookup"><span data-stu-id="657e5-116">System Support for PAE</span></span>

<span data-ttu-id="657e5-117">O PAE tem suporte apenas nas seguintes versões de 32 bits do Windows em execução em sistemas baseados em x86:</span><span class="sxs-lookup"><span data-stu-id="657e5-117">PAE is supported only on the following 32-bit versions of Windows running on x86-based systems:</span></span>

-   <span data-ttu-id="657e5-118">Windows 7 (somente 32 bits)</span><span class="sxs-lookup"><span data-stu-id="657e5-118">Windows 7 (32 bit only)</span></span>
-   <span data-ttu-id="657e5-119">Windows Server 2008 (somente 32 bits)</span><span class="sxs-lookup"><span data-stu-id="657e5-119">Windows Server 2008 (32-bit only)</span></span>
-   <span data-ttu-id="657e5-120">Windows Vista (somente 32 bits)</span><span class="sxs-lookup"><span data-stu-id="657e5-120">Windows Vista (32-bit only)</span></span>
-   <span data-ttu-id="657e5-121">Windows Server 2003 (somente 32 bits)</span><span class="sxs-lookup"><span data-stu-id="657e5-121">Windows Server 2003 (32-bit only)</span></span>
-   <span data-ttu-id="657e5-122">Windows XP (somente 32 bits)</span><span class="sxs-lookup"><span data-stu-id="657e5-122">Windows XP (32-bit only)</span></span>

## <a name="enabling-pae"></a><span data-ttu-id="657e5-123">Habilitando PAE</span><span class="sxs-lookup"><span data-stu-id="657e5-123">Enabling PAE</span></span>

<span data-ttu-id="657e5-124">O Windows habilita automaticamente o PAE se a DEP estiver habilitada em um computador com suporte para DEP habilitada para hardware ou se o computador estiver configurado para adicionar dispositivos de memória a quente em intervalos de memória além de 4 GB.</span><span class="sxs-lookup"><span data-stu-id="657e5-124">Windows automatically enables PAE if DEP is enabled on a computer that supports hardware-enabled DEP, or if the computer is configured for hot-add memory devices in memory ranges beyond 4 GB.</span></span> <span data-ttu-id="657e5-125">Se o computador não oferecer suporte a DEP habilitada para hardware ou não estiver configurado para adicionar dispositivos de memória a quente em intervalos de memória além de 4 GB, a PAE deverá ser habilitada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="657e5-125">If the computer does not support hardware-enabled DEP or is not configured for hot-add memory devices in memory ranges beyond 4 GB, PAE must be explicitly enabled.</span></span>

<span data-ttu-id="657e5-126">Para habilitar explicitamente o PAE, use o seguinte comando [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) para definir a opção de entrada de inicialização de **PAE** :</span><span class="sxs-lookup"><span data-stu-id="657e5-126">To explicitly enable PAE, use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) command to set the **pae** boot entry option:</span></span>

 <span data-ttu-id="657e5-127">**bcdedit/set \[ {ID} \] PAE ForceEnable**</span><span class="sxs-lookup"><span data-stu-id="657e5-127">**bcdedit /set \[{ID}\] pae ForceEnable**</span></span>  


<span data-ttu-id="657e5-128">SE a DEP estiver habilitada, o PAE não poderá ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="657e5-128">IF DEP is enabled, PAE cannot be disabled.</span></span> <span data-ttu-id="657e5-129">Use os seguintes comandos [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) para desabilitar o DEP e o PAE:</span><span class="sxs-lookup"><span data-stu-id="657e5-129">Use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) commands to disable both DEP and PAE:</span></span>

 <span data-ttu-id="657e5-130">**bcdedit/set \[ {ID} \] NX AlwaysOff**</span><span class="sxs-lookup"><span data-stu-id="657e5-130">**bcdedit /set \[{ID}\] nx AlwaysOff**</span></span>  
<span data-ttu-id="657e5-131">**bcdedit/set \[ {ID} \] PAE ForceDisable**</span><span class="sxs-lookup"><span data-stu-id="657e5-131">**bcdedit /set \[{ID}\] pae ForceDisable**</span></span>  


<span data-ttu-id="657e5-132">**Windows Server 2003 e Windows XP:** Para habilitar o PAE, use a opção **/PAE** no arquivo de [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) .</span><span class="sxs-lookup"><span data-stu-id="657e5-132">**Windows Server 2003 and Windows XP:** To enable PAE, use the **/PAE** switch in the [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) file.</span></span> <span data-ttu-id="657e5-133">Para desabilitar o PAE, use a opção **/NOPAE**</span><span class="sxs-lookup"><span data-stu-id="657e5-133">To disable PAE, use the **/NOPAE** switch.</span></span> <span data-ttu-id="657e5-134">Para desabilitar o DEP, use a opção **/Execute** .</span><span class="sxs-lookup"><span data-stu-id="657e5-134">To disable DEP, use the **/EXECUTE** switch.</span></span>

## <a name="comparing-pae-and-other-large-memory-support"></a><span data-ttu-id="657e5-135">Comparando o PAE e outros suporte de memória grande</span><span class="sxs-lookup"><span data-stu-id="657e5-135">Comparing PAE and other Large Memory Support</span></span>

<span data-ttu-id="657e5-136">PAE, [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) e [extensões de janelas de endereço](address-windowing-extensions.md) (AWE) servem para diferentes finalidades e podem ser usados independentemente um do outro:</span><span class="sxs-lookup"><span data-stu-id="657e5-136">PAE, [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT), and [Address Windowing Extensions](address-windowing-extensions.md) (AWE) serve different purposes and can be used independently of each other:</span></span>

-   <span data-ttu-id="657e5-137">O PAE permite que o sistema operacional acesse e use mais de 4 GB de memória física.</span><span class="sxs-lookup"><span data-stu-id="657e5-137">PAE allows the operating system to access and use more than 4 GB of physical memory.</span></span>
-   <span data-ttu-id="657e5-138">4GT aumenta a parte do espaço de endereço virtual disponível para um processo de 2 GB para até 3 GB.</span><span class="sxs-lookup"><span data-stu-id="657e5-138">4GT increases the portion of the virtual address space that is available to a process from 2 GB to up to 3 GB.</span></span>
-   <span data-ttu-id="657e5-139">O AWE é um conjunto de APIs que permite a um processo alocar memória física não paginável e, em seguida, mapear dinamicamente partes dessa memória para o espaço de endereço virtual do processo.</span><span class="sxs-lookup"><span data-stu-id="657e5-139">AWE is a set of APIs that allows a process to allocate nonpaged physical memory and then dynamically map portions of this memory into the virtual address space of the process.</span></span>

<span data-ttu-id="657e5-140">Quando não há nenhum 4GT nem AWE sendo usado, a quantidade de memória física que um único processo de 32 bits pode usar é limitada pelo tamanho de seu espaço de endereço (2 GB).</span><span class="sxs-lookup"><span data-stu-id="657e5-140">When neither 4GT nor AWE are being used, the amount of physical memory that a single 32-bit process can use is limited by the size of its address space (2 GB).</span></span> <span data-ttu-id="657e5-141">Nesse caso, um sistema habilitado para PAE ainda pode usar mais de 4 GB de RAM para executar vários processos ao mesmo tempo ou para armazenar em cache os dados de arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="657e5-141">In this case, a PAE-enabled system can still make use of more than 4 GB of RAM to run multiple processes at the same time or to cache file data in memory.</span></span>

<span data-ttu-id="657e5-142">4GT pode ser usado com ou sem PAE.</span><span class="sxs-lookup"><span data-stu-id="657e5-142">4GT can be used with or without PAE.</span></span> <span data-ttu-id="657e5-143">No entanto, algumas versões do Windows limitam a quantidade máxima de memória física que pode ter suporte quando 4GT é usado.</span><span class="sxs-lookup"><span data-stu-id="657e5-143">However, some versions of Windows limit the maximum amount of physical memory that can be supported when 4GT is used.</span></span> <span data-ttu-id="657e5-144">Em tais sistemas, a inicialização com 4GT habilitado faz com que o sistema operacional ignore qualquer memória que ultrapasse o limite.</span><span class="sxs-lookup"><span data-stu-id="657e5-144">On such systems, booting with 4GT enabled causes the operating system to ignore any memory in excess of the limit.</span></span>

<span data-ttu-id="657e5-145">O AWE não requer PAE ou 4GT, mas geralmente é usado junto com o PAE para alocar mais de 4 GB de memória física a partir de um único processo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="657e5-145">AWE does not require PAE or 4GT but is often used together with PAE to allocate more than 4 GB of physical memory from a single 32-bit process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="657e5-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="657e5-146">Related topics</span></span>



[<span data-ttu-id="657e5-147">**IsProcessorFeaturePresent**</span><span class="sxs-lookup"><span data-stu-id="657e5-147">**IsProcessorFeaturePresent**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

<span data-ttu-id="657e5-148">[Referência técnica do PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="657e5-148">[PAE X86 Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span></span>
</dt> </dl>

 

 
