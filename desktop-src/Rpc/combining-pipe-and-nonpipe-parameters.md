---
title: Combinando parâmetros de pipe e nonpipe
description: Combinando parâmetros de pipe e nonpipe na chamada de procedimento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823914"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="46b10-103">Combinando parâmetros de pipe e nonpipe</span><span class="sxs-lookup"><span data-stu-id="46b10-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="46b10-104">Quando você combina tipos de pipe e outros tipos em uma chamada de procedimento remoto, os dados são transmitidos de acordo com a direção do parâmetro:</span><span class="sxs-lookup"><span data-stu-id="46b10-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="46b10-105">Na direção **\[ in \]** , os dados de todos os argumentos de não-pipe são transmitidos primeiro, seguidos por dados de pipe.</span><span class="sxs-lookup"><span data-stu-id="46b10-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="46b10-106">Na direção de **\[ saída \]** , o servidor envia os dados do pipe primeiro.</span><span class="sxs-lookup"><span data-stu-id="46b10-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="46b10-107">Depois que a rotina Manager é retornada, o servidor transmite os dados sem pipe.</span><span class="sxs-lookup"><span data-stu-id="46b10-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="46b10-108">Quando há argumentos **\[ de pipe in \] , out** combinados com argumentos **\[ in, \] out** non-pipe, primeiro os dados de entrada são transmitidos em sua totalidade, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="46b10-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="46b10-109">Em seguida, os dados de saída são transmitidos conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="46b10-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="46b10-110">A seguinte restrição se aplica a esta implementação de Pipes (MIDL 3,0): quando você combina tipos de pipe e outros tipos em uma única chamada de procedimento remoto, os parâmetros de não-pipe devem ter um tamanho bem definido para permitir que o compilador MIDL Calcule o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="46b10-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="46b10-111">Por exemplo, você não pode combinar parâmetros de pipe com um \[ [](/windows/desktop/Midl/unique) \] ponteiro exclusivo ou uma estrutura compatível, já que seus tamanhos não podem ser determinados no tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="46b10-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46b10-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46b10-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46b10-113">pipe</span><span class="sxs-lookup"><span data-stu-id="46b10-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="46b10-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="46b10-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 