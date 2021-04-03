---
title: O alocador de memória OLE
description: O alocador de memória OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084922"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="c8464-103">O alocador de memória OLE</span><span class="sxs-lookup"><span data-stu-id="c8464-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="c8464-104">A biblioteca COM fornece uma implementação de um alocador de memória que é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c8464-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="c8464-105">(Ou seja, isso não pode causar problemas em situações multi-threaded). Sempre que a propriedade de um bloco alocado de memória é passada por meio de uma interface COM ou entre um cliente e a biblioteca COM, você deve usar esse alocador de COM para alocar a memória.</span><span class="sxs-lookup"><span data-stu-id="c8464-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="c8464-106">A alocação interna a um objeto pode usar qualquer esquema de alocação desejado, mas o alocador de memória COM é um alocador útil, eficiente e seguro para thread.</span><span class="sxs-lookup"><span data-stu-id="c8464-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="c8464-107">Uma chamada para a função de API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fornece um ponteiro para o alocador OLE, que é uma implementação da interface [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="c8464-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="c8464-108">No entanto, é mais eficiente chamar as funções auxiliares [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)e [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), que encapsulam a obtenção de um ponteiro para o alocador de memória da tarefa, chamando o método **IMalloc** correspondente e, em seguida, liberando o ponteiro para o alocador.</span><span class="sxs-lookup"><span data-stu-id="c8464-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8464-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8464-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8464-110">Gerenciando a alocação de memória</span><span class="sxs-lookup"><span data-stu-id="c8464-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="c8464-111">A biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="c8464-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 