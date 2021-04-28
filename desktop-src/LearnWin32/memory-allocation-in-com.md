---
title: Alocação de memória em COM
description: Alocação de memória em COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103884"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="8b3a1-103">Alocação de memória em COM</span><span class="sxs-lookup"><span data-stu-id="8b3a1-103">Memory Allocation in COM</span></span>

<span data-ttu-id="8b3a1-104">Às vezes, um método aloca um buffer de memória no heap e retorna o endereço do buffer para o chamador.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="8b3a1-105">COM define um par de funções para alocar e liberar memória no heap.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="8b3a1-106">A função [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) aloca um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="8b3a1-107">A função [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera um bloco de memória que foi alocado com [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="8b3a1-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="8b3a1-108">Vimos um exemplo desse padrão no [exemplo de caixa de diálogo abrir](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="8b3a1-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="8b3a1-109">O método [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) aloca memória para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="8b3a1-110">Internamente, o método chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="8b3a1-111">Quando o método retorna, *pszFilePath* aponta para o local da memória do novo buffer.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="8b3a1-112">O chamador é responsável por chamar [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="8b3a1-113">Por que o COM define suas próprias funções de alocação de memória?</span><span class="sxs-lookup"><span data-stu-id="8b3a1-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="8b3a1-114">Um motivo é fornecer uma camada de abstração sobre o alocador de heap.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="8b3a1-115">Caso contrário, alguns métodos poderão chamar **malloc** enquanto outros chamarem **New**.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="8b3a1-116">Em seguida, seu programa precisaria chamar **gratuitamente** em alguns casos e **excluir** em outros, e manter o controle da ti tudo rapidamente se tornaria impossível.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="8b3a1-117">As funções de alocação COM criam uma abordagem uniforme.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="8b3a1-118">Outra consideração é o fato de que COM é um padrão *binário* , portanto, ele não está vinculado a uma linguagem de programação específica.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="8b3a1-119">Portanto, o COM não pode contar com qualquer forma específica de linguagem de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="8b3a1-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="8b3a1-120">Avançar</span><span class="sxs-lookup"><span data-stu-id="8b3a1-120">Next</span></span>

[<span data-ttu-id="8b3a1-121">Práticas de codificação COM</span><span class="sxs-lookup"><span data-stu-id="8b3a1-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
