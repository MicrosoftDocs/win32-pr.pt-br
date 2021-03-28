---
description: Um aplicativo combina duas regiões chamando a função CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinando regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552818"
---
# <a name="combining-regions"></a><span data-ttu-id="57d3c-103">Combinando regiões</span><span class="sxs-lookup"><span data-stu-id="57d3c-103">Combining Regions</span></span>

<span data-ttu-id="57d3c-104">Um aplicativo combina duas regiões chamando a função [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .</span><span class="sxs-lookup"><span data-stu-id="57d3c-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="57d3c-105">Usando essa função, um aplicativo pode combinar partes de interseção de duas regiões, tudo exceto as partes interseccionadas de duas regiões, as duas regiões originais em sua totalidade e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="57d3c-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="57d3c-106">A seguir estão cinco valores que definem as combinações de regiões.</span><span class="sxs-lookup"><span data-stu-id="57d3c-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="57d3c-107">Valor</span><span class="sxs-lookup"><span data-stu-id="57d3c-107">Value</span></span>     | <span data-ttu-id="57d3c-108">Significado</span><span class="sxs-lookup"><span data-stu-id="57d3c-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57d3c-109">RGN \_ e</span><span class="sxs-lookup"><span data-stu-id="57d3c-109">RGN\_AND</span></span>  | <span data-ttu-id="57d3c-110">As partes de interseção de duas regiões originais definem uma nova região.</span><span class="sxs-lookup"><span data-stu-id="57d3c-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="57d3c-111">\_cópia RGN</span><span class="sxs-lookup"><span data-stu-id="57d3c-111">RGN\_COPY</span></span> | <span data-ttu-id="57d3c-112">Uma cópia da primeira (das duas regiões originais) define uma nova região.</span><span class="sxs-lookup"><span data-stu-id="57d3c-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="57d3c-113">RGN \_ diff</span><span class="sxs-lookup"><span data-stu-id="57d3c-113">RGN\_DIFF</span></span> | <span data-ttu-id="57d3c-114">A parte da primeira região que não faz interseção com a segunda define uma nova região.</span><span class="sxs-lookup"><span data-stu-id="57d3c-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="57d3c-115">RGN \_ ou</span><span class="sxs-lookup"><span data-stu-id="57d3c-115">RGN\_OR</span></span>   | <span data-ttu-id="57d3c-116">As duas regiões originais definem uma nova região.</span><span class="sxs-lookup"><span data-stu-id="57d3c-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="57d3c-117">\_XOR RGN</span><span class="sxs-lookup"><span data-stu-id="57d3c-117">RGN\_XOR</span></span>  | <span data-ttu-id="57d3c-118">Essas partes das duas regiões originais que não se sobrepõem definem uma nova região.</span><span class="sxs-lookup"><span data-stu-id="57d3c-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="57d3c-119">A ilustração a seguir mostra as cinco combinações possíveis de um quadrado e uma região circular resultante de uma chamada para [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span><span class="sxs-lookup"><span data-stu-id="57d3c-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![ilustração que demonstra os resultados descritos na tabela anterior](images/csrgn-02.png)

 

 



