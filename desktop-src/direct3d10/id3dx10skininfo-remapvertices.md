---
description: Altere quais vértices são influenciados por quais Bones.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Método ID3DX10SkinInfo:: RemapVertices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765319"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="2e0c4-103">Método ID3DX10SkinInfo:: RemapVertices</span><span class="sxs-lookup"><span data-stu-id="2e0c4-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="2e0c4-104">Altere quais vértices são influenciados por quais Bones.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e0c4-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="2e0c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e0c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0c4-107">*NewVertexCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e0c4-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0c4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e0c4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e0c4-109">O novo número de vértices.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="2e0c4-110">*pVertexRemap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e0c4-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0c4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e0c4-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e0c4-112">Um ponteiro para uma matriz de índices de vértice, que descrevem o remapeamento.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="2e0c4-113">Por exemplo, digamos que SkinInfo contenha alguns vértices de modo que bone0 seja mapeado para V0, bone1 para v1 e bone2 para v2, e matriz com 2, 1, 0 seja especificado para pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="2e0c4-114">Isso fará com que bone0 seja mapeado para v2, bone1 para v1 e bone2 para V0.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e0c4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e0c4-115">Return value</span></span>

<span data-ttu-id="2e0c4-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e0c4-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e0c4-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2e0c4-118">Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0c4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e0c4-119">Requirements</span></span>



| <span data-ttu-id="2e0c4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0c4-120">Requirement</span></span> | <span data-ttu-id="2e0c4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2e0c4-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0c4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e0c4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2e0c4-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0c4-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e0c4-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e0c4-124">Library</span></span><br/> | <dl> <span data-ttu-id="2e0c4-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e0c4-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0c4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e0c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0c4-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="2e0c4-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="2e0c4-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2e0c4-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
