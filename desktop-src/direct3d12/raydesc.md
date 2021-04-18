---
description: Passado para a função TraceRay para definir a origem, a direção e as extensões do raio.
ms.assetid: ''
title: Estrutura RayDesc
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814049"
---
# <a name="raydesc-structure"></a><span data-ttu-id="d55df-103">Estrutura RayDesc</span><span class="sxs-lookup"><span data-stu-id="d55df-103">RayDesc structure</span></span>

<span data-ttu-id="d55df-104">Passado para a função [**TraceRay**](traceray-function.md) para definir a origem, a direção e as extensões do raio.</span><span class="sxs-lookup"><span data-stu-id="d55df-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d55df-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="d55df-106">Campos</span><span class="sxs-lookup"><span data-stu-id="d55df-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="d55df-107"><span id="Origin"></span><span id="origin"></span>**Ter**</span><span class="sxs-lookup"><span data-stu-id="d55df-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="d55df-108">A origem do raio.</span><span class="sxs-lookup"><span data-stu-id="d55df-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="d55df-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span><span class="sxs-lookup"><span data-stu-id="d55df-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="d55df-110">A extensão mínima do raio.</span><span class="sxs-lookup"><span data-stu-id="d55df-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="d55df-111"><span id="Direction"></span><span id="direction"></span>**Direção**</span><span class="sxs-lookup"><span data-stu-id="d55df-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="d55df-112">A direção do raio.</span><span class="sxs-lookup"><span data-stu-id="d55df-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="d55df-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span><span class="sxs-lookup"><span data-stu-id="d55df-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="d55df-114">A extensão máxima do raio.</span><span class="sxs-lookup"><span data-stu-id="d55df-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="d55df-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d55df-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="d55df-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d55df-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55df-117">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d55df-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




