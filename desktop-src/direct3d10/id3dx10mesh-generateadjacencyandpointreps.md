---
description: Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Método ID3DX10Mesh:: GenerateAdjacencyAndPointReps (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506507"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="efd38-103">Método ID3DX10Mesh:: GenerateAdjacencyAndPointReps</span><span class="sxs-lookup"><span data-stu-id="efd38-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="efd38-104">Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.</span><span class="sxs-lookup"><span data-stu-id="efd38-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efd38-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="efd38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efd38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd38-107">*Épsilon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efd38-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd38-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efd38-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efd38-109">Especifica que os vértices que diferem na posição por menos de Épsilon devem ser tratados como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="efd38-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd38-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efd38-110">Return value</span></span>

<span data-ttu-id="efd38-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efd38-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efd38-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="efd38-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="efd38-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="efd38-113">Remarks</span></span>

<span data-ttu-id="efd38-114">Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="efd38-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="efd38-115">A ordem das entradas no buffer de adjacência é determinada pela ordem dos índices de vértice no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="efd38-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="efd38-116">O triângulo adjacente 0 sempre corresponde à borda entre os índices dos cantos 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="efd38-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="efd38-117">O triângulo adjacente 1 sempre corresponde à borda entre os índices dos cantos 1 e 2, enquanto o triângulo adjacente 2 corresponde à borda entre os índices dos cantos 2 e 0.</span><span class="sxs-lookup"><span data-stu-id="efd38-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd38-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efd38-118">Requirements</span></span>



| <span data-ttu-id="efd38-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="efd38-119">Requirement</span></span> | <span data-ttu-id="efd38-120">Valor</span><span class="sxs-lookup"><span data-stu-id="efd38-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efd38-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efd38-121">Header</span></span><br/>  | <dl> <span data-ttu-id="efd38-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd38-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="efd38-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efd38-123">Library</span></span><br/> | <dl> <span data-ttu-id="efd38-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efd38-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efd38-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="efd38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd38-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="efd38-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="efd38-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="efd38-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
