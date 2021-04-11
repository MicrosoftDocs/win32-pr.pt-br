---
description: Combina duas cores.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: Função D3DXColorModulate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173074"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="db64c-103">Função D3DXColorModulate</span><span class="sxs-lookup"><span data-stu-id="db64c-103">D3DXColorModulate function</span></span>

<span data-ttu-id="db64c-104">Combina duas cores.</span><span class="sxs-lookup"><span data-stu-id="db64c-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="db64c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db64c-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="db64c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db64c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db64c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="db64c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="db64c-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="db64c-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="db64c-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="db64c-110"> \ \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db64c-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="db64c-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="db64c-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="db64c-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db64c-113">*pC2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db64c-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="db64c-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="db64c-115">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="db64c-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db64c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db64c-116">Return value</span></span>

<span data-ttu-id="db64c-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="db64c-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="db64c-118">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="db64c-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="db64c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="db64c-119">Remarks</span></span>

<span data-ttu-id="db64c-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="db64c-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="db64c-121">Dessa forma, a função **D3DXColorModulate** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="db64c-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="db64c-122">Essa função combina duas cores multiplicando os componentes de cor correspondentes, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="db64c-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="db64c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db64c-123">Requirements</span></span>



| <span data-ttu-id="db64c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="db64c-124">Requirement</span></span> | <span data-ttu-id="db64c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="db64c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db64c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db64c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="db64c-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="db64c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db64c-128">Library</span></span><br/> | <dl> <span data-ttu-id="db64c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db64c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="db64c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db64c-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="db64c-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="db64c-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="db64c-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="db64c-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="db64c-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="db64c-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="db64c-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




