---
title: Efeito de transferência discreta
description: Use o efeito de transferência discreta para mapear as intensidades de cor de uma imagem usando uma função de transferência de etapa criada a partir de uma lista de valores que você fornece.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- efeito de transferência discreta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104564069"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="c6a69-104">Efeito de transferência discreta</span><span class="sxs-lookup"><span data-stu-id="c6a69-104">Discrete transfer effect</span></span>

<span data-ttu-id="c6a69-105">Use o efeito de transferência discreta para mapear as intensidades de cor de uma imagem usando uma função de transferência de etapa criada a partir de uma lista de valores que você fornece.</span><span class="sxs-lookup"><span data-stu-id="c6a69-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="c6a69-106">O CLSID para esse efeito é CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="c6a69-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="c6a69-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c6a69-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c6a69-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c6a69-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c6a69-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="c6a69-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c6a69-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6a69-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c6a69-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c6a69-111">Example image</span></span>

<span data-ttu-id="c6a69-112">A imagem aqui mostra a entrada e a saída do efeito de transferência discreta.</span><span class="sxs-lookup"><span data-stu-id="c6a69-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="c6a69-113">Antes</span><span class="sxs-lookup"><span data-stu-id="c6a69-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)        |
| <span data-ttu-id="c6a69-115">After (após)</span><span class="sxs-lookup"><span data-stu-id="c6a69-115">After</span></span>                                                             |
| ![a imagem após a transformação.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="c6a69-117">A função de transferência é baseada na lista de entradas: V = (V0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="c6a69-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="c6a69-118">, V<sub>N</sub>), em que N é o número de elementos-1.</span><span class="sxs-lookup"><span data-stu-id="c6a69-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="c6a69-119">A intensidade do pixel de entrada é representada como C. A intensidade do pixel de saída, C é calculada com a equação:</span><span class="sxs-lookup"><span data-stu-id="c6a69-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="c6a69-120">Para um valor C, escolha um valor k, de modo que:</span><span class="sxs-lookup"><span data-stu-id="c6a69-120">For a value C, pick a value k, such that:</span></span>

![fórmula para o processo.](images/discrete-transfer1.png)

<span data-ttu-id="c6a69-122">A saída C pode ser calculada usando a equação: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="c6a69-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="c6a69-123">Esse efeito funciona em imagens alfa retas e semimultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="c6a69-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="c6a69-124">O efeito gera bitmaps alfa multiplicados.</span><span class="sxs-lookup"><span data-stu-id="c6a69-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="c6a69-125">Esta é a aparência do grafo da função de transferência discreta se as entradas forem `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="c6a69-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![gráfico de intensidade de pixel para a função de transferência discreta.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="c6a69-127">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c6a69-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="c6a69-128">Os valores de todos os canais das propriedades de transferência discretas não são unitários e têm um mínimo de 0,0 e um máximo de 1,0.</span><span class="sxs-lookup"><span data-stu-id="c6a69-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="c6a69-129">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="c6a69-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="c6a69-130">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="c6a69-130">Type and default value</span></span>                       | <span data-ttu-id="c6a69-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6a69-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a69-132">RedTable</span><span class="sxs-lookup"><span data-stu-id="c6a69-132">RedTable</span></span><br/> <span data-ttu-id="c6a69-133">\_ \_ \_ Tabela vermelha d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="c6a69-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="c6a69-134">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="c6a69-135">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="c6a69-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="c6a69-136">A lista de valores usada para definir a função de transferência para o canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="c6a69-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c6a69-137">RedDisable</span><span class="sxs-lookup"><span data-stu-id="c6a69-137">RedDisable</span></span><br/> <span data-ttu-id="c6a69-138">D2D1 \_ DISCRETETRANSFER \_ prop \_ Red \_ Disable</span><span class="sxs-lookup"><span data-stu-id="c6a69-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="c6a69-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="c6a69-139">BOOL</span></span><br/> <span data-ttu-id="c6a69-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6a69-140">FALSE</span></span><br/>             | <span data-ttu-id="c6a69-141">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="c6a69-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="c6a69-142">Se você definir isso como falso, o efeito aplicará a função RedDiscreteTransfer ao canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="c6a69-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c6a69-143">Verdetable</span><span class="sxs-lookup"><span data-stu-id="c6a69-143">GreenTable</span></span><br/> <span data-ttu-id="c6a69-144">\_ \_ Tabela verde de prop d2d1 DISCRETETRANSFER \_ \_</span><span class="sxs-lookup"><span data-stu-id="c6a69-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="c6a69-145">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="c6a69-146">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="c6a69-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="c6a69-147">A lista de valores que definem a função de transferência para o canal verde.</span><span class="sxs-lookup"><span data-stu-id="c6a69-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c6a69-148">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="c6a69-148">GreenDisable</span></span><br/> <span data-ttu-id="c6a69-149">D2D1 \_ DISCRETETRANSFER \_ prop \_ - \_ Disable verde</span><span class="sxs-lookup"><span data-stu-id="c6a69-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="c6a69-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="c6a69-150">BOOL</span></span><br/> <span data-ttu-id="c6a69-151">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6a69-151">FALSE</span></span><br/>             | <span data-ttu-id="c6a69-152">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal verde.</span><span class="sxs-lookup"><span data-stu-id="c6a69-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="c6a69-153">Se você definir isso como falso, o efeito aplicará a função GreenDiscreteTransfer ao canal verde.</span><span class="sxs-lookup"><span data-stu-id="c6a69-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c6a69-154">Azultable</span><span class="sxs-lookup"><span data-stu-id="c6a69-154">BlueTable</span></span><br/> <span data-ttu-id="c6a69-155">\_ \_ \_ Tabela azul d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="c6a69-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="c6a69-156">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="c6a69-157">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="c6a69-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="c6a69-158">A lista de valores que definem a função de transferência para o canal azul.</span><span class="sxs-lookup"><span data-stu-id="c6a69-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c6a69-159">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="c6a69-159">BlueDisable</span></span><br/> <span data-ttu-id="c6a69-160">\_ \_ \_ Desabilitação azul d2d1 DISCRETETRANSFER prop \_</span><span class="sxs-lookup"><span data-stu-id="c6a69-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="c6a69-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="c6a69-161">BOOL</span></span><br/> <span data-ttu-id="c6a69-162">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6a69-162">FALSE</span></span><br/>             | <span data-ttu-id="c6a69-163">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal azul.</span><span class="sxs-lookup"><span data-stu-id="c6a69-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="c6a69-164">Se você definir isso como falso, o efeito aplicará a função BlueDiscreteTransfer ao canal azul.</span><span class="sxs-lookup"><span data-stu-id="c6a69-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c6a69-165">Alphatable</span><span class="sxs-lookup"><span data-stu-id="c6a69-165">AlphaTable</span></span><br/> <span data-ttu-id="c6a69-166">\_ \_ \_ Tabela Alpha d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="c6a69-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="c6a69-167">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="c6a69-168">{0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="c6a69-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="c6a69-169">A lista de valores que definem a função de transferência para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="c6a69-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c6a69-170">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="c6a69-170">AlphaDisable</span></span><br/> <span data-ttu-id="c6a69-171">\_Desabilitação do d2d1 DISCRETETRANSFER \_ prop \_ Alpha \_</span><span class="sxs-lookup"><span data-stu-id="c6a69-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="c6a69-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="c6a69-172">BOOL</span></span><br/> <span data-ttu-id="c6a69-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6a69-173">FALSE</span></span><br/>             | <span data-ttu-id="c6a69-174">Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal alfa.</span><span class="sxs-lookup"><span data-stu-id="c6a69-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="c6a69-175">Se você definir isso como falso, o efeito aplicará a função AlphaDiscreteTransfer ao canal alfa.</span><span class="sxs-lookup"><span data-stu-id="c6a69-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c6a69-176">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="c6a69-176">ClampOutput</span></span><br/> <span data-ttu-id="c6a69-177">\_Saída d2d1 DISCRETETRANSFER \_ prop \_ fixe \_</span><span class="sxs-lookup"><span data-stu-id="c6a69-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="c6a69-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="c6a69-178">BOOL</span></span><br/> <span data-ttu-id="c6a69-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6a69-179">FALSE</span></span><br/>             | <span data-ttu-id="c6a69-180">Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo.</span><span class="sxs-lookup"><span data-stu-id="c6a69-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="c6a69-181">O efeito coloca os valores antes de premultiplicar o alfa.</span><span class="sxs-lookup"><span data-stu-id="c6a69-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="c6a69-182">Se você definir isso como verdadeiro, o efeito irá fixe os valores.</span><span class="sxs-lookup"><span data-stu-id="c6a69-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="c6a69-183">Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.</span><span class="sxs-lookup"><span data-stu-id="c6a69-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c6a69-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a69-184">Requirements</span></span>



| <span data-ttu-id="c6a69-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a69-185">Requirement</span></span> | <span data-ttu-id="c6a69-186">Valor</span><span class="sxs-lookup"><span data-stu-id="c6a69-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a69-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6a69-187">Minimum supported client</span></span> | <span data-ttu-id="c6a69-188">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c6a69-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6a69-189">Minimum supported server</span></span> | <span data-ttu-id="c6a69-190">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c6a69-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c6a69-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6a69-191">Header</span></span>                   | <span data-ttu-id="c6a69-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c6a69-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c6a69-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6a69-193">Library</span></span>                  | <span data-ttu-id="c6a69-194">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c6a69-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c6a69-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6a69-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a69-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c6a69-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

