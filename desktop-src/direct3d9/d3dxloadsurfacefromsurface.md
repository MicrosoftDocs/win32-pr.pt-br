---
description: Carrega uma superfície de outra superfície com conversão de cores.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: Função D3DXLoadSurfaceFromSurface (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664051"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="396df-103">Função D3DXLoadSurfaceFromSurface</span><span class="sxs-lookup"><span data-stu-id="396df-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="396df-104">Carrega uma superfície de outra superfície com conversão de cores.</span><span class="sxs-lookup"><span data-stu-id="396df-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="396df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="396df-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="396df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="396df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396df-107">*pDestSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="396df-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="396df-109">Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="396df-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="396df-110">Especifica a superfície de destino, que recebe a imagem.</span><span class="sxs-lookup"><span data-stu-id="396df-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="396df-111">*pDestPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="396df-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="396df-113">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de destino de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="396df-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="396df-114">*pDestRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="396df-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="396df-116">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="396df-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="396df-117">Especifica o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="396df-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="396df-118">Defina esse parâmetro como **NULL** para especificar a superfície inteira.</span><span class="sxs-lookup"><span data-stu-id="396df-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="396df-119">*pSrcSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-120">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="396df-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="396df-121">Ponteiro para uma interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , representando a superfície de origem.</span><span class="sxs-lookup"><span data-stu-id="396df-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="396df-122">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-123">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="396df-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="396df-124">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , a paleta de origem de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="396df-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="396df-125">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="396df-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="396df-127">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="396df-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="396df-128">Especifica o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="396df-128">Specifies the source rectangle.</span></span> <span data-ttu-id="396df-129">Defina esse parâmetro como **NULL** para especificar a superfície inteira.</span><span class="sxs-lookup"><span data-stu-id="396df-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="396df-130">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="396df-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="396df-132">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="396df-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="396df-133">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="396df-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="396df-134">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="396df-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396df-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="396df-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="396df-136">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="396df-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="396df-137">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="396df-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="396df-138">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="396df-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="396df-139">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="396df-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396df-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="396df-140">Return value</span></span>

<span data-ttu-id="396df-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="396df-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="396df-142">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="396df-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="396df-143">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="396df-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="396df-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="396df-144">Remarks</span></span>

<span data-ttu-id="396df-145">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="396df-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="396df-146">Gravar em uma superfície de não nível zero não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="396df-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="396df-147">Se **D3DXLoadSurfaceFromSurface** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na superfície.</span><span class="sxs-lookup"><span data-stu-id="396df-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="396df-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="396df-148">Requirements</span></span>



| <span data-ttu-id="396df-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="396df-149">Requirement</span></span> | <span data-ttu-id="396df-150">Valor</span><span class="sxs-lookup"><span data-stu-id="396df-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="396df-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="396df-151">Header</span></span><br/>  | <dl> <span data-ttu-id="396df-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="396df-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="396df-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="396df-153">Library</span></span><br/> | <dl> <span data-ttu-id="396df-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="396df-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="396df-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="396df-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396df-156">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="396df-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
