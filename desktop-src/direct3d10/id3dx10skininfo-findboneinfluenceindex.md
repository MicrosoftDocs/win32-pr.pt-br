---
description: Localize o índice que indica onde um determinado vértice está em uma determinada lista de vértices influenciados.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'Método ID3DX10SkinInfo:: FindBoneInfluenceIndex (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173095"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="8b356-103">Método ID3DX10SkinInfo:: FindBoneInfluenceIndex</span><span class="sxs-lookup"><span data-stu-id="8b356-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="8b356-104">Localize o índice que indica onde um determinado vértice está em uma determinada lista de vértices influenciados.</span><span class="sxs-lookup"><span data-stu-id="8b356-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b356-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b356-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="8b356-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b356-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b356-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b356-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b356-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b356-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b356-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="8b356-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="8b356-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="8b356-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b356-111">*VertexIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b356-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b356-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b356-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b356-113">O índice do vértice no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="8b356-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8b356-114">*pInfluenceIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b356-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b356-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b356-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8b356-116">O índice do vértice na lista de vértices influenciados do Bone.</span><span class="sxs-lookup"><span data-stu-id="8b356-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b356-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b356-117">Return value</span></span>

<span data-ttu-id="8b356-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b356-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b356-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b356-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8b356-120">Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8b356-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b356-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b356-121">Requirements</span></span>



| <span data-ttu-id="8b356-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b356-122">Requirement</span></span> | <span data-ttu-id="8b356-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8b356-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b356-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b356-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8b356-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b356-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b356-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b356-126">Library</span></span><br/> | <dl> <span data-ttu-id="8b356-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b356-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b356-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b356-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b356-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8b356-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8b356-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8b356-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
