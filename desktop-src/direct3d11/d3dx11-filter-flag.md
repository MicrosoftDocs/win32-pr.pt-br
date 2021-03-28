---
title: Enumeração de D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Sinalizadores de filtragem de textura.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Enumeração D3DX11_FILTER_FLAG Direct3D 11
- Ponteiro de enumeração LPD3DX11_FILTER_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968697"
---
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="da1c2-106">Enumeração de sinalizador de \_ filtro D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="da1c2-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="da1c2-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="da1c2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="da1c2-108">Sinalizadores de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="da1c2-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1c2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="da1c2-109">Syntax</span></span>


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="da1c2-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="da1c2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da1c2-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**Filtro de D3DX11 \_ \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="da1c2-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-112">Nenhum dimensionamento ou filtragem ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="da1c2-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="da1c2-113">Os pixels fora dos limites da imagem de origem são considerados pretos transparentes.</span><span class="sxs-lookup"><span data-stu-id="da1c2-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Ponto de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-115">Cada pixel de destino é computado por amostragem do pixel mais próximo da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="da1c2-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ filtro \_ linear**</span><span class="sxs-lookup"><span data-stu-id="da1c2-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-117">Cada pixel de destino é computado por amostragem dos quatro pixels mais próximos da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="da1c2-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="da1c2-118">Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.</span><span class="sxs-lookup"><span data-stu-id="da1c2-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triângulo de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-120">Cada pixel na imagem de origem contribui igualmente para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="da1c2-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="da1c2-121">Esse é o mais lento dos filtros.</span><span class="sxs-lookup"><span data-stu-id="da1c2-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Caixa de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-123">Cada pixel é calculado pela média de uma caixa de pixels 2x2 (x2) da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="da1c2-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="da1c2-124">Esse filtro funciona somente quando as dimensões do destino são metades da origem, como é o caso com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="da1c2-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Espelho do filtro D3DX11 \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="da1c2-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-126">Os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="da1c2-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**Espelho de filtro do D3DX11 \_ \_ \_ V**</span><span class="sxs-lookup"><span data-stu-id="da1c2-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-128">Os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="da1c2-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Espelho de filtro D3DX11 \_ \_ W**</span><span class="sxs-lookup"><span data-stu-id="da1c2-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-130">Os pixels da borda da textura no eixo w devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="da1c2-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Espelho de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-132">A especificação desse sinalizador é a mesma que especificar o D3DX do espelho do filtro do D3DX filtro do \_ \_ espelho V e do filtro do D3DX para \_ \_ \_ \_ \_ \_ espelhar os \_ sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="da1c2-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Pontilhamento de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-134">A imagem resultante deve ser dificada usando um algoritmo de pontilhamento 4x4 ordenado.</span><span class="sxs-lookup"><span data-stu-id="da1c2-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="da1c2-135">Isso acontece ao converter de um formato para outro.</span><span class="sxs-lookup"><span data-stu-id="da1c2-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_Difusão de \_ pontilhamento de filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="da1c2-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-137">Faça o pontilhado difuso na imagem ao alterar de um formato para outro.</span><span class="sxs-lookup"><span data-stu-id="da1c2-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ Filtrar \_ sRGB \_ em**</span><span class="sxs-lookup"><span data-stu-id="da1c2-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-139">Os dados de entrada estão no espaço de cores RGB padrão (sRGB).</span><span class="sxs-lookup"><span data-stu-id="da1c2-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="da1c2-140">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="da1c2-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtro \_ sRGB \_ out**</span><span class="sxs-lookup"><span data-stu-id="da1c2-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-142">Os dados de saída estão no espaço de cores RGB padrão (sRGB).</span><span class="sxs-lookup"><span data-stu-id="da1c2-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="da1c2-143">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="da1c2-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da1c2-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ filtro \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="da1c2-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="da1c2-145">O mesmo que especificar D3DX \_ Filter \_ sRGB \_ no \| D3DX \_ Filter \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="da1c2-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="da1c2-146">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="da1c2-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da1c2-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="da1c2-147">Remarks</span></span>

<span data-ttu-id="da1c2-148">O D3DX11 executa automaticamente a correção de gama (para converter dados de cores de espaço RGB em espaço RGB padrão) ao carregar dados de textura.</span><span class="sxs-lookup"><span data-stu-id="da1c2-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="da1c2-149">Isso é feito automaticamente por instância quando dados RGB são carregados de um arquivo. png em uma textura sRGB.</span><span class="sxs-lookup"><span data-stu-id="da1c2-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="da1c2-150">Use os sinalizadores de filtro SRGB para indicar se os dados não precisam ser convertidos em espaço sRGB.</span><span class="sxs-lookup"><span data-stu-id="da1c2-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1c2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1c2-151">Requirements</span></span>



| <span data-ttu-id="da1c2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1c2-152">Requirement</span></span> | <span data-ttu-id="da1c2-153">Valor</span><span class="sxs-lookup"><span data-stu-id="da1c2-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da1c2-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da1c2-154">Header</span></span><br/> | <dl> <span data-ttu-id="da1c2-155"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="da1c2-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1c2-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="da1c2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1c2-157">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="da1c2-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





