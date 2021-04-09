---
description: Usa interpolação linear para criar um valor de cor.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Função D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837943"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="1b5be-103">Função D3DXColorLerp</span><span class="sxs-lookup"><span data-stu-id="1b5be-103">D3DXColorLerp function</span></span>

<span data-ttu-id="1b5be-104">Usa interpolação linear para criar um valor de cor.</span><span class="sxs-lookup"><span data-stu-id="1b5be-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b5be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b5be-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="1b5be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b5be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5be-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1b5be-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5be-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b5be-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="1b5be-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1b5be-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1b5be-110"> \ \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b5be-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5be-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b5be-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="1b5be-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1b5be-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b5be-113">*pC2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b5be-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5be-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b5be-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="1b5be-115">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1b5be-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b5be-116">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1b5be-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5be-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b5be-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b5be-118">Parâmetro que interpola linearmente entre as cores, o e o pC2, tratando-as tanto como vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="1b5be-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="1b5be-119">Não há limites para o valor de s.</span><span class="sxs-lookup"><span data-stu-id="1b5be-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5be-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b5be-120">Return value</span></span>

<span data-ttu-id="1b5be-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b5be-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="1b5be-122">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="1b5be-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b5be-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b5be-123">Remarks</span></span>

<span data-ttu-id="1b5be-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1b5be-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1b5be-125">Dessa forma, a função **D3DXColorLerp** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1b5be-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1b5be-126">Essa função interpola os componentes vermelho, verde, azul e alfa de uma estrutura [**D3DXCOLOR**](d3dxcolor.md) entre duas cores, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b5be-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="1b5be-127">Se você estiver interpolando linearmente entre as cores a e B, e s for 0, a cor resultante será um. Se s for 1, a cor resultante será a cor B.</span><span class="sxs-lookup"><span data-stu-id="1b5be-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b5be-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b5be-128">Requirements</span></span>



| <span data-ttu-id="1b5be-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b5be-129">Requirement</span></span> | <span data-ttu-id="1b5be-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1b5be-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5be-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b5be-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1b5be-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5be-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1b5be-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b5be-133">Library</span></span><br/> | <dl> <span data-ttu-id="1b5be-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b5be-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b5be-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b5be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b5be-136">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1b5be-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1b5be-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="1b5be-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="1b5be-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="1b5be-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="1b5be-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="1b5be-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
