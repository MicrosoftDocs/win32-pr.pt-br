---
description: Declare uma classe C++ que herda a classe base que você escolheu como parte da escrita de um filtro de transformação.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Etapa 2. Declarar a classe Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410059"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="4a309-104">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="4a309-104">Step 2.</span></span> <span data-ttu-id="4a309-105">Declarar a classe Filter</span><span class="sxs-lookup"><span data-stu-id="4a309-105">Declare the Filter Class</span></span>

<span data-ttu-id="4a309-106">Esta é a etapa 2 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="4a309-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="4a309-107">Comece declarando uma classe C++ que herda a classe base:</span><span class="sxs-lookup"><span data-stu-id="4a309-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="4a309-108">Cada uma das classes de filtro tem classes de pino associadas.</span><span class="sxs-lookup"><span data-stu-id="4a309-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="4a309-109">Dependendo das necessidades específicas do filtro, talvez seja necessário substituir as classes de pino.</span><span class="sxs-lookup"><span data-stu-id="4a309-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="4a309-110">No caso de **CTransformFilter**, os pinos delegam a maior parte de seu trabalho ao filtro, portanto, você provavelmente não precisa substituir os pinos.</span><span class="sxs-lookup"><span data-stu-id="4a309-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="4a309-111">Você deve gerar um CLSID exclusivo para o filtro.</span><span class="sxs-lookup"><span data-stu-id="4a309-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="4a309-112">Você pode usar o utilitário Guidgen ou Uuidgen; nunca copie um GUID existente.</span><span class="sxs-lookup"><span data-stu-id="4a309-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="4a309-113">Há várias maneiras de declarar um CLSID.</span><span class="sxs-lookup"><span data-stu-id="4a309-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="4a309-114">O exemplo a seguir usa a **macro \_ DEFINE GUID:**</span><span class="sxs-lookup"><span data-stu-id="4a309-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="4a309-115">Em seguida, escreva um método de construtor para o filtro:</span><span class="sxs-lookup"><span data-stu-id="4a309-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="4a309-116">Observe que um dos parâmetros para o construtor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) é o CLSID definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4a309-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="4a309-117">Próximo: [Etapa 3. Suporte à negociação de tipo de mídia](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="4a309-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a309-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a309-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a309-119">Escrevendo filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4a309-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



