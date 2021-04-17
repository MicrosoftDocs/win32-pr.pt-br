---
description: Obtém os parâmetros de deslocamento da geometria de malha.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'Método ID3DXPatchMesh:: GetDisplaceParam (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771416"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="e7b71-103">Método ID3DXPatchMesh:: GetDisplaceParam</span><span class="sxs-lookup"><span data-stu-id="e7b71-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="e7b71-104">Obtém os parâmetros de deslocamento da geometria de malha.</span><span class="sxs-lookup"><span data-stu-id="e7b71-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7b71-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="e7b71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7b71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b71-107">*Textura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="e7b71-109">Textura que contém os dados de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="e7b71-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="e7b71-110">*MinFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-111">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="e7b71-112">Nível de minificação.</span><span class="sxs-lookup"><span data-stu-id="e7b71-112">Minification level.</span></span> <span data-ttu-id="e7b71-113">Para obter mais informações, consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="e7b71-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7b71-114">*MagFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-115">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="e7b71-116">Nível de ampliação.</span><span class="sxs-lookup"><span data-stu-id="e7b71-116">Magnification level.</span></span> <span data-ttu-id="e7b71-117">Para obter mais informações, consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="e7b71-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7b71-118">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-119">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="e7b71-120">Nível de filtro MIP.</span><span class="sxs-lookup"><span data-stu-id="e7b71-120">Mip filter level.</span></span> <span data-ttu-id="e7b71-121">Para obter mais informações, consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="e7b71-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7b71-122">*Encapsular* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-123">Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="e7b71-124">Modo de quebra automática de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="e7b71-124">Texture address wrap mode.</span></span> <span data-ttu-id="e7b71-125">Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="e7b71-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7b71-126">*dwLODBias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7b71-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b71-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7b71-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7b71-128">Nível de valor de tendência de detalhes.</span><span class="sxs-lookup"><span data-stu-id="e7b71-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b71-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7b71-129">Return value</span></span>

<span data-ttu-id="e7b71-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7b71-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7b71-131">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7b71-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7b71-132">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e7b71-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b71-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7b71-133">Remarks</span></span>

<span data-ttu-id="e7b71-134">Os mapas de substituição só podem ser texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="e7b71-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="e7b71-135">Mipmapping é ignorado para mosaico não adaptável.</span><span class="sxs-lookup"><span data-stu-id="e7b71-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b71-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b71-136">Requirements</span></span>



| <span data-ttu-id="e7b71-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b71-137">Requirement</span></span> | <span data-ttu-id="e7b71-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e7b71-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b71-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7b71-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b71-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b71-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b71-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7b71-141">Library</span></span><br/> | <dl> <span data-ttu-id="e7b71-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7b71-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7b71-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7b71-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b71-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="e7b71-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
