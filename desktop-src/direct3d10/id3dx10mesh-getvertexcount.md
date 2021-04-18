---
description: Obtenha o número de vértices na malha.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Método ID3DX10Mesh:: GetVertexCount (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771578"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="73d2b-103">Método ID3DX10Mesh:: GetVertexCount</span><span class="sxs-lookup"><span data-stu-id="73d2b-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="73d2b-104">Obtenha o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="73d2b-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="73d2b-105">Uma malha pode conter vários buffers de vértice (ou seja, um buffer de vértice pode conter todos os dados de posição, outro pode incluir todos os dados de coordenadas de textura, etc.), no entanto, cada buffer de vértice conterá o mesmo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="73d2b-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d2b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73d2b-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="73d2b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73d2b-107">Parameters</span></span>

<span data-ttu-id="73d2b-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="73d2b-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73d2b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73d2b-109">Return value</span></span>

<span data-ttu-id="73d2b-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73d2b-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73d2b-111">O número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="73d2b-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d2b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73d2b-112">Requirements</span></span>



| <span data-ttu-id="73d2b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d2b-113">Requirement</span></span> | <span data-ttu-id="73d2b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="73d2b-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73d2b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73d2b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="73d2b-116"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d2b-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="73d2b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73d2b-117">Library</span></span><br/> | <dl> <span data-ttu-id="73d2b-118"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73d2b-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d2b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="73d2b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d2b-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="73d2b-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="73d2b-121">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="73d2b-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
