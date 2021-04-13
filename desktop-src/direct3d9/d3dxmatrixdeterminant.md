---
description: Retorna o determinante de uma matriz.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Função D3DXMatrixDeterminant (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298491"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="384c3-103">Função D3DXMatrixDeterminant (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="384c3-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="384c3-104">Retorna o determinante de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="384c3-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="384c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="384c3-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="384c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="384c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="384c3-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="384c3-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="384c3-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="384c3-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="384c3-109">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="384c3-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="384c3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="384c3-110">Return value</span></span>

<span data-ttu-id="384c3-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="384c3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="384c3-112">Retorna o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="384c3-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="384c3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="384c3-113">Requirements</span></span>



| <span data-ttu-id="384c3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="384c3-114">Requirement</span></span> | <span data-ttu-id="384c3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="384c3-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="384c3-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="384c3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="384c3-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="384c3-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="384c3-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="384c3-118">Library</span></span><br/> | <dl> <span data-ttu-id="384c3-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="384c3-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="384c3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="384c3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="384c3-121">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="384c3-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
