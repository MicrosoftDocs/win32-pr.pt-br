---
description: Converte uma matriz de 32-bit floats em floats de 16 bits.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Função D3DXFloat32To16Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808356"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="953ed-103">Função D3DXFloat32To16Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="953ed-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="953ed-104">Converte uma matriz de 32-bit floats em floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="953ed-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="953ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="953ed-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="953ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="953ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="953ed-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="953ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="953ed-108">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="953ed-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="953ed-109">Ponteiro para a matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="953ed-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="953ed-110">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953ed-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953ed-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="953ed-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="953ed-112">Ponteiro para uma matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="953ed-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="953ed-113">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="953ed-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953ed-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="953ed-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="953ed-115">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="953ed-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="953ed-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="953ed-116">Return value</span></span>

<span data-ttu-id="953ed-117">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="953ed-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="953ed-118">Ponteiro para uma matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="953ed-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="953ed-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="953ed-119">Requirements</span></span>



| <span data-ttu-id="953ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="953ed-120">Requirement</span></span> | <span data-ttu-id="953ed-121">Valor</span><span class="sxs-lookup"><span data-stu-id="953ed-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="953ed-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="953ed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="953ed-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="953ed-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="953ed-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="953ed-124">Library</span></span><br/> | <dl> <span data-ttu-id="953ed-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="953ed-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="953ed-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="953ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953ed-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="953ed-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
