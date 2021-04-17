---
description: Chamado por um sombreador de interseção para relatar uma interseção de Ray.
ms.assetid: ''
title: Função ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790623"
---
# <a name="reporthit-function"></a><span data-ttu-id="b9e9b-103">Função ReportHit</span><span class="sxs-lookup"><span data-stu-id="b9e9b-103">ReportHit function</span></span>

<span data-ttu-id="b9e9b-104">Chamado por um [sombreador de interseção](intersection-shader.md) para relatar uma interseção de Ray.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9e9b-105">Syntax</span></span>
<span data-ttu-id="b9e9b-106">Essa definição de função intrínseca é equivalente ao seguinte modelo de função:</span><span class="sxs-lookup"><span data-stu-id="b9e9b-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="b9e9b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9e9b-107">Parameters</span></span>

`THit`

<span data-ttu-id="b9e9b-108">Um valor float que especifica a distância paramétrica da interseção..</span><span class="sxs-lookup"><span data-stu-id="b9e9b-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="b9e9b-109">Um inteiro sem sinal que identifica o tipo de ocorrência que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="b9e9b-110">Este é um valor especificado pelo usuário no intervalo de 0-127.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="b9e9b-111">O valor pode ser lido por [qualquer acesso](any-hit-shader.md) ou sombreadores de [tecle mais próximos](closest-hit-shader.md) com o intrínseco **HitKind** .</span><span class="sxs-lookup"><span data-stu-id="b9e9b-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="b9e9b-112">A estrutura de [**estrutura de atributo de interseção**](intersection-attributes.md) definida pelo usuário que especifica os atributos de interseção.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="b9e9b-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b9e9b-113">Return Value</span></span>

<span data-ttu-id="b9e9b-114">**bool** True se o pressionamento for aceito.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="b9e9b-115">Um pressionamento será rejeitado se *THit* estiver fora do intervalo de Ray atual, ou se qualquer sombreador de clique chamar [**IgnoreHit**](ignorehit-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9e9b-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="b9e9b-116">O intervalo de Ray atual é definido por **RayTMin** e **RayTCurrent**.</span><span class="sxs-lookup"><span data-stu-id="b9e9b-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e9b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9e9b-117">Remarks</span></span>

<span data-ttu-id="b9e9b-118">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="b9e9b-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="b9e9b-119">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="b9e9b-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="b9e9b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9e9b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e9b-121">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b9e9b-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




