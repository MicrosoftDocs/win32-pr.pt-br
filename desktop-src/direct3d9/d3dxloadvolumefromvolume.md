---
description: Carrega um volume de outro volume.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: Função D3DXLoadVolumeFromVolume (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930688"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="7ded3-103">Função D3DXLoadVolumeFromVolume</span><span class="sxs-lookup"><span data-stu-id="7ded3-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="7ded3-104">Carrega um volume de outro volume.</span><span class="sxs-lookup"><span data-stu-id="7ded3-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ded3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ded3-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="7ded3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ded3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ded3-107">*pDestVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="7ded3-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="7ded3-109">Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="7ded3-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="7ded3-110">Especifica o volume de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="7ded3-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="7ded3-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7ded3-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7ded3-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-114">*pDestBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ded3-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="7ded3-116">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="7ded3-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="7ded3-117">Especifica a caixa de destino.</span><span class="sxs-lookup"><span data-stu-id="7ded3-117">Specifies the destination box.</span></span> <span data-ttu-id="7ded3-118">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="7ded3-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-119">*pSrcVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-120">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="7ded3-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="7ded3-121">Um ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="7ded3-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="7ded3-122">Especifica o volume de origem.</span><span class="sxs-lookup"><span data-stu-id="7ded3-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-123">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-124">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="7ded3-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7ded3-125">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de origem de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7ded3-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-126">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ded3-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="7ded3-128">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="7ded3-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="7ded3-129">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="7ded3-129">Specifies the source box.</span></span> <span data-ttu-id="7ded3-130">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="7ded3-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-131">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ded3-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ded3-133">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="7ded3-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="7ded3-134">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7ded3-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7ded3-135">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ded3-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ded3-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7ded3-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7ded3-137">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="7ded3-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7ded3-138">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="7ded3-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7ded3-139">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="7ded3-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7ded3-140">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="7ded3-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ded3-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ded3-141">Return value</span></span>

<span data-ttu-id="7ded3-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ded3-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ded3-143">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ded3-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ded3-144">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="7ded3-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ded3-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ded3-145">Remarks</span></span>

<span data-ttu-id="7ded3-146">Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="7ded3-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="7ded3-147">Se **D3DXLoadVolumeFromVolume** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na superfície.</span><span class="sxs-lookup"><span data-stu-id="7ded3-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ded3-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ded3-148">Requirements</span></span>



| <span data-ttu-id="7ded3-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ded3-149">Requirement</span></span> | <span data-ttu-id="7ded3-150">Valor</span><span class="sxs-lookup"><span data-stu-id="7ded3-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ded3-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ded3-151">Header</span></span><br/>  | <dl> <span data-ttu-id="7ded3-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ded3-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7ded3-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ded3-153">Library</span></span><br/> | <dl> <span data-ttu-id="7ded3-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ded3-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7ded3-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ded3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ded3-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="7ded3-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="7ded3-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7ded3-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="7ded3-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="7ded3-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="7ded3-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="7ded3-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="7ded3-160">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7ded3-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
