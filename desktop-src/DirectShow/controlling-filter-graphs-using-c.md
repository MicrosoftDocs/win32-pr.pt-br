---
description: Controlando gráficos de filtro usando C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlando gráficos de filtro usando C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370251"
---
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="4b57a-103">Controlando gráficos de filtro usando C</span><span class="sxs-lookup"><span data-stu-id="4b57a-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="4b57a-104">Se você estiver escrevendo um aplicativo DirectShow em C (em vez de C++), deverá usar um ponteiro vtable para chamar métodos.</span><span class="sxs-lookup"><span data-stu-id="4b57a-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="4b57a-105">O exemplo a seguir ilustra como chamar o método **IUnknown:: QueryInterface** de um aplicativo escrito em C:</span><span class="sxs-lookup"><span data-stu-id="4b57a-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="4b57a-106">O seguinte mostra a chamada equivalente em C++:</span><span class="sxs-lookup"><span data-stu-id="4b57a-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="4b57a-107">Em C, as interfaces COM são definidas como estruturas.</span><span class="sxs-lookup"><span data-stu-id="4b57a-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="4b57a-108">O membro **lpVtbl** é um ponteiro para uma tabela de métodos de interface (a vtable).</span><span class="sxs-lookup"><span data-stu-id="4b57a-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="4b57a-109">Todos os métodos usam um parâmetro adicional, que é um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="4b57a-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b57a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b57a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b57a-111">Apêndices</span><span class="sxs-lookup"><span data-stu-id="4b57a-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



