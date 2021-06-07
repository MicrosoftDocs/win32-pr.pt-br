---
description: O conjunto de trabalho de um programa é uma coleção dessas páginas em seu espaço de endereço virtual que foram referenciadas recentemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Conjunto de trabalho do processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549898"
---
# <a name="process-working-set"></a><span data-ttu-id="1a299-103">Conjunto de trabalho do processo</span><span class="sxs-lookup"><span data-stu-id="1a299-103">Process Working Set</span></span>

<span data-ttu-id="1a299-104">O *conjunto de* trabalho de um programa é uma coleção dessas páginas em seu espaço de endereço virtual que foram referenciadas recentemente.</span><span class="sxs-lookup"><span data-stu-id="1a299-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="1a299-105">Ele inclui dados compartilhados e privados.</span><span class="sxs-lookup"><span data-stu-id="1a299-105">It includes both shared and private data.</span></span> <span data-ttu-id="1a299-106">Os dados compartilhados incluem páginas que contêm todas as instruções que seu aplicativo executa, incluindo aquelas em suas DLLs e as DLLs do sistema.</span><span class="sxs-lookup"><span data-stu-id="1a299-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="1a299-107">À medida que o tamanho do conjunto de trabalho aumenta, a demanda de memória aumenta.</span><span class="sxs-lookup"><span data-stu-id="1a299-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="1a299-108">Um processo tem um tamanho mínimo do conjunto de trabalho associado e o tamanho máximo do conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a299-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="1a299-109">Cada vez que você chama [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), ele reserva o tamanho mínimo do conjunto de trabalho para o processo.</span><span class="sxs-lookup"><span data-stu-id="1a299-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="1a299-110">O gerenciador de memória virtual tenta manter memória suficiente para o conjunto de trabalho mínimo residente quando o processo está ativo, mas não mantém mais do que o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="1a299-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="1a299-111">Para obter os tamanhos mínimo e máximo solicitados do conjunto de trabalho para seu aplicativo, chame a [**função GetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="1a299-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="1a299-112">O sistema define os tamanhos padrão do conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a299-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="1a299-113">Você também pode modificar os tamanhos do conjunto de trabalho usando a [**função SetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="1a299-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="1a299-114">Definir esses valores não é uma garantia de que a memória será reservada ou residente.</span><span class="sxs-lookup"><span data-stu-id="1a299-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="1a299-115">Tenha cuidado ao solicitar um tamanho mínimo ou máximo de conjunto de trabalho muito grande, pois isso pode prejudicar o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="1a299-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="1a299-116">Para obter o tamanho atual ou de pico do conjunto de trabalho para seu processo, use a [**função GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)</span><span class="sxs-lookup"><span data-stu-id="1a299-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a299-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a299-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1a299-118">[Informações de desempenho de memória](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a299-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a299-119">Conjunto de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1a299-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
