---
title: Função QuadReadLaneAt
description: Retorna o valor de origem especificado da pista identificada pela ID da pista dentro do Quad atual.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- HLSL da função QuadReadLaneAt
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454455"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="36244-104">Função QuadReadLaneAt</span><span class="sxs-lookup"><span data-stu-id="36244-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="36244-105">Retorna o valor de origem especificado da pista identificada pela ID da pista dentro do Quad atual.</span><span class="sxs-lookup"><span data-stu-id="36244-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="36244-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36244-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="36244-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36244-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36244-108">*origemvalue*</span><span class="sxs-lookup"><span data-stu-id="36244-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="36244-109">O tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="36244-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="36244-110">*quadLaneID*</span><span class="sxs-lookup"><span data-stu-id="36244-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="36244-111">A ID da raia; Esse será um valor de 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="36244-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36244-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36244-112">Return value</span></span>

<span data-ttu-id="36244-113">O valor de origem especificado.</span><span class="sxs-lookup"><span data-stu-id="36244-113">The specified source value.</span></span> <span data-ttu-id="36244-114">O resultado dessa função é uniforme em todo o quad.</span><span class="sxs-lookup"><span data-stu-id="36244-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="36244-115">Se a pista de origem estiver inativa, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="36244-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="36244-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="36244-116">Remarks</span></span>

<span data-ttu-id="36244-117">Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="36244-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="36244-118">Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.</span><span class="sxs-lookup"><span data-stu-id="36244-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="36244-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="36244-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36244-120">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="36244-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




