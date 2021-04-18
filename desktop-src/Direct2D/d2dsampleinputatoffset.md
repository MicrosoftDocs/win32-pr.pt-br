---
title: Função D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Exemplos de entrada N em um deslocamento de deslocamento da coordenada de entrada. Disponível somente para entradas complexas.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Direct2D da função D2DSampleInputAtOffset
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755807"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="cb3aa-105">Função D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="cb3aa-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="cb3aa-106">Exemplos de entrada N em um deslocamento de deslocamento da coordenada de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="cb3aa-107">Disponível somente para entradas complexas.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3aa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb3aa-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="cb3aa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb3aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3aa-110">*N* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="cb3aa-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3aa-111">O número de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="cb3aa-112">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb3aa-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3aa-113">O deslocamento UV.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3aa-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb3aa-114">Return value</span></span>

<span data-ttu-id="cb3aa-115">A função retorna um **FLOAT4**, no formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3aa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb3aa-116">Remarks</span></span>

<span data-ttu-id="cb3aa-117">O exemplo a seguir mostra a função que está sendo usada como parte de uma máscara de gradiente de realce e sombra.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="cb3aa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb3aa-118">Requirements</span></span>



| <span data-ttu-id="cb3aa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3aa-119">Requirement</span></span> | <span data-ttu-id="cb3aa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cb3aa-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3aa-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb3aa-121">Header</span></span><br/> | <dl> <span data-ttu-id="cb3aa-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="cb3aa-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="cb3aa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cb3aa-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="cb3aa-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb3aa-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="cb3aa-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb3aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3aa-126">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="cb3aa-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="cb3aa-127">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="cb3aa-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





