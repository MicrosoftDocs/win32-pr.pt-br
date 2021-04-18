---
title: Alocação de memória em COM
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105761973"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="d877e-103">Alocação de memória em COM</span><span class="sxs-lookup"><span data-stu-id="d877e-103">Memory Allocation in COM</span></span>

<span data-ttu-id="d877e-104">Às vezes, um método aloca um buffer de memória no heap e retorna o endereço do buffer para o chamador.</span><span class="sxs-lookup"><span data-stu-id="d877e-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="d877e-105">COM define um par de funções para alocar e liberar memória no heap.</span><span class="sxs-lookup"><span data-stu-id="d877e-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="d877e-106">A função [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) aloca um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="d877e-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="d877e-107">A função [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera um bloco de memória que foi alocado com [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="d877e-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="d877e-108">Vimos um exemplo desse padrão no [exemplo de caixa de diálogo abrir](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="d877e-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="d877e-109">O método [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) aloca memória para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d877e-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="d877e-110">Internamente, o método chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d877e-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="d877e-111">Quando o método retorna, *pszFilePath* aponta para o local da memória do novo buffer.</span><span class="sxs-lookup"><span data-stu-id="d877e-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="d877e-112">O chamador é responsável por chamar [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="d877e-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="d877e-113">Por que o COM define suas próprias funções de alocação de memória?</span><span class="sxs-lookup"><span data-stu-id="d877e-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="d877e-114">Um motivo é fornecer uma camada de abstração sobre o alocador de heap.</span><span class="sxs-lookup"><span data-stu-id="d877e-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="d877e-115">Caso contrário, alguns métodos poderão chamar **malloc** enquanto outros chamarem **New**.</span><span class="sxs-lookup"><span data-stu-id="d877e-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="d877e-116">Em seguida, seu programa precisaria chamar **gratuitamente** em alguns casos e **excluir** em outros, e manter o controle da ti tudo rapidamente se tornaria impossível.</span><span class="sxs-lookup"><span data-stu-id="d877e-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="d877e-117">As funções de alocação COM criam uma abordagem uniforme.</span><span class="sxs-lookup"><span data-stu-id="d877e-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="d877e-118">Outra consideração é o fato de que COM é um padrão *binário* , portanto, ele não está vinculado a uma linguagem de programação específica.</span><span class="sxs-lookup"><span data-stu-id="d877e-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="d877e-119">Portanto, o COM não pode contar com qualquer forma específica de linguagem de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="d877e-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="d877e-120">Avançar</span><span class="sxs-lookup"><span data-stu-id="d877e-120">Next</span></span>

[<span data-ttu-id="d877e-121">Práticas de codificação COM</span><span class="sxs-lookup"><span data-stu-id="d877e-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 