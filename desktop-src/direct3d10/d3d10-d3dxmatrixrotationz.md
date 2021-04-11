---
description: Cria uma matriz que gira em volta do eixo z.
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: Função D3DXMatrixRotationZ (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3dfe1d3d43e4110c4e7554c75fba3ac89a69ccb3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173142"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="891b0-103">Função D3DXMatrixRotationZ (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="891b0-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="891b0-104">Cria uma matriz que gira em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="891b0-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="891b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="891b0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="891b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="891b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891b0-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="891b0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="891b0-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="891b0-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="891b0-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="891b0-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="891b0-110">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="891b0-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="891b0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="891b0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="891b0-112">Ângulo de rotação, em radianos.</span><span class="sxs-lookup"><span data-stu-id="891b0-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="891b0-113">Os ângulos são medidos no sentido horário quando exibidos do eixo de rotação (lado positivo) em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="891b0-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891b0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="891b0-114">Return value</span></span>

<span data-ttu-id="891b0-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="891b0-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="891b0-116">Ponteiro para uma estrutura D3DXMATRIX girado em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="891b0-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="891b0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="891b0-117">Remarks</span></span>

<span data-ttu-id="891b0-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="891b0-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="891b0-119">Dessa forma, a função D3DXMatrixRotationZ pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="891b0-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="891b0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="891b0-120">Requirements</span></span>



| <span data-ttu-id="891b0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="891b0-121">Requirement</span></span> | <span data-ttu-id="891b0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="891b0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="891b0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="891b0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="891b0-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="891b0-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="891b0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="891b0-125">Library</span></span><br/> | <dl> <span data-ttu-id="891b0-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="891b0-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="891b0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="891b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891b0-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="891b0-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
