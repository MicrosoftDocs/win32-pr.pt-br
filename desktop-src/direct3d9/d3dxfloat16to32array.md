---
description: Converte uma matriz de floats de 16 bits em floats de 32 bits.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Função D3DXFloat16To32Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791066"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="97c67-103">Função D3DXFloat16To32Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="97c67-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="97c67-104">Converte uma matriz de floats de 16 bits em floats de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="97c67-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97c67-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="97c67-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97c67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c67-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="97c67-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c67-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="97c67-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="97c67-109">Ponteiro para a matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="97c67-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="97c67-110">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97c67-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c67-111">Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="97c67-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="97c67-112">Ponteiro para uma matriz de floats de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="97c67-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="97c67-113">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="97c67-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c67-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c67-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c67-115">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="97c67-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c67-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97c67-116">Return value</span></span>

<span data-ttu-id="97c67-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="97c67-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="97c67-118">Ponteiro para uma matriz de flutuações de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="97c67-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c67-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c67-119">Requirements</span></span>



| <span data-ttu-id="97c67-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c67-120">Requirement</span></span> | <span data-ttu-id="97c67-121">Valor</span><span class="sxs-lookup"><span data-stu-id="97c67-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c67-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97c67-122">Header</span></span><br/>  | <dl> <span data-ttu-id="97c67-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c67-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="97c67-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97c67-124">Library</span></span><br/> | <dl> <span data-ttu-id="97c67-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c67-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97c67-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="97c67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c67-127">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="97c67-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
