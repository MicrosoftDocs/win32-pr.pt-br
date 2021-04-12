---
title: Gerenciando a alocação de memória
description: Gerenciando a alocação de memória
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366787"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="4c4f8-103">Gerenciando a alocação de memória</span><span class="sxs-lookup"><span data-stu-id="4c4f8-103">Managing Memory Allocation</span></span>

<span data-ttu-id="4c4f8-104">No COM, muitos, se não a maioria, os métodos de interface são chamados pelo código escrito por uma organização de programação e implementados pelo código escrito por outro.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="4c4f8-105">Muitos dos parâmetros e valores de retorno dessas funções são de tipos que podem ser transmitidos por valor.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="4c4f8-106">Às vezes, no entanto, é necessário passar estruturas de dados para as quais esse não é o caso, portanto, é necessário para o chamador e chamado ter uma política de alocação e desalocação compatível.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="4c4f8-107">COM define uma convenção universal para alocação de memória, porque ela é mais razoável do que definir regras de caso por caso e para que a implementação de chamada de procedimento remoto COM possa gerenciar corretamente a memória.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="4c4f8-108">Os métodos de uma interface COM sempre fornecem gerenciamento de memória de ponteiros para a interface chamando as funções [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) encontradas na interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , da qual todas as outras interfaces com derivam.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="4c4f8-109">(Consulte [regras para gerenciar contagens de referência](rules-for-managing-reference-counts.md) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="4c4f8-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="4c4f8-110">Esta seção descreve apenas como alocar memória para parâmetros que não são passados por valor — não ponteiros para interfaces, mas coisas mais comunss, como cadeias de caracteres, ponteiros para estruturas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="4c4f8-111">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="4c4f8-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4c4f8-112">O alocador de memória OLE</span><span class="sxs-lookup"><span data-stu-id="4c4f8-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="4c4f8-113">Regras de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="4c4f8-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="4c4f8-114">Depurando alocações de memória</span><span class="sxs-lookup"><span data-stu-id="4c4f8-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 