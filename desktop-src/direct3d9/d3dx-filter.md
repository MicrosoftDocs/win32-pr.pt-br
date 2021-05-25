---
description: Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83fd0b3e12d6b5bccb13f9c5fab5e078587dbd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342861"
---
# <a name="d3dx_filter"></a><span data-ttu-id="828ca-103">Filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="828ca-103">D3DX\_FILTER</span></span>

<span data-ttu-id="828ca-104">Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.</span><span class="sxs-lookup"><span data-stu-id="828ca-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="828ca-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="828ca-105">\#define</span></span>                | <span data-ttu-id="828ca-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="828ca-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828ca-107">Filtro de D3DX \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="828ca-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="828ca-108">Nenhum dimensionamento ou filtragem ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="828ca-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="828ca-109">Os pixels fora dos limites da imagem de origem são considerados pretos transparentes.</span><span class="sxs-lookup"><span data-stu-id="828ca-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="828ca-110">\_Ponto de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="828ca-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="828ca-111">Cada pixel de destino é computado por amostragem do pixel mais próximo da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="828ca-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="828ca-112">D3DX \_ filtro \_ linear</span><span class="sxs-lookup"><span data-stu-id="828ca-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="828ca-113">Cada pixel de destino é computado por amostragem dos quatro pixels mais próximos da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="828ca-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="828ca-114">Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.</span><span class="sxs-lookup"><span data-stu-id="828ca-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="828ca-115">\_Triângulo de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="828ca-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="828ca-116">Cada pixel na imagem de origem contribui igualmente para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="828ca-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="828ca-117">Esse é o mais lento dos filtros.</span><span class="sxs-lookup"><span data-stu-id="828ca-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="828ca-118">\_Caixa de filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="828ca-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="828ca-119">Cada pixel é calculado pela média de uma caixa de pixels 2x2 (x2) da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="828ca-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="828ca-120">Esse filtro funciona somente quando as dimensões do destino são metades da origem, como é o caso com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="828ca-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="828ca-121">\_Espelho do filtro D3DX \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="828ca-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="828ca-122">Pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.</span><span class="sxs-lookup"><span data-stu-id="828ca-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="828ca-123">ESPELHO DE FILTRO D3DX \_ \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="828ca-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="828ca-124">Os pixels da borda da textura no eixo v devem ser espelhados, não empacotados.</span><span class="sxs-lookup"><span data-stu-id="828ca-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="828ca-125">D3DX \_ FILTER \_ MIRROR \_ W</span><span class="sxs-lookup"><span data-stu-id="828ca-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="828ca-126">Pixels fora da borda da textura no eixo w devem ser espelhados, não empacotados.</span><span class="sxs-lookup"><span data-stu-id="828ca-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="828ca-127">ESPELHO DE FILTRO D3DX \_ \_</span><span class="sxs-lookup"><span data-stu-id="828ca-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="828ca-128">Especificar esse sinalizador é o mesmo que especificar os sinalizadores D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.</span><span class="sxs-lookup"><span data-stu-id="828ca-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="828ca-129">DITHER DE FILTRO \_ \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="828ca-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="828ca-130">A imagem resultante deve ser dithered usando um algoritmo dither ordenado 4x4.</span><span class="sxs-lookup"><span data-stu-id="828ca-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="828ca-131">FILTRO D3DX \_ \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="828ca-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="828ca-132">Os dados de entrada estão no espaço de cores sRGB (gama 2.2).</span><span class="sxs-lookup"><span data-stu-id="828ca-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="828ca-133">FILTRO D3DX \_ \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="828ca-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="828ca-134">Os dados de saída estão no espaço de cores sRGB (gama 2.2).</span><span class="sxs-lookup"><span data-stu-id="828ca-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="828ca-135">FILTRO D3DX \_ \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="828ca-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="828ca-136">O mesmo que especificar SRGB DE FILTRO D3DX \_ \_ EM FILTRO \_ \| D3DX \_ \_ SRGB \_ OUT.</span><span class="sxs-lookup"><span data-stu-id="828ca-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="828ca-137">Cada filtro válido deve conter exatamente um dos seguintes sinalizadores: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE ou \_ \_ D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="828ca-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="828ca-138">Além disso, você pode usar o operador OR para especificar zero ou mais dos seguintes sinalizadores opcionais com um filtro válido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT ou \_ \_ \_ D3DX \_ FILTER \_ SRGB.</span><span class="sxs-lookup"><span data-stu-id="828ca-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="828ca-139">Especificar D3DX DEFAULT para esse parâmetro geralmente é o equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="828ca-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="828ca-140">No entanto, D3DX \_ DEFAULT pode ter significados diferentes, dependendo de qual método usa o filtro.</span><span class="sxs-lookup"><span data-stu-id="828ca-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="828ca-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="828ca-141">For example:</span></span>

-   <span data-ttu-id="828ca-142">Ao usar [**D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT mapeia para \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="828ca-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="828ca-143">Ao usar [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ o padrão de D3DX é mapeado para a \_ \_ caixa de filtro D3DX se o tamanho da textura for uma potência de dois e a \_ caixa de filtro D3DX D3DX o \_ \| \_ pontilhado de filtro de \_ outra forma.</span><span class="sxs-lookup"><span data-stu-id="828ca-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="828ca-144">Referencie cada método para verificar se há informações sobre como o \_ filtro padrão D3DX é mapeado.</span><span class="sxs-lookup"><span data-stu-id="828ca-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="828ca-145">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="828ca-145">Constant Information</span></span>



| <span data-ttu-id="828ca-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="828ca-146">Requirement</span></span>                         | <span data-ttu-id="828ca-147">Valor</span><span class="sxs-lookup"><span data-stu-id="828ca-147">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="828ca-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="828ca-148">Header</span></span>                   | <span data-ttu-id="828ca-149">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="828ca-149">d3dx9tex.h</span></span> |
| <span data-ttu-id="828ca-150">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="828ca-150">Minimum operating system</span></span> | <span data-ttu-id="828ca-151">Windows 98</span><span class="sxs-lookup"><span data-stu-id="828ca-151">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="828ca-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="828ca-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="828ca-153">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="828ca-153">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



