---
description: Retorna o tamanho de um vértice para um formato de vértice flexível (FVF).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Função D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812288"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="0139a-103">Função D3DXGetFVFVertexSize</span><span class="sxs-lookup"><span data-stu-id="0139a-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="0139a-104">Retorna o tamanho de um vértice para um formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="0139a-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="0139a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0139a-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="0139a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0139a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0139a-107">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0139a-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0139a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0139a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0139a-109">FVF a ser consultada.</span><span class="sxs-lookup"><span data-stu-id="0139a-109">FVF to be queried.</span></span> <span data-ttu-id="0139a-110">Uma combinação de [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="0139a-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0139a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0139a-111">Return value</span></span>

<span data-ttu-id="0139a-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0139a-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0139a-113">O tamanho do vértice FVF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0139a-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0139a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0139a-114">Requirements</span></span>



| <span data-ttu-id="0139a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0139a-115">Requirement</span></span> | <span data-ttu-id="0139a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0139a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0139a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0139a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0139a-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0139a-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0139a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0139a-119">Library</span></span><br/> | <dl> <span data-ttu-id="0139a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0139a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0139a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0139a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0139a-122">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="0139a-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
