---
description: Obtém o número máximo de influências em uma malha de triângulos com o buffer de índice especificado.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'Método ID3DXSkinInfo:: GetMaxFaceInfluences (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370914"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="90f77-103">Método ID3DXSkinInfo:: GetMaxFaceInfluences</span><span class="sxs-lookup"><span data-stu-id="90f77-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="90f77-104">Obtém o número máximo de influências em uma malha de triângulos com o buffer de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="90f77-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="90f77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90f77-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="90f77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90f77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90f77-107">*pIB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90f77-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90f77-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="90f77-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="90f77-109">Ponteiro para o buffer de índice que contém os dados do índice de malha.</span><span class="sxs-lookup"><span data-stu-id="90f77-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="90f77-110">*NumFaces* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90f77-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90f77-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90f77-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90f77-112">Número de faces na malha.</span><span class="sxs-lookup"><span data-stu-id="90f77-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="90f77-113">*maxFaceInfluences* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90f77-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90f77-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="90f77-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="90f77-115">Ponteiro para a superfície máxima influencia.</span><span class="sxs-lookup"><span data-stu-id="90f77-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90f77-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90f77-116">Return value</span></span>

<span data-ttu-id="90f77-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90f77-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90f77-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90f77-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="90f77-119">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="90f77-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="90f77-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90f77-120">Requirements</span></span>



| <span data-ttu-id="90f77-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="90f77-121">Requirement</span></span> | <span data-ttu-id="90f77-122">Valor</span><span class="sxs-lookup"><span data-stu-id="90f77-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90f77-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90f77-123">Header</span></span><br/>  | <dl> <span data-ttu-id="90f77-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="90f77-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="90f77-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90f77-125">Library</span></span><br/> | <dl> <span data-ttu-id="90f77-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90f77-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90f77-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="90f77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f77-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="90f77-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
