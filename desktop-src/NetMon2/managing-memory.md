---
description: Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gerenciando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921002"
---
# <a name="managing-memory"></a><span data-ttu-id="0aeee-103">Gerenciando memória</span><span class="sxs-lookup"><span data-stu-id="0aeee-103">Managing Memory</span></span>

<span data-ttu-id="0aeee-104">Caso um especialista falhe durante o tempo de execução, se você usar Monitor de Rede funções para gerenciamento de memória, Monitor de Rede liberará a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="0aeee-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="0aeee-105">No entanto, quando você escreve um especialista, pode ser necessário adquirir recursos do sistema e informações da estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="0aeee-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="0aeee-106">Por exemplo, o especialista de União de protocolo Monitor de Rede adquire um identificador de arquivo para criar uma nova captura.</span><span class="sxs-lookup"><span data-stu-id="0aeee-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="0aeee-107">Cada especialista deve criar seu próprio tratamento **try/catch** para que o especialista possa liberar recursos adquiridos.</span><span class="sxs-lookup"><span data-stu-id="0aeee-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="0aeee-108">Quando a memória for alocada, use as seguintes funções de memória existentes:</span><span class="sxs-lookup"><span data-stu-id="0aeee-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="0aeee-109">**ExpertAllocMemory**</span><span class="sxs-lookup"><span data-stu-id="0aeee-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="0aeee-110">**ExpertReallocMemory**</span><span class="sxs-lookup"><span data-stu-id="0aeee-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



