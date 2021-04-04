---
title: Ponteiros e RPC
description: É muito eficiente usar ponteiros como parâmetros de função C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822878"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="dcabd-103">Ponteiros e RPC</span><span class="sxs-lookup"><span data-stu-id="dcabd-103">Pointers and RPC</span></span>

<span data-ttu-id="dcabd-104">É muito eficiente usar ponteiros como parâmetros de função C.</span><span class="sxs-lookup"><span data-stu-id="dcabd-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="dcabd-105">O ponteiro custa apenas alguns bytes e pode ser usado para acessar uma grande quantidade de memória.</span><span class="sxs-lookup"><span data-stu-id="dcabd-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="dcabd-106">No entanto, em um aplicativo distribuído, os procedimentos de cliente e servidor residem em espaços de endereço diferentes — eles podem estar em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="dcabd-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="dcabd-107">Portanto, o cliente e o servidor normalmente não têm acesso ao mesmo espaço de memória.</span><span class="sxs-lookup"><span data-stu-id="dcabd-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="dcabd-108">Quando um dos parâmetros do procedimento remoto é um ponteiro para um objeto, o cliente deve transmitir uma cópia desse objeto e seu ponteiro para o servidor.</span><span class="sxs-lookup"><span data-stu-id="dcabd-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="dcabd-109">Se o procedimento remoto modificar o objeto por meio de seu ponteiro, o servidor retornará o ponteiro e sua cópia modificada.</span><span class="sxs-lookup"><span data-stu-id="dcabd-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="dcabd-110">O MIDL oferece atributos de ponteiro para minimizar a quantidade de sobrecarga necessária e o tamanho do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcabd-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="dcabd-111">Esta seção aborda a finalidade e os usos dos atributos de ponteiro de MIDL.</span><span class="sxs-lookup"><span data-stu-id="dcabd-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="dcabd-112">Ele também apresenta informações sobre manipulação de ponteiros em aplicativos RPC.</span><span class="sxs-lookup"><span data-stu-id="dcabd-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="dcabd-113">Ele é dividido nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="dcabd-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="dcabd-114">Tipos de ponteiros</span><span class="sxs-lookup"><span data-stu-id="dcabd-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="dcabd-115">Ponteiros e alocação de memória</span><span class="sxs-lookup"><span data-stu-id="dcabd-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="dcabd-116">Tipos de ponteiro padrão</span><span class="sxs-lookup"><span data-stu-id="dcabd-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="dcabd-117">Herança de tipo de atributo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="dcabd-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




