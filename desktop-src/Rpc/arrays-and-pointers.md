---
title: Matrizes e ponteiros
description: A RPC (chamada de procedimento remoto) foi projetada para ser praticamente transparente para os desenvolvedores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Chamada de procedimento remoto RPC, descrito, matrizes e ponteiros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636180"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="e6398-104">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="e6398-104">Arrays and Pointers</span></span>

<span data-ttu-id="e6398-105">A RPC (chamada de procedimento remoto) foi projetada para ser praticamente transparente para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="e6398-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="e6398-106">Para obter essa transparência, o stub do cliente transmite para o servidor o ponteiro e o objeto de dados para o qual ele aponta.</span><span class="sxs-lookup"><span data-stu-id="e6398-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="e6398-107">Se o procedimento remoto alterar os dados, o servidor deverá transmitir os novos dados de volta para o cliente para que o cliente possa copiar os novos dados nos dados originais.</span><span class="sxs-lookup"><span data-stu-id="e6398-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="e6398-108">Em geral, uma chamada de procedimento remoto se comporta exatamente como uma chamada de procedimento local.</span><span class="sxs-lookup"><span data-stu-id="e6398-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="e6398-109">Ou seja, quando um ponteiro é um parâmetro, o procedimento remoto pode acessar o objeto de dados ao qual o ponteiro se refere da mesma maneira que um procedimento local pode.</span><span class="sxs-lookup"><span data-stu-id="e6398-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="e6398-110">Como os programas cliente e servidor são executados em espaços de endereço diferentes, os desenvolvedores devem usar os atributos linguagem IDL da Microsoft (MIDL) para descrever como os dados da matriz e do ponteiro são transmitidos entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e6398-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="e6398-111">Esta seção apresenta uma visão geral de como usar matrizes e ponteiros em aplicativos distribuídos, nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e6398-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="e6398-112">Matrizes e RPC</span><span class="sxs-lookup"><span data-stu-id="e6398-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="e6398-113">Ponteiros e RPC</span><span class="sxs-lookup"><span data-stu-id="e6398-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="e6398-114">Usando matrizes, cadeias de caracteres e ponteiros</span><span class="sxs-lookup"><span data-stu-id="e6398-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




