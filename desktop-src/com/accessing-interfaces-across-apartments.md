---
title: Acessando interfaces em Apartments
description: Acessando interfaces em Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635488"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="6730e-103">Acessando interfaces em Apartments</span><span class="sxs-lookup"><span data-stu-id="6730e-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="6730e-104">COM fornece uma maneira para qualquer Apartment em um processo obter acesso a uma interface implementada em um objeto em qualquer outro apartamento no processo.</span><span class="sxs-lookup"><span data-stu-id="6730e-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="6730e-105">Isso é feito por meio da interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="6730e-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="6730e-106">Essa interface tem três métodos, que permitem que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6730e-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="6730e-107">Registrar uma interface como uma interface *global* (processwide).</span><span class="sxs-lookup"><span data-stu-id="6730e-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="6730e-108">Obtenha um ponteiro para essa interface de qualquer outro apartamento por meio de um cookie.</span><span class="sxs-lookup"><span data-stu-id="6730e-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="6730e-109">Revogue o registro global de uma interface.</span><span class="sxs-lookup"><span data-stu-id="6730e-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="6730e-110">A interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) é uma maneira eficiente para um processo armazenar um ponteiro de interface em um local de memória que pode ser acessado de vários Apartments dentro do processo, como variáveis de todo o processo e objetos *Agile* (objetos de thread livre, empacotados) que contêm ponteiros de interface para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="6730e-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="6730e-111">Um objeto ágil não reconhece a infraestrutura COM subjacente na qual ele é executado; em outras palavras, o apartamento, o contexto e o thread em que ele está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="6730e-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="6730e-112">O objeto pode estar mantendo as interfaces específicas para um apartamento ou contexto.</span><span class="sxs-lookup"><span data-stu-id="6730e-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="6730e-113">Por esse motivo, chamar essas interfaces a partir de onde o componente Agile está em execução pode nem sempre funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="6730e-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="6730e-114">A tabela de interface global evita esse problema garantindo que um proxy válido (ou ponteiro direto) para o objeto seja usado, com base em onde o objeto Agile está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="6730e-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="6730e-115">A tabela de interface global não é portátil entre os limites do processo ou da máquina, portanto, não pode ser usada no lugar do mecanismo de passagem de parâmetro normal.</span><span class="sxs-lookup"><span data-stu-id="6730e-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="6730e-116">Para obter informações sobre como criar e usar uma tabela de interface global, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6730e-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="6730e-117">Criando a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="6730e-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="6730e-118">Quando usar a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="6730e-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="6730e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6730e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6730e-120">Escolhendo o modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="6730e-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="6730e-121">Apartments multithread</span><span class="sxs-lookup"><span data-stu-id="6730e-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="6730e-122">Problemas de Threading do servidor em processo</span><span class="sxs-lookup"><span data-stu-id="6730e-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="6730e-123">Processos, threads e Apartments</span><span class="sxs-lookup"><span data-stu-id="6730e-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="6730e-124">Comunicação de thread único e multithread</span><span class="sxs-lookup"><span data-stu-id="6730e-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="6730e-125">Apartments de thread único</span><span class="sxs-lookup"><span data-stu-id="6730e-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




