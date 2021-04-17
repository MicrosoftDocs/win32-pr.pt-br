---
description: Retorna o valor passado como o parâmetro HitKind para ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749523"
---
# <a name="hitkind"></a><span data-ttu-id="519ac-103">HitKind</span><span class="sxs-lookup"><span data-stu-id="519ac-103">HitKind</span></span>

<span data-ttu-id="519ac-104">Retorna o valor passado como o parâmetro **HitKind** para [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="519ac-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="519ac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="519ac-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="519ac-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="519ac-106">Remarks</span></span>

<span data-ttu-id="519ac-107">Se a interseção foi relatada pela interseção de triângulo de função fixa, **HitKind** será um dos tipos de toque na **\_ \_ \_ \_ face frontal** (254) ou no tipo de botão de **\_ \_ fundo de triângulo \_ \_** (255).</span><span class="sxs-lookup"><span data-stu-id="519ac-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="519ac-108">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="519ac-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="519ac-109">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="519ac-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="519ac-110">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="519ac-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="519ac-111">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="519ac-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="519ac-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="519ac-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519ac-113">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="519ac-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




