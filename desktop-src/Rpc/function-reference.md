---
title: Referência de função
description: Esta seção documenta as funções de tempo de execução do RPC (chamada de procedimento remoto) com suporte no Microsoft RPC.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453615"
---
# <a name="function-reference"></a><span data-ttu-id="dfed7-103">Referência de função</span><span class="sxs-lookup"><span data-stu-id="dfed7-103">Function Reference</span></span>

<span data-ttu-id="dfed7-104">Esta seção documenta as funções de tempo de execução do RPC (chamada de procedimento remoto) com suporte no Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="dfed7-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="dfed7-105">Esta seção descreve a finalidade de cada função, a sintaxe, os parâmetros de entrada e os valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="dfed7-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="dfed7-106">Ele também fornece informações adicionais para ajudá-lo a usar as funções RPC em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfed7-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="dfed7-107">Todos os ponteiros passados para as funções RPC devem incluir o atributo **\_ \_ \_ distante do RPC** .</span><span class="sxs-lookup"><span data-stu-id="dfed7-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="dfed7-108">Por exemplo, o **\_ \_ identificador \* de ligação RPC** do ponteiro torna-se uma **\_ Associação \_ \_ \_ \_ \* RPC para** cima e o **caractere \* \*** *PTR* torna-se um **caractere \_ \_ \_ \* \_ \_ \_ \*** RPC na extremidade do RPC.</span><span class="sxs-lookup"><span data-stu-id="dfed7-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="dfed7-109">Esta seção apresenta as referências de função nos seguintes grupos:</span><span class="sxs-lookup"><span data-stu-id="dfed7-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="dfed7-110">Funções RPC</span><span class="sxs-lookup"><span data-stu-id="dfed7-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="dfed7-111">Retorno de chamada RPC e funções de notificação</span><span class="sxs-lookup"><span data-stu-id="dfed7-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




