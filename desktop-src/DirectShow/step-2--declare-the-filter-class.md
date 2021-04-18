---
description: Etapa 2.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Etapa 2. Declarar a classe de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757671"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="74f30-104">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="74f30-104">Step 2.</span></span> <span data-ttu-id="74f30-105">Declarar a classe de filtro</span><span class="sxs-lookup"><span data-stu-id="74f30-105">Declare the Filter Class</span></span>

<span data-ttu-id="74f30-106">Esta é a etapa 2 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="74f30-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="74f30-107">Comece declarando uma classe C++ que herda a classe base:</span><span class="sxs-lookup"><span data-stu-id="74f30-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="74f30-108">Cada uma das classes de filtro tem classes de PIN associadas.</span><span class="sxs-lookup"><span data-stu-id="74f30-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="74f30-109">Dependendo das necessidades específicas do filtro, talvez seja necessário substituir as classes de PIN.</span><span class="sxs-lookup"><span data-stu-id="74f30-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="74f30-110">No caso do **CTransformFilter**, os Pins delegam a maior parte de seu trabalho para o filtro, de modo que você provavelmente não precisa substituir os Pins.</span><span class="sxs-lookup"><span data-stu-id="74f30-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="74f30-111">Você deve gerar um CLSID exclusivo para o filtro.</span><span class="sxs-lookup"><span data-stu-id="74f30-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="74f30-112">Você pode usar o utilitário GUIDGEN ou uuidgen; Nunca Copie um GUID existente.</span><span class="sxs-lookup"><span data-stu-id="74f30-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="74f30-113">Há várias maneiras de declarar um CLSID.</span><span class="sxs-lookup"><span data-stu-id="74f30-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="74f30-114">O exemplo a seguir usa a macro **definir \_ GUID** :</span><span class="sxs-lookup"><span data-stu-id="74f30-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="74f30-115">Em seguida, escreva um método de construtor para o filtro:</span><span class="sxs-lookup"><span data-stu-id="74f30-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="74f30-116">Observe que um dos parâmetros para o construtor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) é o CLSID definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="74f30-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="74f30-117">Em seguida: [etapa 3. Suporte à negociação de tipo de mídia](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="74f30-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74f30-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74f30-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f30-119">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="74f30-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



