---
description: Dimensione o plano com o fator de dimensionamento fornecido.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: Função D3DXPlaneScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105755149"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="23f68-103">Função D3DXPlaneScale</span><span class="sxs-lookup"><span data-stu-id="23f68-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="23f68-104">Dimensione o plano com o fator de dimensionamento fornecido.</span><span class="sxs-lookup"><span data-stu-id="23f68-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23f68-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="23f68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23f68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f68-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="23f68-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="23f68-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="23f68-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="23f68-109">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="23f68-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="23f68-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23f68-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f68-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="23f68-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="23f68-112">Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="23f68-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="23f68-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="23f68-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f68-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23f68-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23f68-115">Fator de escala.</span><span class="sxs-lookup"><span data-stu-id="23f68-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f68-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23f68-116">Return value</span></span>

<span data-ttu-id="23f68-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="23f68-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="23f68-118">Ponteiro para uma estrutura [**D3DXPLANE**](d3dxplane.md) que representa o plano dimensionado.</span><span class="sxs-lookup"><span data-stu-id="23f68-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f68-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="23f68-119">Remarks</span></span>

<span data-ttu-id="23f68-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="23f68-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="23f68-121">Portanto, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="23f68-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f68-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f68-122">Requirements</span></span>



| <span data-ttu-id="23f68-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f68-123">Requirement</span></span> | <span data-ttu-id="23f68-124">Valor</span><span class="sxs-lookup"><span data-stu-id="23f68-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f68-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23f68-125">Header</span></span><br/>  | <dl> <span data-ttu-id="23f68-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f68-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="23f68-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23f68-127">Library</span></span><br/> | <dl> <span data-ttu-id="23f68-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23f68-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23f68-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="23f68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f68-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="23f68-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
