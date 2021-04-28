---
description: Função D3DXFloat32To16Array (D3DX10Math. h) – converte uma matriz de 32 bits floats em floats de 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Função D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103514"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="770b4-103">Função D3DXFloat32To16Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="770b4-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="770b4-104">Converte uma matriz de 32-bit floats em floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="770b4-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="770b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="770b4-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="770b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="770b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="770b4-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="770b4-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770b4-108">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="770b4-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="770b4-109">Ponteiro para a matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="770b4-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="770b4-110">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="770b4-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770b4-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="770b4-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="770b4-112">Ponteiro para uma matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="770b4-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="770b4-113">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="770b4-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770b4-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="770b4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="770b4-115">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="770b4-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="770b4-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="770b4-116">Return value</span></span>

<span data-ttu-id="770b4-117">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="770b4-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="770b4-118">Ponteiro para uma matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="770b4-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="770b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="770b4-119">Requirements</span></span>



| <span data-ttu-id="770b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="770b4-120">Requirement</span></span> | <span data-ttu-id="770b4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="770b4-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="770b4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="770b4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="770b4-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="770b4-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="770b4-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="770b4-124">Library</span></span><br/> | <dl> <span data-ttu-id="770b4-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="770b4-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="770b4-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="770b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770b4-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="770b4-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
