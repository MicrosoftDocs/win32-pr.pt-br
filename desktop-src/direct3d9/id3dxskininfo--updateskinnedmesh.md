---
description: Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Método ID3DXSkinInfo:: UpdateSkinnedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780372"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="ea8db-103">Método ID3DXSkinInfo:: UpdateSkinnedMesh</span><span class="sxs-lookup"><span data-stu-id="ea8db-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="ea8db-104">Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.</span><span class="sxs-lookup"><span data-stu-id="ea8db-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea8db-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="ea8db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea8db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8db-107">*pBoneTransforms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea8db-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8db-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8db-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ea8db-109">Matriz de transformação de Bone.</span><span class="sxs-lookup"><span data-stu-id="ea8db-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ea8db-110">*pBoneInvTransposeTransforms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea8db-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8db-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8db-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ea8db-112">Transpose inversa da matriz de transformação Bone.</span><span class="sxs-lookup"><span data-stu-id="ea8db-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ea8db-113">*pVerticesSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea8db-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8db-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea8db-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea8db-115">Ponteiro para o buffer que contém os vértices de origem.</span><span class="sxs-lookup"><span data-stu-id="ea8db-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ea8db-116">*pVerticesDst* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea8db-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8db-117">Tipo: **[ **pVoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea8db-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea8db-118">Ponteiro para o buffer que contém os vértices de destino.</span><span class="sxs-lookup"><span data-stu-id="ea8db-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8db-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea8db-119">Return value</span></span>

<span data-ttu-id="ea8db-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea8db-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea8db-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea8db-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea8db-122">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea8db-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8db-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea8db-123">Remarks</span></span>

<span data-ttu-id="ea8db-124">Quando usado para vértices de capa com dois elementos position, esse método diverte o segundo elemento position com o inverso do Bone em vez do próprio Bone.</span><span class="sxs-lookup"><span data-stu-id="ea8db-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea8db-125">Requirements</span></span>



| <span data-ttu-id="ea8db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8db-126">Requirement</span></span> | <span data-ttu-id="ea8db-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ea8db-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8db-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea8db-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ea8db-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8db-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ea8db-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea8db-130">Library</span></span><br/> | <dl> <span data-ttu-id="ea8db-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea8db-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea8db-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea8db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8db-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="ea8db-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
