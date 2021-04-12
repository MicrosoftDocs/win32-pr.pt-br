---
description: Determina se uma matriz é uma matriz de identidade.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: Função D3DXMatrixIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298736"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="78630-103">Função D3DXMatrixIsIdentity</span><span class="sxs-lookup"><span data-stu-id="78630-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="78630-104">Determina se uma matriz é uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="78630-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="78630-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78630-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="78630-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78630-107">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78630-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78630-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="78630-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78630-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que será testada para identidade.</span><span class="sxs-lookup"><span data-stu-id="78630-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78630-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78630-110">Return value</span></span>

<span data-ttu-id="78630-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78630-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78630-112">Se a matriz for uma matriz de identidade, essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="78630-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="78630-113">Caso contrário, essa função retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="78630-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78630-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78630-114">Requirements</span></span>



| <span data-ttu-id="78630-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="78630-115">Requirement</span></span> | <span data-ttu-id="78630-116">Valor</span><span class="sxs-lookup"><span data-stu-id="78630-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78630-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78630-117">Header</span></span><br/>  | <dl> <span data-ttu-id="78630-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78630-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="78630-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78630-119">Library</span></span><br/> | <dl> <span data-ttu-id="78630-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78630-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78630-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="78630-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78630-122">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="78630-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="78630-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="78630-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 
