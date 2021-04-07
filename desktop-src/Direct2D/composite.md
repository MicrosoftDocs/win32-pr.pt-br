---
title: Efeito composto
description: Use o efeito composto para combinar duas ou mais imagens. Esse efeito tem 13 modos compostos diferentes.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- efeito composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918597"
---
# <a name="composite-effect"></a><span data-ttu-id="ad53e-105">Efeito composto</span><span class="sxs-lookup"><span data-stu-id="ad53e-105">Composite effect</span></span>

<span data-ttu-id="ad53e-106">Use o efeito composto para combinar duas ou mais imagens.</span><span class="sxs-lookup"><span data-stu-id="ad53e-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="ad53e-107">Esse efeito tem 13 modos compostos diferentes.</span><span class="sxs-lookup"><span data-stu-id="ad53e-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="ad53e-108">T</span><span class="sxs-lookup"><span data-stu-id="ad53e-108">T</span></span>

<span data-ttu-id="ad53e-109">O efeito composto aceita duas ou mais entradas.</span><span class="sxs-lookup"><span data-stu-id="ad53e-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="ad53e-110">Quando você especifica 2 imagens, o destino é a primeira entrada (índice 0) e a origem é a segunda entrada (índice 1).</span><span class="sxs-lookup"><span data-stu-id="ad53e-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="ad53e-111">Se você especificar mais de duas entradas, as imagens serão compostas a partir da primeira entrada e a segunda, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ad53e-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="ad53e-112">Esse efeito implementa todos os modos usando a unidade de mesclagem da GPU (unidade de processamento gráfico).</span><span class="sxs-lookup"><span data-stu-id="ad53e-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="ad53e-113">O CLSID para esse efeito é CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="ad53e-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="ad53e-114">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ad53e-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ad53e-115">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ad53e-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ad53e-116">Tipos de modo</span><span class="sxs-lookup"><span data-stu-id="ad53e-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="ad53e-117">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="ad53e-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="ad53e-118">Requirements</span><span class="sxs-lookup"><span data-stu-id="ad53e-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ad53e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad53e-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ad53e-120">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ad53e-120">Example image</span></span>

<span data-ttu-id="ad53e-121">A imagem aqui mostra dois retângulos arredondados do mesmo tamanho que se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="ad53e-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="ad53e-122">O retângulo azul é a origem e o retângulo vermelho é o destino.</span><span class="sxs-lookup"><span data-stu-id="ad53e-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="ad53e-123">As imagens foram compostas com o modo de origem sobre.</span><span class="sxs-lookup"><span data-stu-id="ad53e-123">The images were composited with the Source Over mode.</span></span>

![uma imagem de exemplo mostrando dois retângulos arredondados do mesmo tamanho que se sobrepõem usando o modo de origem sobre.](images/composite-over.png)

<span data-ttu-id="ad53e-125">Aqui está outro exemplo usando o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="ad53e-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="ad53e-126">Antes da imagem 1</span><span class="sxs-lookup"><span data-stu-id="ad53e-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="ad53e-128">Antes da imagem 2</span><span class="sxs-lookup"><span data-stu-id="ad53e-128">Before image 2</span></span>                                                          |
| ![a segunda imagem antes do efeito.](images/3-composite(2of2).png)    |
| <span data-ttu-id="ad53e-130">After (após)</span><span class="sxs-lookup"><span data-stu-id="ad53e-130">After</span></span>                                                                   |
| ![a imagem após a transformação.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="ad53e-132">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ad53e-132">Effect properties</span></span>



| <span data-ttu-id="ad53e-133">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="ad53e-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="ad53e-134">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="ad53e-134">Type and default value</span></span>                                                          | <span data-ttu-id="ad53e-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad53e-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="ad53e-136">Mode</span><span class="sxs-lookup"><span data-stu-id="ad53e-136">Mode</span></span><br/> <span data-ttu-id="ad53e-137">\_Modo de \_ prop d2d1 Composite \_</span><span class="sxs-lookup"><span data-stu-id="ad53e-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="ad53e-138">\_Modo composto \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="ad53e-139">\_Origem do \_ modo composto d2d1 \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="ad53e-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="ad53e-140">O modo usado para o efeito.</span><span class="sxs-lookup"><span data-stu-id="ad53e-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="ad53e-141">Tipos de modo</span><span class="sxs-lookup"><span data-stu-id="ad53e-141">Mode types</span></span>

<span data-ttu-id="ad53e-142">A tabela aqui mostra os modos desse efeito.</span><span class="sxs-lookup"><span data-stu-id="ad53e-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="ad53e-143">As equações listadas na tabela usam estes elementos:</span><span class="sxs-lookup"><span data-stu-id="ad53e-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="ad53e-144">O = saída</span><span class="sxs-lookup"><span data-stu-id="ad53e-144">O = Output</span></span>
-   <span data-ttu-id="ad53e-145">S = origem</span><span class="sxs-lookup"><span data-stu-id="ad53e-145">S = Source</span></span>
-   <span data-ttu-id="ad53e-146">SA = origem alfa</span><span class="sxs-lookup"><span data-stu-id="ad53e-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="ad53e-147">D = destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-147">D = Destination</span></span>
-   <span data-ttu-id="ad53e-148">DA = destino alfa</span><span class="sxs-lookup"><span data-stu-id="ad53e-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="ad53e-149">Enumeração</span><span class="sxs-lookup"><span data-stu-id="ad53e-149">Enumeration</span></span>                                  | <span data-ttu-id="ad53e-150">Subscrito</span><span class="sxs-lookup"><span data-stu-id="ad53e-150">Equation</span></span>                          | <span data-ttu-id="ad53e-151">Tamanho do bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="ad53e-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad53e-152">\_Origem do \_ modo composto d2d1 \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="ad53e-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="ad53e-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="ad53e-154">União de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="ad53e-155">\_Destino do \_ modo \_ composto \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="ad53e-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="ad53e-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="ad53e-157">União de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="ad53e-158">\_ \_ Origem do modo composto d2d1 \_ \_ em</span><span class="sxs-lookup"><span data-stu-id="ad53e-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="ad53e-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="ad53e-159">O = DA \* S</span></span>                       | <span data-ttu-id="ad53e-160">Interseção de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="ad53e-161">\_ \_ Destino do modo composto d2d1 \_ \_ em</span><span class="sxs-lookup"><span data-stu-id="ad53e-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="ad53e-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-162">O = SA \* D</span></span>                       | <span data-ttu-id="ad53e-163">Interseção de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="ad53e-164">\_Saída do \_ modo \_ composto \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="ad53e-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="ad53e-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="ad53e-166">Região do bitmap de origem</span><span class="sxs-lookup"><span data-stu-id="ad53e-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="ad53e-167">\_Destino do \_ modo \_ composto \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="ad53e-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="ad53e-169">Região do bitmap de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="ad53e-170">\_Origem do modo composto d2d1 por \_ \_ \_ cima</span><span class="sxs-lookup"><span data-stu-id="ad53e-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="ad53e-171">O = DA \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="ad53e-172">Região do bitmap de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="ad53e-173">\_Destino do modo composto d2d1 por \_ \_ \_ cima</span><span class="sxs-lookup"><span data-stu-id="ad53e-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="ad53e-174">O = (1-DA) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="ad53e-175">Região do bitmap de origem</span><span class="sxs-lookup"><span data-stu-id="ad53e-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="ad53e-176">\_XOR de \_ modo \_ composto d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="ad53e-177">O = (1-DA) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="ad53e-178">União de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="ad53e-179">\_Modo composto \_ d2d1 \_ mais</span><span class="sxs-lookup"><span data-stu-id="ad53e-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="ad53e-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="ad53e-180">O = S + D</span></span>                         | <span data-ttu-id="ad53e-181">União de bitmaps de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="ad53e-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="ad53e-182">\_Cópia de \_ origem do modo composto \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="ad53e-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="ad53e-183">O = S</span><span class="sxs-lookup"><span data-stu-id="ad53e-183">O = S</span></span>                             | <span data-ttu-id="ad53e-184">Região do bitmap de origem</span><span class="sxs-lookup"><span data-stu-id="ad53e-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="ad53e-185">\_Cópia de \_ \_ origem vinculada \_ do \_ modo composto do d2d1</span><span class="sxs-lookup"><span data-stu-id="ad53e-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="ad53e-186">O = S (somente onde a origem existe)</span><span class="sxs-lookup"><span data-stu-id="ad53e-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="ad53e-187">União de bitmaps de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="ad53e-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="ad53e-188">O destino não é substituído onde a origem não exista.</span><span class="sxs-lookup"><span data-stu-id="ad53e-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="ad53e-189">\_ \_ \_ Inverter máscara de modo composto d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="ad53e-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="ad53e-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="ad53e-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="ad53e-191">União de bitmaps de origem e de destino. Os valores Alfa são inalterados.</span><span class="sxs-lookup"><span data-stu-id="ad53e-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="ad53e-192">A figura aqui mostra um exemplo de cada um dos modos com imagens que têm uma opacidade de 1,0 ou 0,5.</span><span class="sxs-lookup"><span data-stu-id="ad53e-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![uma imagem de exemplo de cada um dos modos com opacidade definida como 1,0 ou 0,5.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="ad53e-194">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="ad53e-194">Sample code</span></span>

<span data-ttu-id="ad53e-195">Para obter um exemplo desse efeito, baixe o [exemplo de modos de efeito composto Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="ad53e-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad53e-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad53e-196">Requirements</span></span>



| <span data-ttu-id="ad53e-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad53e-197">Requirement</span></span> | <span data-ttu-id="ad53e-198">Valor</span><span class="sxs-lookup"><span data-stu-id="ad53e-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad53e-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad53e-199">Minimum supported client</span></span> | <span data-ttu-id="ad53e-200">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ad53e-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad53e-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad53e-201">Minimum supported server</span></span> | <span data-ttu-id="ad53e-202">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ad53e-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad53e-203">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad53e-203">Header</span></span>                   | <span data-ttu-id="ad53e-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ad53e-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ad53e-205">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad53e-205">Library</span></span>                  | <span data-ttu-id="ad53e-206">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ad53e-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ad53e-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad53e-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad53e-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ad53e-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

