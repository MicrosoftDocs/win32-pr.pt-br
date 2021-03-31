---
title: Matrizes fixas
description: Se a sua interface especifica uma matriz com um número específico de elementos como um parâmetro, ele está usando uma matriz fixa. Ao usar MIDL, você define matrizes fixas da mesma maneira que as define em C. Especifique o tipo, o nome e o tamanho da matriz.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636212"
---
# <a name="fixed-arrays"></a><span data-ttu-id="21e9f-104">Matrizes fixas</span><span class="sxs-lookup"><span data-stu-id="21e9f-104">Fixed Arrays</span></span>

<span data-ttu-id="21e9f-105">Se a sua interface especifica uma matriz com um número específico de elementos como um parâmetro, ele está usando uma matriz fixa.</span><span class="sxs-lookup"><span data-stu-id="21e9f-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="21e9f-106">Ao usar MIDL, você define matrizes fixas da mesma maneira que as define em C. Especifique o tipo, o nome e o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="21e9f-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="21e9f-107">O exemplo a seguir demonstra como definir uma matriz fixa.</span><span class="sxs-lookup"><span data-stu-id="21e9f-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="21e9f-108">Quando um programa cliente passa uma matriz fixa para um programa de servidor, o stub do cliente envia a matriz inteira para o stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="21e9f-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="21e9f-109">O stub do servidor aloca memória para a matriz e armazena os dados da matriz que recebe pela rede na memória alocada.</span><span class="sxs-lookup"><span data-stu-id="21e9f-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="21e9f-110">Em seguida, ele passa a matriz para o procedimento remoto no servidor.</span><span class="sxs-lookup"><span data-stu-id="21e9f-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="21e9f-111">O servidor pode modificar os dados na matriz.</span><span class="sxs-lookup"><span data-stu-id="21e9f-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="21e9f-112">Quando o procedimento remoto é encerrado, o stub do servidor envia o conteúdo da matriz de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="21e9f-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="21e9f-113">O stub do cliente copia os dados recebidos do stub do servidor na matriz original.</span><span class="sxs-lookup"><span data-stu-id="21e9f-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="21e9f-114">O programa cliente pode usar os dados como faria se eles recebissem os dados de uma chamada de procedimento local.</span><span class="sxs-lookup"><span data-stu-id="21e9f-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




