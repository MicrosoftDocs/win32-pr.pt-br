---
description: Função D3DXMatrixDeterminant (D3DX10Math. h) – retorna o determinante de uma matriz.
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Função D3DXMatrixDeterminant (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103454"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="4eebd-103">Função D3DXMatrixDeterminant (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4eebd-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="4eebd-104">Retorna o determinante de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="4eebd-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eebd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4eebd-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4eebd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4eebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eebd-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4eebd-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eebd-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4eebd-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4eebd-109">Ponteiro para a estrutura de D3DXMATRIX de origem.</span><span class="sxs-lookup"><span data-stu-id="4eebd-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eebd-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4eebd-110">Return value</span></span>

<span data-ttu-id="4eebd-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4eebd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4eebd-112">Retorna o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="4eebd-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eebd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eebd-113">Requirements</span></span>



| <span data-ttu-id="4eebd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eebd-114">Requirement</span></span> | <span data-ttu-id="4eebd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4eebd-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eebd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4eebd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4eebd-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eebd-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4eebd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4eebd-118">Library</span></span><br/> | <dl> <span data-ttu-id="4eebd-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4eebd-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4eebd-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4eebd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eebd-121">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="4eebd-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
