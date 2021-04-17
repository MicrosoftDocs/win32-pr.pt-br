---
description: Com o armazenamento local de threads (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global. Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Armazenamento local de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553826"
---
# <a name="thread-local-storage"></a><span data-ttu-id="0cea0-104">Armazenamento local de thread</span><span class="sxs-lookup"><span data-stu-id="0cea0-104">Thread Local Storage</span></span>

<span data-ttu-id="0cea0-105">Todos os threads de um processo compartilham seu espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="0cea0-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="0cea0-106">As variáveis locais de uma função são exclusivas para cada thread que executa a função.</span><span class="sxs-lookup"><span data-stu-id="0cea0-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="0cea0-107">No entanto, as variáveis estática e global são compartilhadas por todos os threads no processo.</span><span class="sxs-lookup"><span data-stu-id="0cea0-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="0cea0-108">Com o *armazenamento local de threads* (TLS), você pode fornecer dados exclusivos para cada thread que o processo pode acessar usando um índice global.</span><span class="sxs-lookup"><span data-stu-id="0cea0-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="0cea0-109">Um thread aloca o índice, que pode ser usado pelos outros threads para recuperar os dados exclusivos associados ao índice.</span><span class="sxs-lookup"><span data-stu-id="0cea0-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="0cea0-110">A constante de \_ mínimo \_ de TLS disponível define o número mínimo de índices TLS disponíveis em cada processo.</span><span class="sxs-lookup"><span data-stu-id="0cea0-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="0cea0-111">Esse mínimo é garantido como sendo pelo menos 64 para todos os sistemas.</span><span class="sxs-lookup"><span data-stu-id="0cea0-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="0cea0-112">O número máximo de índices por processo é de 1.088.</span><span class="sxs-lookup"><span data-stu-id="0cea0-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="0cea0-113">Quando os threads são criados, o sistema aloca uma matriz de valores **LPVOID** para TLS, que são inicializados como NULL.</span><span class="sxs-lookup"><span data-stu-id="0cea0-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="0cea0-114">Antes que um índice possa ser usado, ele deve ser alocado por um dos threads.</span><span class="sxs-lookup"><span data-stu-id="0cea0-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="0cea0-115">Cada thread armazena seus dados para um índice TLS em um *slot TLS* na matriz.</span><span class="sxs-lookup"><span data-stu-id="0cea0-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="0cea0-116">Se os dados associados a um índice couberem em um valor de **LPVOID** , você poderá armazenar os dados diretamente no slot TLS.</span><span class="sxs-lookup"><span data-stu-id="0cea0-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="0cea0-117">No entanto, se você estiver usando um grande número de índices dessa forma, é melhor alocar armazenamento separado, consolidar os dados e minimizar o número de Slots TLS em uso.</span><span class="sxs-lookup"><span data-stu-id="0cea0-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="0cea0-118">O diagrama a seguir ilustra como o TLS funciona.</span><span class="sxs-lookup"><span data-stu-id="0cea0-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="0cea0-119">Para obter um exemplo de código que ilustra o uso do armazenamento local de thread, consulte [usando o armazenamento local de thread](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="0cea0-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Diagrama que mostra como o processo do T L S funciona.](images/tls.png)

<span data-ttu-id="0cea0-121">O processo tem dois threads, thread 1 e thread 2.</span><span class="sxs-lookup"><span data-stu-id="0cea0-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="0cea0-122">Ele aloca dois índices para uso com TLS, gdwTlsIndex1 e gdwTlsIndex2.</span><span class="sxs-lookup"><span data-stu-id="0cea0-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="0cea0-123">Cada thread aloca dois blocos de memória (um para cada índice) para armazenar os dados e armazena os ponteiros para esses blocos de memória nos slots TLS correspondentes.</span><span class="sxs-lookup"><span data-stu-id="0cea0-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="0cea0-124">Para acessar os dados associados a um índice, o thread recupera o ponteiro para o bloco de memória do slot TLS e o armazena na variável local lpvData.</span><span class="sxs-lookup"><span data-stu-id="0cea0-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="0cea0-125">É ideal usar TLS em uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="0cea0-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="0cea0-126">Para obter um exemplo, consulte [usando o armazenamento local de thread em uma biblioteca de vínculo dinâmico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="0cea0-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cea0-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cea0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cea0-128">Armazenamento local de threads (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="0cea0-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="0cea0-129">Uso de armazenamento local de thread</span><span class="sxs-lookup"><span data-stu-id="0cea0-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="0cea0-130">Usando o armazenamento local de threads em uma biblioteca de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="0cea0-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
