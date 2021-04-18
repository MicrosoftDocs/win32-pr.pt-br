---
description: Carrega um volume de um arquivo.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: Função D3DXLoadVolumeFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764495"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="accc4-103">Função D3DXLoadVolumeFromFile</span><span class="sxs-lookup"><span data-stu-id="accc4-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="accc4-104">Carrega um volume de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="accc4-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="accc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="accc4-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="accc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="accc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accc4-107">*pDestVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="accc4-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="accc4-109">Ponteiro para uma interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="accc4-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="accc4-110">Especifica o volume de destino.</span><span class="sxs-lookup"><span data-stu-id="accc4-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="accc4-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="accc4-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="accc4-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-114">*pDestBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="accc4-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="accc4-116">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="accc4-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="accc4-117">Especifica a caixa de destino.</span><span class="sxs-lookup"><span data-stu-id="accc4-117">Specifies the destination box.</span></span> <span data-ttu-id="accc4-118">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="accc4-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-119">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="accc4-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="accc4-121">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="accc4-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="accc4-122">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="accc4-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="accc4-123">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="accc4-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="accc4-124">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="accc4-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-125">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-126">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="accc4-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="accc4-127">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="accc4-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="accc4-128">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="accc4-128">Specifies the source box.</span></span> <span data-ttu-id="accc4-129">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="accc4-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-130">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="accc4-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="accc4-132">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="accc4-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="accc4-133">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="accc4-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-134">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="accc4-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="accc4-136">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="accc4-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="accc4-137">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="accc4-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="accc4-138">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="accc4-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="accc4-139">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="accc4-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="accc4-140">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="accc4-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc4-141">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="accc4-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="accc4-142">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="accc4-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accc4-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="accc4-143">Return value</span></span>

<span data-ttu-id="accc4-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="accc4-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="accc4-145">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="accc4-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="accc4-146">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="accc4-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="accc4-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="accc4-147">Remarks</span></span>

<span data-ttu-id="accc4-148">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="accc4-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="accc4-149">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadVolumeFromFileW.</span><span class="sxs-lookup"><span data-stu-id="accc4-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="accc4-150">Caso contrário, a chamada de função é resolvida como D3DXLoadVolumeFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="accc4-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="accc4-151">Essa função manipula a conversão de e para formatos de textura compactados e oferece suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="accc4-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="accc4-152">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="accc4-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="accc4-153">Gravar em uma superfície de não nível zero da textura do volume não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="accc4-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="accc4-154">Se **D3DXLoadVolumeFromFile** for chamado e a textura ainda não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar explicitamente [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) na textura do volume.</span><span class="sxs-lookup"><span data-stu-id="accc4-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="accc4-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accc4-155">Requirements</span></span>



| <span data-ttu-id="accc4-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="accc4-156">Requirement</span></span> | <span data-ttu-id="accc4-157">Valor</span><span class="sxs-lookup"><span data-stu-id="accc4-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="accc4-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="accc4-158">Header</span></span><br/>  | <dl> <span data-ttu-id="accc4-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="accc4-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="accc4-160">Library</span></span><br/> | <dl> <span data-ttu-id="accc4-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="accc4-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="accc4-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accc4-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="accc4-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="accc4-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="accc4-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="accc4-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="accc4-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="accc4-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="accc4-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="accc4-167">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="accc4-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
