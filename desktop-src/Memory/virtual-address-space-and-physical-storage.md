---
description: A quantidade máxima de memória física com suporte do Microsoft Windows varia de 2 GB a 2 TB, dependendo da versão do Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espaço de endereço virtual e armazenamento físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505806"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="9fee4-103">Espaço de endereço virtual e armazenamento físico</span><span class="sxs-lookup"><span data-stu-id="9fee4-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="9fee4-104">A quantidade máxima de memória física com suporte do Microsoft Windows varia de 2 GB a 24 TB, dependendo da versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fee4-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="9fee4-105">Para obter mais informações, consulte [limites de memória para versões do Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="9fee4-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="9fee4-106">O espaço de endereço virtual de cada processo pode ser menor ou maior do que a memória física total disponível no computador.</span><span class="sxs-lookup"><span data-stu-id="9fee4-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="9fee4-107">O subconjunto do espaço de endereço virtual de um processo que reside na memória física é conhecido como o *conjunto de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="9fee4-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="9fee4-108">Se os threads de um processo tentarem usar mais memória física do que o disponível no momento, o sistema paginará parte do conteúdo da memória para o disco.</span><span class="sxs-lookup"><span data-stu-id="9fee4-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="9fee4-109">A quantidade total de espaço de endereço virtual disponível para um processo é limitada pela memória física e o espaço livre em disco disponível para o arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="9fee4-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="9fee4-110">O armazenamento físico e o espaço de endereço virtual de cada processo são organizados em *páginas*, unidades de memória, cujo tamanho depende do computador host.</span><span class="sxs-lookup"><span data-stu-id="9fee4-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="9fee4-111">Por exemplo, em computadores x86, o tamanho da página do host é de 4 quilobytes.</span><span class="sxs-lookup"><span data-stu-id="9fee4-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="9fee4-112">Para maximizar sua flexibilidade no gerenciamento de memória, o sistema pode mover páginas de memória física de e para um arquivo de paginação no disco.</span><span class="sxs-lookup"><span data-stu-id="9fee4-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="9fee4-113">Quando uma página é movida na memória física, o sistema atualiza os mapas de página dos processos afetados.</span><span class="sxs-lookup"><span data-stu-id="9fee4-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="9fee4-114">Quando o sistema precisa de espaço na memória física, ele move as páginas usadas menos recentemente da memória física para o arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="9fee4-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="9fee4-115">A manipulação de memória física pelo sistema é completamente transparente para aplicativos, que operam somente em seus espaços de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="9fee4-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



