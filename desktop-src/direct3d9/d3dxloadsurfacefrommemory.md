---
description: Carrega uma superfície da memória.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Função D3DXLoadSurfaceFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012076"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="ceacd-103">Função D3DXLoadSurfaceFromMemory</span><span class="sxs-lookup"><span data-stu-id="ceacd-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="ceacd-104">Carrega uma superfície da memória.</span><span class="sxs-lookup"><span data-stu-id="ceacd-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceacd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceacd-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="ceacd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ceacd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceacd-107">*pDestSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="ceacd-109">Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="ceacd-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="ceacd-110">Especifica a superfície de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="ceacd-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ceacd-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ceacd-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ceacd-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-114">*pDestRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ceacd-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ceacd-116">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ceacd-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ceacd-117">Especifica o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="ceacd-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="ceacd-118">Defina esse parâmetro como **NULL** para especificar a superfície inteira.</span><span class="sxs-lookup"><span data-stu-id="ceacd-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-119">*pSrcMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceacd-121">Ponteiro para o canto superior esquerdo da imagem de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="ceacd-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-122">*SrcFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ceacd-124">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , o formato de pixel da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="ceacd-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-125">*SrcPitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceacd-127">Densidade da imagem de origem, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceacd-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="ceacd-128">Para formatos DXT, esse número deve representar a largura de uma linha de células, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceacd-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-129">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-130">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ceacd-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ceacd-131">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de origem de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ceacd-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-132">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-133">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ceacd-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ceacd-134">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ceacd-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ceacd-135">Especifica as dimensões da imagem de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="ceacd-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="ceacd-136">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ceacd-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-137">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceacd-139">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="ceacd-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ceacd-140">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ceacd-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ceacd-141">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceacd-142">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ceacd-143">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="ceacd-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ceacd-144">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="ceacd-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ceacd-145">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="ceacd-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ceacd-146">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ceacd-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceacd-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ceacd-147">Return value</span></span>

<span data-ttu-id="ceacd-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ceacd-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ceacd-149">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ceacd-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ceacd-150">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ceacd-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceacd-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceacd-151">Remarks</span></span>

<span data-ttu-id="ceacd-152">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="ceacd-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="ceacd-153">Gravar em uma superfície de não nível zero não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="ceacd-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ceacd-154">Se **D3DXLoadSurfaceFromMemory** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na superfície.</span><span class="sxs-lookup"><span data-stu-id="ceacd-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceacd-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceacd-155">Requirements</span></span>



| <span data-ttu-id="ceacd-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceacd-156">Requirement</span></span> | <span data-ttu-id="ceacd-157">Valor</span><span class="sxs-lookup"><span data-stu-id="ceacd-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceacd-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ceacd-158">Header</span></span><br/>  | <dl> <span data-ttu-id="ceacd-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceacd-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ceacd-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ceacd-160">Library</span></span><br/> | <dl> <span data-ttu-id="ceacd-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ceacd-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ceacd-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceacd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceacd-163">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ceacd-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
