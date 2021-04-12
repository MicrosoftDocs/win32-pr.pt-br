---
title: Escolhendo o modelo de Threading
description: Escolhendo o modelo de Threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364399"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="24bd5-103">Escolhendo o modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="24bd5-103">Choosing the Threading Model</span></span>

<span data-ttu-id="24bd5-104">Escolher o modelo de threading para um objeto depende da função do objeto.</span><span class="sxs-lookup"><span data-stu-id="24bd5-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="24bd5-105">Um objeto que executa e/s extensiva pode dar suporte a Threading livre para fornecer o máximo de resposta aos clientes, permitindo chamadas de interface durante a latência de e/s.</span><span class="sxs-lookup"><span data-stu-id="24bd5-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="24bd5-106">Por outro lado, um objeto que interage com o usuário pode dar suporte ao Threading Apartment para sincronizar chamadas COM de entrada com suas operações de janela.</span><span class="sxs-lookup"><span data-stu-id="24bd5-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="24bd5-107">É mais fácil oferecer suporte a Threading de apartamento em Apartments de thread único porque o COM fornece sincronização em uma base por chamada.</span><span class="sxs-lookup"><span data-stu-id="24bd5-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="24bd5-108">O suporte ao Threading livre é mais difícil porque o objeto deve implementar a sincronização; no entanto, a resposta aos clientes pode ser melhor porque a sincronização pode ser implementada para seções menores de código.</span><span class="sxs-lookup"><span data-stu-id="24bd5-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24bd5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24bd5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24bd5-110">Acessando interfaces em Apartments</span><span class="sxs-lookup"><span data-stu-id="24bd5-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="24bd5-111">Apartments multithread</span><span class="sxs-lookup"><span data-stu-id="24bd5-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="24bd5-112">Problemas de Threading do servidor em processo</span><span class="sxs-lookup"><span data-stu-id="24bd5-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="24bd5-113">Processos, threads e Apartments</span><span class="sxs-lookup"><span data-stu-id="24bd5-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="24bd5-114">Comunicação de thread único e multithread</span><span class="sxs-lookup"><span data-stu-id="24bd5-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="24bd5-115">Apartments de thread único</span><span class="sxs-lookup"><span data-stu-id="24bd5-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




