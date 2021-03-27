---
title: Função QuadReadAcrossY
description: Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- HLSL da função QuadReadAcrossY
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967232"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="344ec-104">Função QuadReadAcrossY</span><span class="sxs-lookup"><span data-stu-id="344ec-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="344ec-105">Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y.</span><span class="sxs-lookup"><span data-stu-id="344ec-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="344ec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="344ec-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="344ec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="344ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344ec-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="344ec-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="344ec-109">O tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="344ec-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="344ec-110">Return value</span></span>

<span data-ttu-id="344ec-111">O valor de origem especificado.</span><span class="sxs-lookup"><span data-stu-id="344ec-111">The specified source value.</span></span> <span data-ttu-id="344ec-112">Se a pista de origem estiver inativa, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="344ec-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="344ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="344ec-113">Remarks</span></span>

<span data-ttu-id="344ec-114">Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="344ec-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="344ec-115">Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.</span><span class="sxs-lookup"><span data-stu-id="344ec-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="344ec-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="344ec-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344ec-117">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="344ec-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




