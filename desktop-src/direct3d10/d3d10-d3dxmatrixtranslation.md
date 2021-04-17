---
description: Crie uma matriz de conversão.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: Função D3DXMatrixTranslation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766544"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="5fec9-103">Função D3DXMatrixTranslation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5fec9-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="5fec9-104">Crie uma matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="5fec9-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fec9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fec9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="5fec9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fec9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fec9-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5fec9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fec9-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5fec9-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5fec9-109">A matriz que se tornará uma matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="5fec9-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="5fec9-110">Consulte [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5fec9-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fec9-111">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5fec9-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fec9-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fec9-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fec9-113">O componente x da tradução.</span><span class="sxs-lookup"><span data-stu-id="5fec9-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5fec9-114">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5fec9-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fec9-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fec9-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fec9-116">O componente y da tradução.</span><span class="sxs-lookup"><span data-stu-id="5fec9-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5fec9-117">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5fec9-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fec9-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fec9-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fec9-119">O componente z da tradução.</span><span class="sxs-lookup"><span data-stu-id="5fec9-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fec9-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fec9-120">Return value</span></span>

<span data-ttu-id="5fec9-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5fec9-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5fec9-122">A matriz de translação.</span><span class="sxs-lookup"><span data-stu-id="5fec9-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fec9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fec9-123">Requirements</span></span>



| <span data-ttu-id="5fec9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fec9-124">Requirement</span></span> | <span data-ttu-id="5fec9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5fec9-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fec9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fec9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5fec9-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fec9-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5fec9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fec9-128">Library</span></span><br/> | <dl> <span data-ttu-id="5fec9-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fec9-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5fec9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fec9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fec9-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="5fec9-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
