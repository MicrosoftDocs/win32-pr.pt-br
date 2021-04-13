---
description: Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456521"
---
# <a name="d3dx_filter"></a><span data-ttu-id="5a94b-103">Filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-103">D3DX\_FILTER</span></span>

<span data-ttu-id="5a94b-104">Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.</span><span class="sxs-lookup"><span data-stu-id="5a94b-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a94b-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="5a94b-105">\#define</span></span>                | <span data-ttu-id="5a94b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a94b-106">Description</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="5a94b-107">Filtro de D3DX \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="5a94b-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="5a94b-108">Nenhum dimensionamento ou filtragem ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="5a94b-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="5a94b-109">Os pixels fora dos limites da imagem de origem são considerados pretos transparentes.</span><span class="sxs-lookup"><span data-stu-id="5a94b-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="5a94b-110">\_Ponto de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="5a94b-111">Cada pixel de destino é computado por amostragem do pixel mais próximo da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5a94b-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="5a94b-112">D3DX \_ filtro \_ linear</span><span class="sxs-lookup"><span data-stu-id="5a94b-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="5a94b-113">Cada pixel de destino é computado por amostragem dos quatro pixels mais próximos da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5a94b-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="5a94b-114">Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.</span><span class="sxs-lookup"><span data-stu-id="5a94b-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="5a94b-115">\_Triângulo de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="5a94b-116">Cada pixel na imagem de origem contribui igualmente para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="5a94b-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="5a94b-117">Esse é o mais lento dos filtros.</span><span class="sxs-lookup"><span data-stu-id="5a94b-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="5a94b-118">\_Caixa de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="5a94b-119">Cada pixel é calculado pela média de uma caixa de pixels 2x2 (x2) da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5a94b-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="5a94b-120">Esse filtro funciona somente quando as dimensões do destino são metades da origem, como é o caso com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="5a94b-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="5a94b-121">\_Espelho do filtro D3DX \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="5a94b-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="5a94b-122">Os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="5a94b-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="5a94b-123">Espelho de filtro do D3DX \_ \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="5a94b-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="5a94b-124">Os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="5a94b-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="5a94b-125">\_Espelho de filtro D3DX \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="5a94b-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="5a94b-126">Os pixels da borda da textura no eixo w devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="5a94b-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="5a94b-127">\_Espelho de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="5a94b-128">A especificação desse sinalizador é a mesma que especificar o D3DX do espelho do filtro do D3DX filtro do \_ \_ espelho V e do filtro do D3DX para \_ \_ \_ \_ \_ \_ espelhar os \_ sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="5a94b-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="5a94b-129">\_Pontilhamento de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="5a94b-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="5a94b-130">A imagem resultante deve ser dificada usando um algoritmo de pontilhamento 4x4 ordenado.</span><span class="sxs-lookup"><span data-stu-id="5a94b-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="5a94b-131">D3DX \_ Filtrar \_ sRGB \_ em</span><span class="sxs-lookup"><span data-stu-id="5a94b-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="5a94b-132">Os dados de entrada estão no espaço de cores sRGB (gama 2,2).</span><span class="sxs-lookup"><span data-stu-id="5a94b-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="5a94b-133">D3DX \_ filtro \_ sRGB \_ out</span><span class="sxs-lookup"><span data-stu-id="5a94b-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="5a94b-134">Os dados de saída estão no espaço de cores sRGB (gama 2,2).</span><span class="sxs-lookup"><span data-stu-id="5a94b-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="5a94b-135">D3DX \_ filtro \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="5a94b-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="5a94b-136">O mesmo que especificar D3DX \_ Filter \_ sRGB \_ no \| D3DX \_ Filter \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="5a94b-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="5a94b-137">Cada filtro válido deve conter exatamente um dos seguintes sinalizadores: filtro D3DX \_ \_ nenhum, ponto de \_ filtro D3DX \_ , filtro de D3DX \_ \_ linear, \_ triângulo de filtro de D3DX \_ ou caixa de \_ filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="5a94b-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="5a94b-138">Além disso, você pode usar o operador OR para especificar zero ou mais dos seguintes sinalizadores opcionais com um filtro válido: D3DX \_ filtro \_ espelho \_ U, D3DX \_ filtro \_ espelho \_ V, D3DX \_ filtro \_ espelho \_ W, D3DX \_ filtro \_ espelho, D3DX \_ Filter \_ pontilhado, D3DX \_ Filter \_ sRGB \_ in, D3DX filtro \_ \_ sRGB \_ out ou D3DX \_ Filter \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="5a94b-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="5a94b-139">A especificação do \_ padrão D3DX para esse parâmetro é geralmente o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5a94b-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="5a94b-140">No entanto, o \_ padrão D3DX pode ter significados diferentes, dependendo de qual método usa o filtro.</span><span class="sxs-lookup"><span data-stu-id="5a94b-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="5a94b-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5a94b-141">For example:</span></span>

-   <span data-ttu-id="5a94b-142">Ao usar [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), o \_ padrão de D3DX é MAPEADO para o D3DX de \_ filtro D3DX de filtro do triângulo de filtragem \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5a94b-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="5a94b-143">Ao usar [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ o padrão de D3DX é mapeado para a \_ \_ caixa de filtro D3DX se o tamanho da textura for uma potência de dois e a \_ caixa de filtro D3DX D3DX o \_ \| \_ pontilhado de filtro de \_ outra forma.</span><span class="sxs-lookup"><span data-stu-id="5a94b-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="5a94b-144">Referencie cada método para verificar se há informações sobre como o \_ filtro padrão D3DX é mapeado.</span><span class="sxs-lookup"><span data-stu-id="5a94b-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="5a94b-145">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="5a94b-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="5a94b-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a94b-146">Header</span></span>                   | <span data-ttu-id="5a94b-147">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="5a94b-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="5a94b-148">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="5a94b-148">Minimum operating system</span></span> | <span data-ttu-id="5a94b-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="5a94b-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5a94b-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a94b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a94b-151">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="5a94b-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



