---
title: Efeito da matriz de cores
description: Use o efeito de matriz de cores para alterar os valores de RGBA de um bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efeito da matriz de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009244"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="d6f79-104">Efeito da matriz de cores</span><span class="sxs-lookup"><span data-stu-id="d6f79-104">Color matrix effect</span></span>

<span data-ttu-id="d6f79-105">Use o efeito de matriz de cores para alterar os valores de RGBA de um bitmap.</span><span class="sxs-lookup"><span data-stu-id="d6f79-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="d6f79-106">Você pode usar esse efeito para:</span><span class="sxs-lookup"><span data-stu-id="d6f79-106">You can use this effect to:</span></span>

-   <span data-ttu-id="d6f79-107">Remova um canal de cor de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d6f79-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="d6f79-108">Reduza a cor em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d6f79-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="d6f79-109">Troque os canais de cores.</span><span class="sxs-lookup"><span data-stu-id="d6f79-109">Swap color channels.</span></span>
-   <span data-ttu-id="d6f79-110">Combine canais de cores.</span><span class="sxs-lookup"><span data-stu-id="d6f79-110">Combine color channels.</span></span>

<span data-ttu-id="d6f79-111">Muitos efeitos internos são especializações de matriz de cores que são otimizadas para o uso pretendido dos efeitos.</span><span class="sxs-lookup"><span data-stu-id="d6f79-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="d6f79-112">Os exemplos incluem [saturação](saturation.md), [rotação de matiz](hue-rotate.md), [sépia](sepia-effect.md)e [temperatura e tonalidade](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="d6f79-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="d6f79-113">O CLSID para esse efeito é CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="d6f79-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="d6f79-114">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d6f79-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="d6f79-115">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d6f79-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d6f79-116">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="d6f79-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="d6f79-117">Requirements</span><span class="sxs-lookup"><span data-stu-id="d6f79-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d6f79-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6f79-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="d6f79-119">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d6f79-119">Example image</span></span>

<span data-ttu-id="d6f79-120">O exemplo aqui mostra as imagens de entrada e saída do efeito de matriz de cores que permuta os canais vermelho e azul.</span><span class="sxs-lookup"><span data-stu-id="d6f79-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="d6f79-121">Antes</span><span class="sxs-lookup"><span data-stu-id="d6f79-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| <span data-ttu-id="d6f79-123">After (após)</span><span class="sxs-lookup"><span data-stu-id="d6f79-123">After</span></span>                                                        |
| ![a imagem após a transformação.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="d6f79-125">Esse efeito multiplica os valores RGBA da imagem por um 5x4, matriz de coluna principal, conforme mostrado nesta equação.</span><span class="sxs-lookup"><span data-stu-id="d6f79-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![uma definição de matriz de exemplo.](images/color-matrix-formula.png)

<span data-ttu-id="d6f79-127">Esse efeito funciona em imagens alfa retas e semimultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="d6f79-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="d6f79-128">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d6f79-128">Effect properties</span></span>



| <span data-ttu-id="d6f79-129">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="d6f79-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="d6f79-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f79-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f79-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="d6f79-131">ColorMatrix</span></span><br/> <span data-ttu-id="d6f79-132">\_Matriz de \_ cores de prop d2d1 ColorMatrix \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6f79-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="d6f79-133">Uma matriz 5x4 de valores float.</span><span class="sxs-lookup"><span data-stu-id="d6f79-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="d6f79-134">Os elementos na matriz não estão vinculados e sem unidade.</span><span class="sxs-lookup"><span data-stu-id="d6f79-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="d6f79-135">O padrão é a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="d6f79-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="d6f79-136">O tipo é D2D1 \_ Matrix \_ 5X4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="d6f79-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="d6f79-137">O valor padrão é Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d6f79-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="d6f79-138">Alphamode</span><span class="sxs-lookup"><span data-stu-id="d6f79-138">AlphaMode</span></span><br/> <span data-ttu-id="d6f79-139">Modo alfa do D2D1 \_ ColorMatrix \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6f79-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="d6f79-140">O modo alfa da saída.</span><span class="sxs-lookup"><span data-stu-id="d6f79-140">The alpha mode of the output.</span></span> <span data-ttu-id="d6f79-141">Consulte [modos alfa](#alpha-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6f79-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="d6f79-142">O tipo é D2D1 \_ ColorMatrix \_ Alpha \_ Mode.</span><span class="sxs-lookup"><span data-stu-id="d6f79-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="d6f79-143">O valor padrão é D2D1 \_ ColorMatrix \_ Alpha \_ mode \_ premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="d6f79-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d6f79-144">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="d6f79-144">ClampOutput</span></span><br/> <span data-ttu-id="d6f79-145">\_Saída d2d1 ColorMatrix \_ prop \_ fixe \_</span><span class="sxs-lookup"><span data-stu-id="d6f79-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="d6f79-146">Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo.</span><span class="sxs-lookup"><span data-stu-id="d6f79-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="d6f79-147">O efeito coloca os valores antes de premultiplicar o alfa.</span><span class="sxs-lookup"><span data-stu-id="d6f79-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="d6f79-148">Se você definir isso como verdadeiro, o efeito irá fixe os valores.</span><span class="sxs-lookup"><span data-stu-id="d6f79-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="d6f79-149">Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.</span><span class="sxs-lookup"><span data-stu-id="d6f79-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="d6f79-150">O tipo é BOOL.</span><span class="sxs-lookup"><span data-stu-id="d6f79-150">The type is BOOL.</span></span><br/> <span data-ttu-id="d6f79-151">O valor padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="d6f79-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="d6f79-152">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="d6f79-152">Alpha modes</span></span>



| <span data-ttu-id="d6f79-153">Nome</span><span class="sxs-lookup"><span data-stu-id="d6f79-153">Name</span></span>                                          | <span data-ttu-id="d6f79-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f79-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f79-155">D2D1 \_ ColorMatrix \_ \_ modo alfa \_ premultiplicado</span><span class="sxs-lookup"><span data-stu-id="d6f79-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="d6f79-156">O efeito não multiplica a entrada, aplica a matriz de cores e, em seguida, multiplica a saída.</span><span class="sxs-lookup"><span data-stu-id="d6f79-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="d6f79-157">\_ \_ Modo Alpha d2d1 \_ ColorMatrix \_ reto</span><span class="sxs-lookup"><span data-stu-id="d6f79-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="d6f79-158">O efeito aplica a matriz de cores diretamente à entrada e não remultiplique a saída.</span><span class="sxs-lookup"><span data-stu-id="d6f79-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6f79-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f79-159">Requirements</span></span>



| <span data-ttu-id="d6f79-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f79-160">Requirement</span></span> | <span data-ttu-id="d6f79-161">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f79-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f79-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f79-162">Minimum supported client</span></span> | <span data-ttu-id="d6f79-163">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d6f79-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d6f79-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f79-164">Minimum supported server</span></span> | <span data-ttu-id="d6f79-165">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d6f79-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d6f79-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6f79-166">Header</span></span>                   | <span data-ttu-id="d6f79-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d6f79-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d6f79-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6f79-168">Library</span></span>                  | <span data-ttu-id="d6f79-169">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d6f79-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d6f79-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6f79-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f79-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d6f79-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

