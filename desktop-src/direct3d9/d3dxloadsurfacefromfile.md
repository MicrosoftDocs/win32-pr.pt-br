---
description: Carrega uma superfície de um arquivo.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Função D3DXLoadSurfaceFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664101"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="8526b-103">Função D3DXLoadSurfaceFromFile</span><span class="sxs-lookup"><span data-stu-id="8526b-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="8526b-104">Carrega uma superfície de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8526b-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8526b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8526b-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8526b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8526b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8526b-107">*pDestSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="8526b-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="8526b-109">Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="8526b-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="8526b-110">Especifica a superfície de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="8526b-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8526b-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8526b-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8526b-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-114">*pDestRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="8526b-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="8526b-116">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8526b-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8526b-117">Especifica o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="8526b-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="8526b-118">Defina esse parâmetro como **NULL** para especificar a superfície inteira.</span><span class="sxs-lookup"><span data-stu-id="8526b-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-119">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8526b-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8526b-121">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8526b-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="8526b-122">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8526b-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8526b-123">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8526b-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="8526b-124">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="8526b-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-125">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="8526b-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="8526b-127">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8526b-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8526b-128">Especifica o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="8526b-128">Specifies the source rectangle.</span></span> <span data-ttu-id="8526b-129">Defina esse parâmetro como **NULL** para especificar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="8526b-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-130">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8526b-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8526b-132">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="8526b-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="8526b-133">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8526b-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-134">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8526b-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="8526b-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="8526b-136">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="8526b-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="8526b-137">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="8526b-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="8526b-138">Alfa é significativo e normalmente deve ser definido como FF para chaves de cores opacas, portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="8526b-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="8526b-139">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8526b-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8526b-140">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8526b-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="8526b-141">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8526b-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8526b-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8526b-142">Return value</span></span>

<span data-ttu-id="8526b-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8526b-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8526b-144">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8526b-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8526b-145">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8526b-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8526b-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="8526b-146">Remarks</span></span>

<span data-ttu-id="8526b-147">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="8526b-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8526b-148">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadSurfaceFromFileW.</span><span class="sxs-lookup"><span data-stu-id="8526b-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="8526b-149">Caso contrário, a chamada de função é resolvida como D3DXLoadSurfaceFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="8526b-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="8526b-150">Essa função manipula a conversão de e para formatos de textura compactados e oferece suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="8526b-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="8526b-151">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="8526b-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="8526b-152">Gravar em uma superfície de não nível zero não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="8526b-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="8526b-153">Se **D3DXLoadSurfaceFromFile** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na superfície.</span><span class="sxs-lookup"><span data-stu-id="8526b-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8526b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8526b-154">Requirements</span></span>



| <span data-ttu-id="8526b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="8526b-155">Requirement</span></span> | <span data-ttu-id="8526b-156">Valor</span><span class="sxs-lookup"><span data-stu-id="8526b-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8526b-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8526b-157">Header</span></span><br/>  | <dl> <span data-ttu-id="8526b-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8526b-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8526b-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8526b-159">Library</span></span><br/> | <dl> <span data-ttu-id="8526b-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8526b-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8526b-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="8526b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8526b-162">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8526b-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
