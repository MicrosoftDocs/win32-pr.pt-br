---
title: " Protótipo de entrada, saída size_is"
description: '\ in, out, Size \_ is \ Prototype usa uma matriz de caracteres de conta única que é passada do cliente para o servidor e do servidor para o cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294139"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="3111b-103">\[in, out, o tamanho \_ é \] protótipo</span><span class="sxs-lookup"><span data-stu-id="3111b-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="3111b-104">O protótipo de função a seguir usa uma matriz de caracteres de conta única que é passada de ambas as maneiras: do cliente para o servidor e do servidor para o cliente:</span><span class="sxs-lookup"><span data-stu-id="3111b-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="3111b-105">Como um \[ parâmetro [**in**](/windows/desktop/Midl/in) \] , *achInOut* deve apontar para um armazenamento válido no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3111b-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="3111b-106">O desenvolvedor aloca memória associada à matriz no lado do cliente antes de fazer a chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3111b-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="3111b-107">Os stubs usam \[ [**o \_**](/windows/desktop/Midl/size-is) \] parâmetro *strsize* para alocar memória no servidor e, em seguida, usar o \[ [**comprimento \_ é**](/windows/desktop/Midl/length-is) o \] parâmetro *pcbSize* para transmitir os elementos da matriz para essa memória.</span><span class="sxs-lookup"><span data-stu-id="3111b-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="3111b-108">O desenvolvedor deve garantir que o código do cliente defina o **\[ comprimento \_ \]** como variável antes de chamar o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3111b-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="3111b-109">Em algumas situações, o uso de parâmetros separados em vez de uma única cadeia de caracteres para a entrada e saída é mais eficiente e fornece flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="3111b-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="3111b-110">Isso é demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="3111b-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="3111b-111">No exemplo anterior, a matriz de caracteres achInOut também é usada como um \[ parâmetro [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="3111b-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="3111b-112">Em C, o nome da matriz é equivalente ao uso de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3111b-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="3111b-113">Por padrão, todos os ponteiros de nível superior são ponteiros de referência — eles não são alterados em valor e apontam para a mesma área de memória no cliente antes e depois da chamada.</span><span class="sxs-lookup"><span data-stu-id="3111b-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="3111b-114">Toda a memória que o procedimento remoto acessa deve se ajustar ao tamanho que o cliente especifica antes da chamada, ou os stubs gerarão uma exceção.</span><span class="sxs-lookup"><span data-stu-id="3111b-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="3111b-115">Antes de retornar, a função Analyze no servidor deve redefinir o parâmetro *pcbSize* para indicar o número de elementos que o servidor transmitirá para o cliente, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="3111b-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 