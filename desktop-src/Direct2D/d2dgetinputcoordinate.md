---
title: Função D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Retorna o valor do TEXCOORDN de entrada. Disponível somente para entradas complexas.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Direct2D da função D2DGetInputCoordinate
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759152"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="ee278-105">Função D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="ee278-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="ee278-106">Retorna o valor do TEXCOORDN de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee278-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="ee278-107">Disponível somente para entradas complexas.</span><span class="sxs-lookup"><span data-stu-id="ee278-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee278-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee278-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="ee278-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee278-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee278-110">*N* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ee278-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee278-111">O número de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee278-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee278-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee278-112">Return value</span></span>

<span data-ttu-id="ee278-113">A função retorna um **FLOAT4**, no formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="ee278-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee278-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee278-114">Remarks</span></span>

<span data-ttu-id="ee278-115">A coordenada retornada por essa função está no espaço Texel.</span><span class="sxs-lookup"><span data-stu-id="ee278-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="ee278-116">Um sombreador não deve assumir nenhuma dependência de como esse valor é calculado.</span><span class="sxs-lookup"><span data-stu-id="ee278-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="ee278-117">Ele deve usá-lo apenas para exemplificar a entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="ee278-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="ee278-118">Para obter mais informações, consulte [adicionando um sombreador de pixel a uma transformação personalizada](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="ee278-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="ee278-119">O exemplo a seguir mostra a função usada para um efeito de mapa de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="ee278-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="ee278-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee278-120">Requirements</span></span>



| <span data-ttu-id="ee278-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee278-121">Requirement</span></span> | <span data-ttu-id="ee278-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ee278-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee278-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee278-123">Header</span></span><br/> | <dl> <span data-ttu-id="ee278-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="ee278-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ee278-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="ee278-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="ee278-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee278-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee278-128">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="ee278-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="ee278-129">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="ee278-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

