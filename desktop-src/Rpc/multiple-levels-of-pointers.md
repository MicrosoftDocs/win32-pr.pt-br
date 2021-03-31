---
title: Vários níveis de ponteiros
description: Usando vários níveis de ponteiros na RPC (chamada de procedimento remoto).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917521"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="4f109-103">Vários níveis de ponteiros</span><span class="sxs-lookup"><span data-stu-id="4f109-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="4f109-104">Quando há vários níveis de ponteiros, os atributos são associados ao ponteiro mais próximo do nome da variável.</span><span class="sxs-lookup"><span data-stu-id="4f109-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="4f109-105">O cliente ainda é responsável por alocar qualquer memória associada à resposta.</span><span class="sxs-lookup"><span data-stu-id="4f109-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="4f109-106">O exemplo a seguir permite que o stub chame o servidor sem saber antecipadamente a quantidade de dados que será retornada:</span><span class="sxs-lookup"><span data-stu-id="4f109-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="4f109-107">Neste exemplo, o stub passa o servidor para um ponteiro exclusivo, que o servidor inicializa como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4f109-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="4f109-108">Em seguida, o servidor aloca um bloco de barras, define o ponteiro, define o argumento de tamanho e retorna.</span><span class="sxs-lookup"><span data-stu-id="4f109-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="4f109-109">Observe que, para que o servidor tenha um efeito no chamador, você deve passar um \[ ponteiro de referência \] para um \[ ponteiro [**exclusivo**](/windows/desktop/Midl/unique) \] para seus dados.</span><span class="sxs-lookup"><span data-stu-id="4f109-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="4f109-110">Observe também que a vírgula em \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is)(, \* psize) \] , que indica que o ponteiro de nível superior não é um ponteiro de tamanho, mas que o ponteiro de nível inferior é.</span><span class="sxs-lookup"><span data-stu-id="4f109-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="4f109-111">No lado do cliente, o stub define \* ppBar como **nulo** antes de chamar o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4f109-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="4f109-112">Em seguida, o stub aloca e desempacota a conjunto de objetos de barra.</span><span class="sxs-lookup"><span data-stu-id="4f109-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="4f109-113">O argumento size indica o tamanho do bloco (e o número de barras não marshaled).</span><span class="sxs-lookup"><span data-stu-id="4f109-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="4f109-114">O cliente deve liberar a matriz retornada de objetos de barra quando ela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="4f109-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f109-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f109-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f109-116">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="4f109-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 