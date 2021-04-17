---
description: Carrega um volume da memória.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Função D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762389"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="59074-103">Função D3DXLoadVolumeFromMemory</span><span class="sxs-lookup"><span data-stu-id="59074-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="59074-104">Carrega um volume da memória.</span><span class="sxs-lookup"><span data-stu-id="59074-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="59074-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59074-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="59074-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59074-107">*pDestVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="59074-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="59074-109">Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="59074-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="59074-110">Especifica o volume de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="59074-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="59074-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="59074-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="59074-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="59074-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59074-114">*pDestBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="59074-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="59074-116">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="59074-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="59074-117">Especifica a caixa de destino.</span><span class="sxs-lookup"><span data-stu-id="59074-117">Specifies the destination box.</span></span> <span data-ttu-id="59074-118">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="59074-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="59074-119">*pSrcMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59074-121">Ponteiro para o canto superior esquerdo do volume de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="59074-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="59074-122">*SrcFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="59074-124">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , o formato de pixel do volume de origem.</span><span class="sxs-lookup"><span data-stu-id="59074-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="59074-125">*SrcRowPitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59074-127">Densidade da imagem de origem, em bytes.</span><span class="sxs-lookup"><span data-stu-id="59074-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="59074-128">Para formatos DXT (formatos de textura compactados), esse número deve representar o tamanho de uma linha de células, em bytes.</span><span class="sxs-lookup"><span data-stu-id="59074-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="59074-129">*SrcSlicePitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59074-131">Densidade da imagem de origem, em bytes.</span><span class="sxs-lookup"><span data-stu-id="59074-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="59074-132">Para formatos DXT (formatos de textura compactados), esse número deve representar o tamanho de uma fatia de células, em bytes.</span><span class="sxs-lookup"><span data-stu-id="59074-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="59074-133">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-134">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="59074-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="59074-135">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de origem de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="59074-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59074-136">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-137">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="59074-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="59074-138">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="59074-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="59074-139">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="59074-139">Specifies the source box.</span></span> <span data-ttu-id="59074-140">**NULL** não é um valor válido para este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="59074-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="59074-141">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-142">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59074-143">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="59074-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="59074-144">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="59074-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="59074-145">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59074-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59074-146">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="59074-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="59074-147">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="59074-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="59074-148">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="59074-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="59074-149">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="59074-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="59074-150">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="59074-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59074-151">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59074-151">Return value</span></span>

<span data-ttu-id="59074-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59074-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59074-153">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59074-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="59074-154">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="59074-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="59074-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="59074-155">Remarks</span></span>

<span data-ttu-id="59074-156">Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="59074-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="59074-157">Se **D3DXLoadVolumeFromMemory** for chamado e a textura ainda não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na textura do volume.</span><span class="sxs-lookup"><span data-stu-id="59074-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="59074-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59074-158">Requirements</span></span>



| <span data-ttu-id="59074-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="59074-159">Requirement</span></span> | <span data-ttu-id="59074-160">Valor</span><span class="sxs-lookup"><span data-stu-id="59074-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59074-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59074-161">Header</span></span><br/>  | <dl> <span data-ttu-id="59074-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="59074-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="59074-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59074-163">Library</span></span><br/> | <dl> <span data-ttu-id="59074-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59074-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="59074-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="59074-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59074-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="59074-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="59074-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="59074-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="59074-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="59074-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="59074-169">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="59074-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
