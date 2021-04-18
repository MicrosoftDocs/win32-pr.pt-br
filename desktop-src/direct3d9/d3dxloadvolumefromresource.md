---
description: Carrega um volume de um recurso.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Função D3DXLoadVolumeFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760643"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="3a566-103">Função D3DXLoadVolumeFromResource</span><span class="sxs-lookup"><span data-stu-id="3a566-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="3a566-104">Carrega um volume de um recurso.</span><span class="sxs-lookup"><span data-stu-id="3a566-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a566-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a566-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3a566-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a566-107">*pDestVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="3a566-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="3a566-109">Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="3a566-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="3a566-110">Especifica o volume de destino.</span><span class="sxs-lookup"><span data-stu-id="3a566-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="3a566-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="3a566-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3a566-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-114">*pDestBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a566-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="3a566-116">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="3a566-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="3a566-117">Especifica a caixa de destino.</span><span class="sxs-lookup"><span data-stu-id="3a566-117">Specifies the destination box.</span></span> <span data-ttu-id="3a566-118">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="3a566-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-119">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-120">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a566-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a566-121">Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="3a566-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-122">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a566-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a566-124">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="3a566-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="3a566-125">Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3a566-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-126">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a566-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="3a566-128">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="3a566-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="3a566-129">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="3a566-129">Specifies the source box.</span></span> <span data-ttu-id="3a566-130">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="3a566-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-131">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a566-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a566-133">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="3a566-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="3a566-134">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3a566-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-135">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3a566-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3a566-137">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="3a566-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="3a566-138">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="3a566-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="3a566-139">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="3a566-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="3a566-140">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="3a566-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="3a566-141">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a566-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a566-142">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a566-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="3a566-143">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3a566-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a566-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a566-144">Return value</span></span>

<span data-ttu-id="3a566-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a566-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a566-146">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a566-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a566-147">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="3a566-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a566-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a566-148">Remarks</span></span>

<span data-ttu-id="3a566-149">O recurso que está sendo carregado deve ser um recurso de bitmap ( \_ bitmap RT).</span><span class="sxs-lookup"><span data-stu-id="3a566-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="3a566-150">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="3a566-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="3a566-151">Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="3a566-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="3a566-152">Se [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) for chamado e a textura ainda não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na textura do volume.</span><span class="sxs-lookup"><span data-stu-id="3a566-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="3a566-153">Essa função dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="3a566-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a566-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a566-154">Requirements</span></span>



| <span data-ttu-id="3a566-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a566-155">Requirement</span></span> | <span data-ttu-id="3a566-156">Valor</span><span class="sxs-lookup"><span data-stu-id="3a566-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a566-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a566-157">Header</span></span><br/>  | <dl> <span data-ttu-id="3a566-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a566-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3a566-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a566-159">Library</span></span><br/> | <dl> <span data-ttu-id="3a566-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a566-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3a566-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a566-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a566-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="3a566-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="3a566-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3a566-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="3a566-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="3a566-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="3a566-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="3a566-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="3a566-166">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="3a566-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
