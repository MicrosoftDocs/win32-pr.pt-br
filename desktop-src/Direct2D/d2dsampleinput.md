---
title: Função D2DSampleInput (D2d1effecthelpers. h)
description: Exemplos de entrada N na posição UV. Disponível somente para entradas complexas.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Direct2D da função D2DSampleInput
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775646"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="7a1be-105">Função D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="7a1be-105">D2DSampleInput function</span></span>

<span data-ttu-id="7a1be-106">Exemplos de entrada N na posição UV.</span><span class="sxs-lookup"><span data-stu-id="7a1be-106">Samples input N at position uv.</span></span> <span data-ttu-id="7a1be-107">Disponível somente para entradas complexas.</span><span class="sxs-lookup"><span data-stu-id="7a1be-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1be-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a1be-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="7a1be-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a1be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a1be-110">*N* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7a1be-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1be-111">O número de entrada.</span><span class="sxs-lookup"><span data-stu-id="7a1be-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="7a1be-112">*UV* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a1be-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1be-113">A posição UV.</span><span class="sxs-lookup"><span data-stu-id="7a1be-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a1be-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a1be-114">Return value</span></span>

<span data-ttu-id="7a1be-115">A função retorna um **FLOAT4**, no formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="7a1be-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a1be-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a1be-116">Remarks</span></span>

<span data-ttu-id="7a1be-117">O exemplo a seguir mostra a função que está sendo usada para calcular os Normals da superfície.</span><span class="sxs-lookup"><span data-stu-id="7a1be-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="7a1be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a1be-118">Requirements</span></span>



| <span data-ttu-id="7a1be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a1be-119">Requirement</span></span> | <span data-ttu-id="7a1be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a1be-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1be-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a1be-121">Header</span></span><br/> | <dl> <span data-ttu-id="7a1be-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="7a1be-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="7a1be-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1be-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="7a1be-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1be-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="7a1be-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a1be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1be-126">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="7a1be-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="7a1be-127">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="7a1be-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





