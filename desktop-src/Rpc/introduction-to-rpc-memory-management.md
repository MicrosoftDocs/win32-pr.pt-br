---
title: Introdução ao gerenciamento de memória RPC
description: Introdução ao gerenciamento de memória RPC (chamada de procedimento remoto).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294369"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="e59f2-103">Introdução ao gerenciamento de memória RPC</span><span class="sxs-lookup"><span data-stu-id="e59f2-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="e59f2-104">No contexto de RPC, o gerenciamento de memória envolve:</span><span class="sxs-lookup"><span data-stu-id="e59f2-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="e59f2-105">Alocar e desalocar a memória necessária para simular um único espaço de endereço conceitual entre o cliente e o servidor nos espaços de endereço diferentes dos threads do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="e59f2-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="e59f2-106">Determinar qual componente de software é responsável por gerenciar a memória — o aplicativo ou o stub gerado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="e59f2-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="e59f2-107">Selecionando atributos de MIDL que afetam o gerenciamento de memória: atributos direcionais, atributos de ponteiro, atributos de matriz e os atributos de ACF \[ [ \_ contagem de bytes](/windows/desktop/Midl/byte-count) \] , \[ [alocação](/windows/desktop/Midl/allocate) \] e \[ [habilitação de \_ alocação](/windows/desktop/Midl/enable-allocate) \] .</span><span class="sxs-lookup"><span data-stu-id="e59f2-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="e59f2-108">Quando um programa chama uma função ou um procedimento em seu espaço de endereço, o gerenciamento de memória é mais direto do que em um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="e59f2-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="e59f2-109">Para ilustrar, o diagrama a seguir ilustra uma árvore binária.</span><span class="sxs-lookup"><span data-stu-id="e59f2-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="e59f2-110">Para passar essa estrutura de dados para um procedimento em seu espaço de endereço, um programa simplesmente passa um ponteiro para a raiz da árvore.</span><span class="sxs-lookup"><span data-stu-id="e59f2-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![uma árvore binária, com ponteiros para estruturar dados armazenados na raiz da árvore](images/bintree.png)

<span data-ttu-id="e59f2-112">Os aplicativos RPC cliente/servidor compartilham dados em dois espaços de memória diferentes.</span><span class="sxs-lookup"><span data-stu-id="e59f2-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="e59f2-113">Esses espaços de memória podem ou não estar no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="e59f2-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="e59f2-114">De qualquer forma, o cliente e o servidor não têm acesso direto ao espaço de memória uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="e59f2-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="e59f2-115">O RPC depende da capacidade de simular o espaço de endereço do programa cliente no espaço de endereço do programa do servidor.</span><span class="sxs-lookup"><span data-stu-id="e59f2-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="e59f2-116">Ele também deve retornar dados, incluindo dados novos e alterados, do servidor para a memória do cliente.</span><span class="sxs-lookup"><span data-stu-id="e59f2-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="e59f2-117">Em casos como a árvore binária representada no diagrama anterior, não é suficiente passar um ponteiro para o nó raiz para um procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e59f2-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="e59f2-118">O programa ou os stubs devem passar a árvore inteira para o espaço de endereço do servidor para que o procedimento remoto opere nele.</span><span class="sxs-lookup"><span data-stu-id="e59f2-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 