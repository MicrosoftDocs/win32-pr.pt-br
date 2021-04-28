---
description: 'Método ID3DXBaseMesh:: GetFVF – Obtém o valor de vértice da função fixa.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Método ID3DXBaseMesh:: GetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115434"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="a6df1-103">Método ID3DXBaseMesh:: GetFVF</span><span class="sxs-lookup"><span data-stu-id="a6df1-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="a6df1-104">Obtém o valor de vértice da função fixa.</span><span class="sxs-lookup"><span data-stu-id="a6df1-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6df1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6df1-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="a6df1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6df1-106">Parameters</span></span>

<span data-ttu-id="a6df1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a6df1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6df1-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a6df1-108">Return value</span></span>

<span data-ttu-id="a6df1-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6df1-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6df1-110">Retorna os códigos de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="a6df1-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6df1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6df1-111">Remarks</span></span>

<span data-ttu-id="a6df1-112">Esse método pode retornar 0 se o formato de vértice não puder ser mapeado diretamente para um código FVF.</span><span class="sxs-lookup"><span data-stu-id="a6df1-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="a6df1-113">Isso ocorrerá para uma malha criada a partir de uma declaração de vértice que não tenha a mesma ordem e elementos suportados pelos códigos FVF.</span><span class="sxs-lookup"><span data-stu-id="a6df1-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6df1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6df1-114">Requirements</span></span>



| <span data-ttu-id="a6df1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6df1-115">Requirement</span></span> | <span data-ttu-id="a6df1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a6df1-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6df1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6df1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a6df1-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6df1-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a6df1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6df1-119">Library</span></span><br/> | <dl> <span data-ttu-id="a6df1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6df1-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6df1-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a6df1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6df1-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a6df1-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
