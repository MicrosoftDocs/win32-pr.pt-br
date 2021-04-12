---
title: Alocação e desalocação de nó por nó
description: A alocação de nó por nó e a desalocação de estruturas de dados pelos stubs são o método padrão de gerenciamento de memória para todos os parâmetros no cliente e no servidor.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454195"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="948e7-103">Alocação e desalocação de nó por nó</span><span class="sxs-lookup"><span data-stu-id="948e7-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="948e7-104">A alocação de nó por nó e a desalocação de estruturas de dados pelos stubs são o método padrão de gerenciamento de memória para todos os parâmetros no cliente e no servidor.</span><span class="sxs-lookup"><span data-stu-id="948e7-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="948e7-105">No lado do cliente, o stub aloca cada nó com uma chamada separada para a [alocação de \_ usuário \_ de MIDL](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="948e7-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="948e7-106">No lado do servidor, em vez de chamar o **usuário de MIDL \_ \_**, a memória privada é usada sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="948e7-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="948e7-107">Se **a \_ \_ alocação de usuário MIDL** for chamada, os stubs de servidor chamarão o **\_ usuário MIDL \_ gratuitamente** para liberar os dados.</span><span class="sxs-lookup"><span data-stu-id="948e7-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="948e7-108">Na maioria dos casos, usar alocação de nó por nó e desalocação em vez de usar **\[ ALLOCATE (todos os \_ nós) \]** resultará em um aumento no desempenho dos stubs do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="948e7-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 