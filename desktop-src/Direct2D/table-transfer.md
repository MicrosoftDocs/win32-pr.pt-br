---
title: Efeito de transferência de tabela
description: Use o efeito de transferência de tabela para mapear as intensidades de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efeito de transferência de tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455158"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="9810d-104">Efeito de transferência de tabela</span><span class="sxs-lookup"><span data-stu-id="9810d-104">Table transfer effect</span></span>

<span data-ttu-id="9810d-105">Use o efeito de transferência de tabela para mapear as intensidades de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.</span><span class="sxs-lookup"><span data-stu-id="9810d-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="9810d-106">O CLSID para esse efeito é CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="9810d-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="9810d-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="9810d-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9810d-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="9810d-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9810d-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="9810d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9810d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9810d-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9810d-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="9810d-111">Example image</span></span>

<span data-ttu-id="9810d-112">A imagem aqui mostra a entrada e a saída do efeito de transferência de tabela.</span><span class="sxs-lookup"><span data-stu-id="9810d-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="9810d-113">Antes</span><span class="sxs-lookup"><span data-stu-id="9810d-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)     |
| <span data-ttu-id="9810d-115">After (após)</span><span class="sxs-lookup"><span data-stu-id="9810d-115">After</span></span>                                                          |
| ![a imagem após a transformação.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="9810d-117">A função de transferência é baseada em uma lista de entradas V = (V0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="9810d-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="9810d-118">, V<sub>N</sub>), em que N é o número de elementos-1.</span><span class="sxs-lookup"><span data-stu-id="9810d-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="9810d-119">A intensidade do pixel de entrada é representada como C. A intensidade do pixel de saída, C, pode ser calculada com a equação.</span><span class="sxs-lookup"><span data-stu-id="9810d-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="9810d-120">Para um valor C, escolha um valor k, de modo que: k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="9810d-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="9810d-121">A saída C é calculada usando a seguinte equação: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="9810d-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="9810d-122">+ (C-k/N) \* N \* (V??? uma?</span><span class="sxs-lookup"><span data-stu-id="9810d-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="9810d-123">-V?)</span><span class="sxs-lookup"><span data-stu-id="9810d-123">- V?)</span></span>

<span data-ttu-id="9810d-124">Esse efeito funciona em imagens alfa retas e semimultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="9810d-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="9810d-125">O efeito gera bitmaps alfa multiplicados.</span><span class="sxs-lookup"><span data-stu-id="9810d-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="9810d-126">Aqui está a aparência do grafo da função de transferência de tabela se a propriedade da tabela for definida como `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="9810d-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![gráfico de intensidade de pixel para a função de transferência de tabela.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="9810d-128">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="9810d-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="9810d-129">Os valores de todos os canais das propriedades de transferência de tabela não são unitários e têm um mínimo de 0,0 e um máximo de 1,0.</span><span class="sxs-lookup"><span data-stu-id="9810d-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="9810d-130">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="9810d-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="9810d-131">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="9810d-131">Type and default value</span></span>                       | <span data-ttu-id="9810d-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="9810d-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9810d-133">RedTable</span><span class="sxs-lookup"><span data-stu-id="9810d-133">RedTable</span></span><br/> <span data-ttu-id="9810d-134">\_ \_ \_ Tabela vermelha d2d1 TABLETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="9810d-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="9810d-135">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="9810d-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="9810d-136">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="9810d-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="9810d-137">A lista de valores usada para definir a função de transferência para o canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="9810d-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9810d-138">RedDisable</span><span class="sxs-lookup"><span data-stu-id="9810d-138">RedDisable</span></span><br/> <span data-ttu-id="9810d-139">D2D1 \_ TABLETRANSFER \_ prop \_ Red \_ Disable</span><span class="sxs-lookup"><span data-stu-id="9810d-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="9810d-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="9810d-140">BOOL</span></span><br/> <span data-ttu-id="9810d-141">FALSE</span><span class="sxs-lookup"><span data-stu-id="9810d-141">FALSE</span></span><br/>             | <span data-ttu-id="9810d-142">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="9810d-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="9810d-143">Se você definir isso como FALSE, ele aplicará a função RedTableTransfer ao canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="9810d-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9810d-144">Verdetable</span><span class="sxs-lookup"><span data-stu-id="9810d-144">GreenTable</span></span><br/> <span data-ttu-id="9810d-145">\_ \_ Tabela verde de prop d2d1 TABLETRANSFER \_ \_</span><span class="sxs-lookup"><span data-stu-id="9810d-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="9810d-146">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="9810d-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="9810d-147">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="9810d-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="9810d-148">A lista de valores usada para definir a função de transferência para o canal verde.</span><span class="sxs-lookup"><span data-stu-id="9810d-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9810d-149">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="9810d-149">GreenDisable</span></span><br/> <span data-ttu-id="9810d-150">D2D1 \_ TABLETRANSFER \_ prop \_ - \_ Disable verde</span><span class="sxs-lookup"><span data-stu-id="9810d-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="9810d-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="9810d-151">BOOL</span></span><br/> <span data-ttu-id="9810d-152">FALSE</span><span class="sxs-lookup"><span data-stu-id="9810d-152">FALSE</span></span><br/>             | <span data-ttu-id="9810d-153">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal verde.</span><span class="sxs-lookup"><span data-stu-id="9810d-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="9810d-154">Se você definir isso como FALSE, ele aplicará a função GreenTableTransfer ao canal verde.</span><span class="sxs-lookup"><span data-stu-id="9810d-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9810d-155">Azultable</span><span class="sxs-lookup"><span data-stu-id="9810d-155">BlueTable</span></span><br/> <span data-ttu-id="9810d-156">\_ \_ \_ Tabela azul d2d1 TABLETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="9810d-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="9810d-157">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="9810d-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="9810d-158">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="9810d-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="9810d-159">A lista de valores usada para definir a função de transferência para o canal azul.</span><span class="sxs-lookup"><span data-stu-id="9810d-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9810d-160">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="9810d-160">BlueDisable</span></span><br/> <span data-ttu-id="9810d-161">\_ \_ \_ Desabilitação azul d2d1 TABLETRANSFER prop \_</span><span class="sxs-lookup"><span data-stu-id="9810d-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="9810d-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="9810d-162">BOOL</span></span><br/> <span data-ttu-id="9810d-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="9810d-163">FALSE</span></span><br/>             | <span data-ttu-id="9810d-164">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal azul.</span><span class="sxs-lookup"><span data-stu-id="9810d-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="9810d-165">Se você definir isso como FALSE, ele aplicará a função BlueTableTransfer ao canal azul.</span><span class="sxs-lookup"><span data-stu-id="9810d-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9810d-166">Alphatable</span><span class="sxs-lookup"><span data-stu-id="9810d-166">AlphaTable</span></span><br/> <span data-ttu-id="9810d-167">\_ \_ \_ \_ Tabela Alpha de transferência de tabela d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="9810d-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="9810d-168">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="9810d-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="9810d-169">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="9810d-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="9810d-170">A lista de valores usada para definir a função de transferência para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9810d-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9810d-171">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="9810d-171">AlphaDisable</span></span><br/> <span data-ttu-id="9810d-172">\_Desabilitação do d2d1 TABLETRANSFER \_ prop \_ Alpha \_</span><span class="sxs-lookup"><span data-stu-id="9810d-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="9810d-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="9810d-173">BOOL</span></span><br/> <span data-ttu-id="9810d-174">FALSE</span><span class="sxs-lookup"><span data-stu-id="9810d-174">FALSE</span></span><br/>             | <span data-ttu-id="9810d-175">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9810d-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="9810d-176">Se você definir isso como FALSE, ele aplicará a função AlphaTableTransfer ao canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9810d-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9810d-177">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="9810d-177">ClampOutput</span></span><br/> <span data-ttu-id="9810d-178">\_Saída d2d1 TABLETRANSFER \_ prop \_ fixe \_</span><span class="sxs-lookup"><span data-stu-id="9810d-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="9810d-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="9810d-179">BOOL</span></span><br/> <span data-ttu-id="9810d-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="9810d-180">FALSE</span></span><br/>             | <span data-ttu-id="9810d-181">Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo.</span><span class="sxs-lookup"><span data-stu-id="9810d-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="9810d-182">O efeito coloca os valores antes de premultiplicar o alfa.</span><span class="sxs-lookup"><span data-stu-id="9810d-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="9810d-183">Se você definir isso como verdadeiro, o efeito irá fixe os valores.</span><span class="sxs-lookup"><span data-stu-id="9810d-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="9810d-184">Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.</span><span class="sxs-lookup"><span data-stu-id="9810d-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9810d-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9810d-185">Requirements</span></span>



| <span data-ttu-id="9810d-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="9810d-186">Requirement</span></span> | <span data-ttu-id="9810d-187">Valor</span><span class="sxs-lookup"><span data-stu-id="9810d-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9810d-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9810d-188">Minimum supported client</span></span> | <span data-ttu-id="9810d-189">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9810d-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9810d-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9810d-190">Minimum supported server</span></span> | <span data-ttu-id="9810d-191">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9810d-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9810d-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9810d-192">Header</span></span>                   | <span data-ttu-id="9810d-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9810d-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9810d-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9810d-194">Library</span></span>                  | <span data-ttu-id="9810d-195">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9810d-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9810d-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9810d-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9810d-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9810d-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

