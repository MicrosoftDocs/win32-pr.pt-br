---
description: Adiciona dois valores de cor juntos para criar um novo valor de cor.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Função D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105778517"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="ca148-103">Função D3DXColorAdd</span><span class="sxs-lookup"><span data-stu-id="ca148-103">D3DXColorAdd function</span></span>

<span data-ttu-id="ca148-104">Adiciona dois valores de cor juntos para criar um novo valor de cor.</span><span class="sxs-lookup"><span data-stu-id="ca148-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca148-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca148-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="ca148-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca148-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ca148-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca148-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca148-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ca148-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ca148-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca148-110"> \ \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca148-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca148-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca148-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ca148-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="ca148-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ca148-113">*pC2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca148-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca148-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca148-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ca148-115">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="ca148-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca148-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca148-116">Return value</span></span>

<span data-ttu-id="ca148-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca148-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ca148-118">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é a soma de dois valores de cor.</span><span class="sxs-lookup"><span data-stu-id="ca148-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca148-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca148-119">Remarks</span></span>

<span data-ttu-id="ca148-120">O valor de retorno para essa função é o mesmo valor retornado em pOut.</span><span class="sxs-lookup"><span data-stu-id="ca148-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="ca148-121">Dessa forma, a função **D3DXColorAdd** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="ca148-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca148-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca148-122">Requirements</span></span>



| <span data-ttu-id="ca148-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca148-123">Requirement</span></span> | <span data-ttu-id="ca148-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ca148-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca148-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca148-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ca148-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca148-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ca148-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca148-127">Library</span></span><br/> | <dl> <span data-ttu-id="ca148-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca148-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca148-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca148-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca148-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ca148-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ca148-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="ca148-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="ca148-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="ca148-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




