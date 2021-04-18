---
description: Define um conjunto de dois valores Boolianos usados no modelo MeshFaceWraps para definir a topologia de textura de uma face individual. Use em vez de Boolean2d quando as coordenadas de textura (u, v) abrangem o intervalo de 0 a 2 em vez de 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105815515"
---
# <a name="materialwrap"></a><span data-ttu-id="93552-104">MaterialWrap</span><span class="sxs-lookup"><span data-stu-id="93552-104">MaterialWrap</span></span>

<span data-ttu-id="93552-105">Define um conjunto de dois valores Boolianos usados no modelo [**MeshFaceWraps**](meshfacewraps.md) para definir a topologia de textura de uma face individual.</span><span class="sxs-lookup"><span data-stu-id="93552-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="93552-106">Use em vez de [**Boolean2d**](boolean2d.md) quando as coordenadas de textura (u, v) abrangem o intervalo de 0 a 2 em vez de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="93552-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="93552-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="93552-107">Where:</span></span>

-   <span data-ttu-id="93552-108">valor u-booliano.</span><span class="sxs-lookup"><span data-stu-id="93552-108">u - Boolean value.</span></span> <span data-ttu-id="93552-109">Consulte [**booliano**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="93552-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="93552-110">valor de v-booliano.</span><span class="sxs-lookup"><span data-stu-id="93552-110">v - Boolean value.</span></span> <span data-ttu-id="93552-111">Consulte [**booliano**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="93552-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="93552-112">O modelo [**MeshFaceWraps**](meshfacewraps.md) não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="93552-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="93552-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="93552-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93552-114">Modelos</span><span class="sxs-lookup"><span data-stu-id="93552-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



