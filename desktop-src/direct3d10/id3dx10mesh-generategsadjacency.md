---
description: Adiciona dados de adjacência ao buffer de índice da malha. Quando a malha é enviada para um sombreador de geometria que usa dados de adjacência, é necessário que o buffer de índice da malha contenha dados de adjacência.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Método ID3DX10Mesh:: GenerateGSAdjacency (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012130"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="ce8af-104">Método ID3DX10Mesh:: GenerateGSAdjacency</span><span class="sxs-lookup"><span data-stu-id="ce8af-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="ce8af-105">Adiciona dados de adjacência ao buffer de índice da malha.</span><span class="sxs-lookup"><span data-stu-id="ce8af-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="ce8af-106">Quando a malha é enviada para um sombreador de geometria que usa dados de adjacência, é necessário que o buffer de índice da malha contenha dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="ce8af-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce8af-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce8af-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="ce8af-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce8af-108">Parameters</span></span>

<span data-ttu-id="ce8af-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ce8af-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce8af-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce8af-110">Return value</span></span>

<span data-ttu-id="ce8af-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce8af-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce8af-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ce8af-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8af-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce8af-113">Requirements</span></span>



| <span data-ttu-id="ce8af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce8af-114">Requirement</span></span> | <span data-ttu-id="ce8af-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ce8af-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce8af-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce8af-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ce8af-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce8af-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce8af-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce8af-118">Library</span></span><br/> | <dl> <span data-ttu-id="ce8af-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce8af-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce8af-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce8af-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce8af-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ce8af-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ce8af-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ce8af-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




