---
description: Atualiza informações de influência de Bone para corresponder os vértices depois que eles são reordenados. Esse método deve ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'Método ID3DXSkinInfo:: remapeador (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790516"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="ab0c0-104">Método ID3DXSkinInfo:: remapeador</span><span class="sxs-lookup"><span data-stu-id="ab0c0-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="ab0c0-105">Atualiza informações de influência de Bone para corresponder os vértices depois que eles são reordenados.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="ab0c0-106">Esse método deve ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0c0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab0c0-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="ab0c0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab0c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab0c0-109">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab0c0-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0c0-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab0c0-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab0c0-111">Número de vértices para remapear.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="ab0c0-112">*pVertexRemap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab0c0-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0c0-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab0c0-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ab0c0-114">Matriz de DWORDs cujo comprimento é especificado por NumVertices.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab0c0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab0c0-115">Return value</span></span>

<span data-ttu-id="ab0c0-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab0c0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab0c0-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab0c0-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0c0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab0c0-119">Remarks</span></span>

<span data-ttu-id="ab0c0-120">Cada elemento em pVertexRemap especifica o índice de vértice anterior para essa posição.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="ab0c0-121">Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap deve conter 3.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="ab0c0-122">A matriz de remapeamento de vértice retornada por [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0c0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab0c0-123">Requirements</span></span>



| <span data-ttu-id="ab0c0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab0c0-124">Requirement</span></span> | <span data-ttu-id="ab0c0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ab0c0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0c0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab0c0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ab0c0-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c0-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ab0c0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab0c0-128">Library</span></span><br/> | <dl> <span data-ttu-id="ab0c0-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c0-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab0c0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab0c0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0c0-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="ab0c0-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
