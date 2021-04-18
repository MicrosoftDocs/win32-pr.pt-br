---
description: As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funções de memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780620"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="00842-103">Funções de memória virtual</span><span class="sxs-lookup"><span data-stu-id="00842-103">Virtual Memory Functions</span></span>

<span data-ttu-id="00842-104">As funções de memória virtual permitem que um processo manipule ou determine o status das páginas em seu espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="00842-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="00842-105">Eles podem executar as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="00842-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="00842-106">Reserve um intervalo de espaço de endereço virtual de um processo.</span><span class="sxs-lookup"><span data-stu-id="00842-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="00842-107">Reservar espaço de endereço não aloca nenhum armazenamento físico, mas impede que outras operações de alocação usem o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="00842-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="00842-108">Ele não afeta os espaços de endereço virtual de outros processos.</span><span class="sxs-lookup"><span data-stu-id="00842-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="00842-109">Reservar páginas impede o consumo de armazenamento físico necessário, ao mesmo tempo em que permite que um processo Reserve um intervalo de seu espaço de endereço no qual uma estrutura de dados dinâmica pode crescer.</span><span class="sxs-lookup"><span data-stu-id="00842-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="00842-110">O processo pode alocar armazenamento físico para esse espaço, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="00842-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="00842-111">Confirme um intervalo de páginas reservadas no espaço de endereço virtual de um processo para que o armazenamento físico (na RAM ou no disco) seja acessível somente para o processo de alocação.</span><span class="sxs-lookup"><span data-stu-id="00842-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="00842-112">Especifique leitura/gravação, somente leitura ou nenhum acesso para um intervalo de páginas confirmadas.</span><span class="sxs-lookup"><span data-stu-id="00842-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="00842-113">Isso difere das funções de alocação padrão que sempre alocam páginas com acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="00842-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="00842-114">Libere uma variedade de páginas reservadas, tornando o intervalo de endereços virtuais disponíveis para operações de alocação subsequentes pelo processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="00842-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="00842-115">Desconfirme um intervalo de páginas confirmadas, liberando seu armazenamento físico e disponibilizando-a para alocação subsequente por qualquer processo.</span><span class="sxs-lookup"><span data-stu-id="00842-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="00842-116">Bloqueie uma ou mais páginas de memória confirmada na RAM (memória física) para que o sistema não possa trocar as páginas no arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="00842-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="00842-117">Obtenha informações sobre um intervalo de páginas no espaço de endereço virtual do processo de chamada ou um processo especificado.</span><span class="sxs-lookup"><span data-stu-id="00842-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="00842-118">Alterar a proteção de acesso para um intervalo especificado de páginas confirmadas no espaço de endereço virtual do processo de chamada ou um processo especificado.</span><span class="sxs-lookup"><span data-stu-id="00842-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="00842-119">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="00842-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="00842-120">Alocando memória virtual</span><span class="sxs-lookup"><span data-stu-id="00842-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="00842-121">Comparando métodos de alocação de memória</span><span class="sxs-lookup"><span data-stu-id="00842-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="00842-122">Liberando memória virtual</span><span class="sxs-lookup"><span data-stu-id="00842-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="00842-123">Trabalhando com páginas</span><span class="sxs-lookup"><span data-stu-id="00842-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="00842-124">Funções de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="00842-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



