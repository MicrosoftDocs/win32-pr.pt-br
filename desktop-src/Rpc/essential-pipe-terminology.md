---
title: Terminologia de pipe essencial
description: Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter parâmetros \ in \ ou \ out \.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499121"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="26aac-103">Terminologia de pipe essencial</span><span class="sxs-lookup"><span data-stu-id="26aac-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="26aac-104">Assim como outros tipos de parâmetros para chamadas de procedimento remotos, os pipes podem ter \[ parâmetros [**de entrada**](/windows/desktop/Midl/in) \] ou \[ [**saída**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="26aac-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="26aac-105">Como o servidor controla a transferência de dados por meio de um pipe, os pipes com o \[  \] atributo in são considerados para efetuar *pull* de dados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="26aac-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="26aac-106">Da mesma forma, os pipes de saída *enviam* dados do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="26aac-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="26aac-107">Os procedimentos que fazem a transferência de dados são chamados de *procedimento de pull* e de *Push*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="26aac-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="26aac-108">O compilador MIDL gera os procedimentos push e pull para o servidor.</span><span class="sxs-lookup"><span data-stu-id="26aac-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="26aac-109">Além disso, ele gerencia a alocação de buffers de dados na memória.</span><span class="sxs-lookup"><span data-stu-id="26aac-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="26aac-110">No entanto, o cliente deve fornecer seus próprios procedimentos de push e pull.</span><span class="sxs-lookup"><span data-stu-id="26aac-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="26aac-111">Ele também deve fornecer um procedimento para alocar os buffers de memória usados pelo pipe.</span><span class="sxs-lookup"><span data-stu-id="26aac-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="26aac-112">Eles são chamados automaticamente no momento apropriado pelo stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="26aac-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="26aac-113">O procedimento de alocação geralmente é chamado de procedimento de alocação ou função de alocação.</span><span class="sxs-lookup"><span data-stu-id="26aac-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 