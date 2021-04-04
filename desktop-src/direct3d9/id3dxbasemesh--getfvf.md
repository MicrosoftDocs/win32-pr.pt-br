---
description: Obtém o valor de vértice da função fixa.
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
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930634"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="14e15-103">Método ID3DXBaseMesh:: GetFVF</span><span class="sxs-lookup"><span data-stu-id="14e15-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="14e15-104">Obtém o valor de vértice da função fixa.</span><span class="sxs-lookup"><span data-stu-id="14e15-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14e15-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="14e15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14e15-106">Parameters</span></span>

<span data-ttu-id="14e15-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="14e15-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14e15-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14e15-108">Return value</span></span>

<span data-ttu-id="14e15-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14e15-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14e15-110">Retorna os códigos de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="14e15-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e15-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="14e15-111">Remarks</span></span>

<span data-ttu-id="14e15-112">Esse método pode retornar 0 se o formato de vértice não puder ser mapeado diretamente para um código FVF.</span><span class="sxs-lookup"><span data-stu-id="14e15-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="14e15-113">Isso ocorrerá para uma malha criada a partir de uma declaração de vértice que não tenha a mesma ordem e elementos suportados pelos códigos FVF.</span><span class="sxs-lookup"><span data-stu-id="14e15-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e15-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14e15-114">Requirements</span></span>



| <span data-ttu-id="14e15-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e15-115">Requirement</span></span> | <span data-ttu-id="14e15-116">Valor</span><span class="sxs-lookup"><span data-stu-id="14e15-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e15-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14e15-117">Header</span></span><br/>  | <dl> <span data-ttu-id="14e15-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e15-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="14e15-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14e15-119">Library</span></span><br/> | <dl> <span data-ttu-id="14e15-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14e15-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14e15-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="14e15-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e15-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="14e15-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
