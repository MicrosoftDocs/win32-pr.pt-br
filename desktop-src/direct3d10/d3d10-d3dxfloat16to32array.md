---
description: Converte uma matriz de floats de 16 bits em floats de 32 bits.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Função D3DXFloat16To32Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298647"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="b70ff-103">Função D3DXFloat16To32Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b70ff-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="b70ff-104">Converte uma matriz de floats de 16 bits em floats de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b70ff-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b70ff-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="b70ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b70ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70ff-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b70ff-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70ff-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b70ff-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b70ff-109">Ponteiro para a matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b70ff-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="b70ff-110">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b70ff-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70ff-111">Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="b70ff-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="b70ff-112">Ponteiro para uma matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b70ff-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="b70ff-113">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b70ff-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70ff-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b70ff-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b70ff-115">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="b70ff-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70ff-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b70ff-116">Return value</span></span>

<span data-ttu-id="b70ff-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b70ff-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b70ff-118">Ponteiro para uma matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b70ff-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70ff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b70ff-119">Requirements</span></span>



| <span data-ttu-id="b70ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b70ff-120">Requirement</span></span> | <span data-ttu-id="b70ff-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b70ff-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b70ff-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b70ff-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b70ff-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b70ff-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b70ff-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b70ff-124">Library</span></span><br/> | <dl> <span data-ttu-id="b70ff-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b70ff-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b70ff-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b70ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70ff-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b70ff-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
