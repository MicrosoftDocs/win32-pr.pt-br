---
description: Cria uma matriz usando os deslocamentos especificados.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Função D3DXMatrixTranslation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298606"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="1612c-103">Função D3DXMatrixTranslation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1612c-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="1612c-104">Cria uma matriz usando os deslocamentos especificados.</span><span class="sxs-lookup"><span data-stu-id="1612c-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="1612c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1612c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="1612c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1612c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1612c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1612c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1612c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1612c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1612c-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1612c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1612c-110">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1612c-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1612c-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1612c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1612c-112">Deslocamento de coordenadas X.</span><span class="sxs-lookup"><span data-stu-id="1612c-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="1612c-113">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1612c-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1612c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1612c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1612c-115">Deslocamento de coordenadas Y.</span><span class="sxs-lookup"><span data-stu-id="1612c-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="1612c-116">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1612c-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1612c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1612c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1612c-118">Deslocamento de coordenadas Z.</span><span class="sxs-lookup"><span data-stu-id="1612c-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1612c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1612c-119">Return value</span></span>

<span data-ttu-id="1612c-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1612c-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1612c-121">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém uma matriz de transformação traduzida.</span><span class="sxs-lookup"><span data-stu-id="1612c-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1612c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1612c-122">Remarks</span></span>

<span data-ttu-id="1612c-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="1612c-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1612c-124">Dessa forma, o D3DXMATRIXTranslation pode ser usado como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1612c-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1612c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1612c-125">Requirements</span></span>



| <span data-ttu-id="1612c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1612c-126">Requirement</span></span> | <span data-ttu-id="1612c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1612c-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1612c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1612c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1612c-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1612c-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1612c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1612c-130">Library</span></span><br/> | <dl> <span data-ttu-id="1612c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1612c-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1612c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1612c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1612c-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1612c-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
