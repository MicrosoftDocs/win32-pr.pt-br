---
description: Define os números de ponto flutuante do efeito. Este modelo substitui o modelo EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009945"
---
# <a name="effectparamfloats"></a><span data-ttu-id="a5e19-104">EffectParamFloats</span><span class="sxs-lookup"><span data-stu-id="a5e19-104">EffectParamFloats</span></span>

<span data-ttu-id="a5e19-105">Define os números de ponto flutuante do efeito.</span><span class="sxs-lookup"><span data-stu-id="a5e19-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="a5e19-106">Este modelo substitui o modelo [**EffectFloats**](effectfloats.md) .</span><span class="sxs-lookup"><span data-stu-id="a5e19-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="a5e19-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="a5e19-107">Where:</span></span>

-   <span data-ttu-id="a5e19-108">ParamName-nome da matriz de floats.</span><span class="sxs-lookup"><span data-stu-id="a5e19-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="a5e19-109">nFloats-número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="a5e19-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="a5e19-110">Flutua \[ nFloats \] -matriz de valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a5e19-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e19-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5e19-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e19-112">Modelos</span><span class="sxs-lookup"><span data-stu-id="a5e19-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



