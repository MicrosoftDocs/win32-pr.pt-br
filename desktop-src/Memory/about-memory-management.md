---
description: Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite o endereçamento de até 4 gigabytes de memória.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Sobre o gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767626"
---
# <a name="about-memory-management"></a><span data-ttu-id="97113-103">Sobre o gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="97113-103">About Memory Management</span></span>

<span data-ttu-id="97113-104">Cada processo no Microsoft Windows de 32 bits tem seu próprio espaço de endereço virtual que permite o endereçamento de até 4 gigabytes de memória.</span><span class="sxs-lookup"><span data-stu-id="97113-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="97113-105">Cada processo no Windows de 64 bits tem um espaço de endereço virtual de 8 terabytes.</span><span class="sxs-lookup"><span data-stu-id="97113-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="97113-106">Todos os threads de um processo podem acessar seu espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="97113-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="97113-107">No entanto, os threads não podem acessar a memória que pertence a outro processo, o que protege um processo de ser corrompido por outro processo.</span><span class="sxs-lookup"><span data-stu-id="97113-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="97113-108">Para obter informações sobre o espaço de endereço virtual e as funções de gerenciamento de memória, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="97113-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="97113-109">Espaço de endereço virtual</span><span class="sxs-lookup"><span data-stu-id="97113-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="97113-110">Pools de memória</span><span class="sxs-lookup"><span data-stu-id="97113-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="97113-111">Informações de desempenho da memória</span><span class="sxs-lookup"><span data-stu-id="97113-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="97113-112">Funções de memória virtual</span><span class="sxs-lookup"><span data-stu-id="97113-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="97113-113">Funções de heap</span><span class="sxs-lookup"><span data-stu-id="97113-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="97113-114">Mapeamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="97113-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="97113-115">Suporte a memória grande</span><span class="sxs-lookup"><span data-stu-id="97113-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="97113-116">Funções globais e locais</span><span class="sxs-lookup"><span data-stu-id="97113-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="97113-117">Funções da biblioteca C padrão</span><span class="sxs-lookup"><span data-stu-id="97113-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="97113-118">Comparando métodos de alocação de memória</span><span class="sxs-lookup"><span data-stu-id="97113-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



