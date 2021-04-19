---
title: Função QuadReadAcrossDiagonal
description: Retorna o valor local especificado que é lido da pista na diagonal oposta neste Quad.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- HLSL da função QuadReadAcrossDiagonal
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104988720"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="92047-104">Função QuadReadAcrossDiagonal</span><span class="sxs-lookup"><span data-stu-id="92047-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="92047-105">Retorna o valor local especificado que é lido da pista na diagonal oposta neste Quad.</span><span class="sxs-lookup"><span data-stu-id="92047-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="92047-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92047-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="92047-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92047-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92047-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="92047-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="92047-109">O tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="92047-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92047-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92047-110">Return value</span></span>

<span data-ttu-id="92047-111">O valor local especificado que é lido da pista na diagonal oposta neste Quad.</span><span class="sxs-lookup"><span data-stu-id="92047-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="92047-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92047-112">Remarks</span></span>

<span data-ttu-id="92047-113">Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="92047-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="92047-114">Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.</span><span class="sxs-lookup"><span data-stu-id="92047-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="92047-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="92047-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92047-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="92047-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




