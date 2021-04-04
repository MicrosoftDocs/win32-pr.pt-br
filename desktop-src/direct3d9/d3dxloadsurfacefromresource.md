---
description: Carrega uma superfície de um recurso.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: Função D3DXLoadSurfaceFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930544"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="4cfb8-103">Função D3DXLoadSurfaceFromResource</span><span class="sxs-lookup"><span data-stu-id="4cfb8-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="4cfb8-104">Carrega uma superfície de um recurso.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfb8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cfb8-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4cfb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cfb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfb8-107">*pDestSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="4cfb8-109">Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="4cfb8-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="4cfb8-110">Especifica a superfície de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4cfb8-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4cfb8-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-114">*pDestRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4cfb8-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4cfb8-116">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4cfb8-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4cfb8-117">Especifica o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="4cfb8-118">Defina esse parâmetro como **NULL** para especificar a superfície inteira.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-119">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-120">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cfb8-121">Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-122">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-123">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cfb8-124">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="4cfb8-125">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4cfb8-126">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4cfb8-127">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-128">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-129">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4cfb8-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4cfb8-130">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4cfb8-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4cfb8-131">Especifica o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-131">Specifies the source rectangle.</span></span> <span data-ttu-id="4cfb8-132">Defina esse parâmetro como **NULL** para especificar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-133">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cfb8-135">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4cfb8-136">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4cfb8-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-137">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-138">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4cfb8-139">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4cfb8-140">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4cfb8-141">Alfa é significativo e normalmente deve ser definido como FF para chaves de cores opacas, portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb8-142">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4cfb8-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb8-143">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfb8-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4cfb8-144">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfb8-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cfb8-145">Return value</span></span>

<span data-ttu-id="4cfb8-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cfb8-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cfb8-147">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4cfb8-148">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfb8-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cfb8-149">Remarks</span></span>

<span data-ttu-id="4cfb8-150">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4cfb8-151">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadSurfaceFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="4cfb8-152">Caso contrário, a chamada de função é resolvida como D3DXLoadSurfaceFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="4cfb8-153">O recurso que está sendo carregado deve ser do tipo \_ bitmap RT ou RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="4cfb8-154">O tipo de recurso RT \_ RCDATA é usado para carregar formatos diferentes de bitmaps (como. tga,. jpg e. DDS).</span><span class="sxs-lookup"><span data-stu-id="4cfb8-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="4cfb8-155">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="4cfb8-156">Gravar em uma superfície de não nível zero não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="4cfb8-157">Se [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na superfície.</span><span class="sxs-lookup"><span data-stu-id="4cfb8-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfb8-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cfb8-158">Requirements</span></span>



| <span data-ttu-id="4cfb8-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfb8-159">Requirement</span></span> | <span data-ttu-id="4cfb8-160">Valor</span><span class="sxs-lookup"><span data-stu-id="4cfb8-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfb8-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cfb8-161">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfb8-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb8-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4cfb8-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cfb8-163">Library</span></span><br/> | <dl> <span data-ttu-id="4cfb8-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb8-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4cfb8-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cfb8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfb8-166">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4cfb8-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
