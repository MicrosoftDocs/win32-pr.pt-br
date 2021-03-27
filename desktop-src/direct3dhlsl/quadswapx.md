---
title: Função QuadReadAcrossX
description: Retorna o valor local especificado lido da outra pista neste Quad na direção X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- HLSL da função QuadReadAcrossX
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085000"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="31c45-104">Função QuadReadAcrossX</span><span class="sxs-lookup"><span data-stu-id="31c45-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="31c45-105">Retorna o valor local especificado lido da outra pista neste Quad na direção X.</span><span class="sxs-lookup"><span data-stu-id="31c45-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c45-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31c45-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="31c45-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31c45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c45-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="31c45-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="31c45-109">O tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="31c45-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c45-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31c45-110">Return value</span></span>

<span data-ttu-id="31c45-111">O valor local especificado.</span><span class="sxs-lookup"><span data-stu-id="31c45-111">The specified local value.</span></span> <span data-ttu-id="31c45-112">Se a pista de origem estiver inativa, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="31c45-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c45-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="31c45-113">Remarks</span></span>

<span data-ttu-id="31c45-114">Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="31c45-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="31c45-115">Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.</span><span class="sxs-lookup"><span data-stu-id="31c45-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="31c45-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="31c45-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c45-117">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="31c45-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




