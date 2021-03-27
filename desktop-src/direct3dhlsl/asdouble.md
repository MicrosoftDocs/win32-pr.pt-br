---
title: função AsDouble
description: Reinterpreta um valor de conversão (valores de 2 32 bits) em um duplo.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- função HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006697"
---
# <a name="asdouble-function"></a><span data-ttu-id="7e087-104">função AsDouble</span><span class="sxs-lookup"><span data-stu-id="7e087-104">asdouble function</span></span>

<span data-ttu-id="7e087-105">Reinterpreta um valor de conversão (valores de 2 32 bits) em um duplo.</span><span class="sxs-lookup"><span data-stu-id="7e087-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e087-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e087-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="7e087-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e087-108">*lowbits* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e087-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e087-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7e087-109">Type: **uint**</span></span>

<span data-ttu-id="7e087-110">O padrão baixo de 32 bits do valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e087-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="7e087-111">*highbits* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e087-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e087-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7e087-112">Type: **uint**</span></span>

<span data-ttu-id="7e087-113">O padrão de alto bit de 32 bits do valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e087-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e087-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e087-114">Return value</span></span>

<span data-ttu-id="7e087-115">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="7e087-115">Type: **double**</span></span>

<span data-ttu-id="7e087-116">A entrada (valores de 2 32 bits) recast como um Double.</span><span class="sxs-lookup"><span data-stu-id="7e087-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e087-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e087-117">Remarks</span></span>

<span data-ttu-id="7e087-118">A seguinte versão sobrecarregada também está disponível:</span><span class="sxs-lookup"><span data-stu-id="7e087-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="7e087-119">Se o valor de entrada for de componentes de 2 32 bits, o tipo de retorno conterá um duplo.</span><span class="sxs-lookup"><span data-stu-id="7e087-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="7e087-120">Se o valor de entrada for de componentes de 4 32 bits, o tipo de retorno conterá dois duplos.</span><span class="sxs-lookup"><span data-stu-id="7e087-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="7e087-121">Se o valor de entrada for um tipo de 64 bits, o valor retornado terá o mesmo número de componentes que o valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e087-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="7e087-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7e087-122">Minimum Shader Model</span></span>

<span data-ttu-id="7e087-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7e087-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7e087-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7e087-124">Shader Model</span></span>                                                                | <span data-ttu-id="7e087-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7e087-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7e087-126">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7e087-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7e087-127">sim</span><span class="sxs-lookup"><span data-stu-id="7e087-127">yes</span></span>       |



 

<span data-ttu-id="7e087-128">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7e087-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7e087-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="7e087-129">Vertex</span></span> | <span data-ttu-id="7e087-130">Envoltória</span><span class="sxs-lookup"><span data-stu-id="7e087-130">Hull</span></span> | <span data-ttu-id="7e087-131">Domínio</span><span class="sxs-lookup"><span data-stu-id="7e087-131">Domain</span></span> | <span data-ttu-id="7e087-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="7e087-132">Geometry</span></span> | <span data-ttu-id="7e087-133">16x16</span><span class="sxs-lookup"><span data-stu-id="7e087-133">Pixel</span></span> | <span data-ttu-id="7e087-134">Computação</span><span class="sxs-lookup"><span data-stu-id="7e087-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7e087-135">x</span><span class="sxs-lookup"><span data-stu-id="7e087-135">x</span></span>      | <span data-ttu-id="7e087-136">x</span><span class="sxs-lookup"><span data-stu-id="7e087-136">x</span></span>    | <span data-ttu-id="7e087-137">x</span><span class="sxs-lookup"><span data-stu-id="7e087-137">x</span></span>      | <span data-ttu-id="7e087-138">x</span><span class="sxs-lookup"><span data-stu-id="7e087-138">x</span></span>        | <span data-ttu-id="7e087-139">x</span><span class="sxs-lookup"><span data-stu-id="7e087-139">x</span></span>     | <span data-ttu-id="7e087-140">x</span><span class="sxs-lookup"><span data-stu-id="7e087-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7e087-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e087-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e087-142">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="7e087-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7e087-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7e087-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




