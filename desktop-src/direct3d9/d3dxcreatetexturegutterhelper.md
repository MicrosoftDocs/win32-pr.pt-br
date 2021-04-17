---
description: Cria um objeto ID3DXTextureGutterHelper com base em uma malha de entrada e dados de textura.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Função D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762333"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="bb534-103">Função D3DXCreateTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="bb534-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="bb534-104">Cria um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) com base em uma malha de entrada e dados de textura.</span><span class="sxs-lookup"><span data-stu-id="bb534-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb534-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb534-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="bb534-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb534-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb534-107">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb534-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb534-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb534-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb534-109">Largura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="bb534-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bb534-110">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb534-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb534-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb534-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb534-112">Altura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="bb534-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bb534-113">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb534-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb534-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bb534-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="bb534-115">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb534-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="bb534-116">*GutterSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb534-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb534-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb534-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb534-118">Número de texels por meio do qual passar a amostra da textura e criar a região da medianiz.</span><span class="sxs-lookup"><span data-stu-id="bb534-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="bb534-119">Deve ser pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="bb534-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="bb534-120">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bb534-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb534-121">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb534-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="bb534-122">Ponteiro para um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bb534-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb534-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb534-123">Return value</span></span>

<span data-ttu-id="bb534-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb534-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb534-125">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb534-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bb534-126">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bb534-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb534-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb534-127">Remarks</span></span>

<span data-ttu-id="bb534-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para transformar uma cena em novas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="bb534-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb534-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb534-129">Requirements</span></span>



| <span data-ttu-id="bb534-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb534-130">Requirement</span></span> | <span data-ttu-id="bb534-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bb534-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb534-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb534-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bb534-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb534-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb534-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb534-134">Library</span></span><br/> | <dl> <span data-ttu-id="bb534-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb534-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb534-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb534-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb534-137">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="bb534-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
