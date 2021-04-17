---
title: Função D2DGetInput (D2d1effecthelpers. h)
description: Retorna a cor da entrada N na coordenada de entrada. Disponível somente para entradas simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Direct2D da função D2DGetInput
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752924"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="c9088-105">Função D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="c9088-105">D2DGetInput function</span></span>

<span data-ttu-id="c9088-106">Retorna a cor da entrada N na coordenada de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9088-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="c9088-107">Disponível somente para entradas simples.</span><span class="sxs-lookup"><span data-stu-id="c9088-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9088-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9088-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="c9088-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9088-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9088-110">*N* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c9088-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9088-111">O número de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9088-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9088-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9088-112">Return value</span></span>

<span data-ttu-id="c9088-113">A função retorna um **FLOAT4**, contendo a cor RGBA no formato inputn.</span><span class="sxs-lookup"><span data-stu-id="c9088-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9088-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9088-114">Remarks</span></span>

<span data-ttu-id="c9088-115">O exemplo a seguir mostra a função que está sendo usada como parte de um efeito composto aritmético.</span><span class="sxs-lookup"><span data-stu-id="c9088-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="c9088-116">Além disso, consulte os comentários para [a \_ \_ entrada do PS D2D](d2d-ps-entry.md) para outro exemplo de uso dessa função.</span><span class="sxs-lookup"><span data-stu-id="c9088-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9088-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9088-117">Requirements</span></span>



| <span data-ttu-id="c9088-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9088-118">Requirement</span></span> | <span data-ttu-id="c9088-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c9088-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9088-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9088-120">Header</span></span><br/> | <dl> <span data-ttu-id="c9088-121"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="c9088-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="c9088-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c9088-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="c9088-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9088-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="c9088-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9088-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9088-125">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="c9088-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="c9088-126">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="c9088-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





