---
title: Efeito de histograma
description: Use o efeito de histograma para gerar um histograma para o bitmap de entrada com base no número especificado de compartimentos.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- efeito de histograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369533"
---
# <a name="histogram-effect"></a><span data-ttu-id="8cdbe-104">Efeito de histograma</span><span class="sxs-lookup"><span data-stu-id="8cdbe-104">Histogram effect</span></span>

<span data-ttu-id="8cdbe-105">Use o efeito de histograma para gerar um histograma para o bitmap de entrada com base no número especificado de compartimentos.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="8cdbe-106">O CLSID para esse efeito é CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="8cdbe-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8cdbe-107">Example</span></span>](#example)
-   [<span data-ttu-id="8cdbe-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="8cdbe-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8cdbe-109">Seletores de canal</span><span class="sxs-lookup"><span data-stu-id="8cdbe-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="8cdbe-110">Saída de dados</span><span class="sxs-lookup"><span data-stu-id="8cdbe-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="8cdbe-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cdbe-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="8cdbe-112">Requirements</span><span class="sxs-lookup"><span data-stu-id="8cdbe-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8cdbe-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cdbe-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="8cdbe-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8cdbe-114">Example</span></span>



| <span data-ttu-id="8cdbe-115">Antes</span><span class="sxs-lookup"><span data-stu-id="8cdbe-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="8cdbe-117">Grafo dos dados de saída do histograma</span><span class="sxs-lookup"><span data-stu-id="8cdbe-117">Graph of the histogram output data</span></span>                         |
| ![a imagem após a transformação.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="8cdbe-119">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="8cdbe-119">Effect properties</span></span>

<span data-ttu-id="8cdbe-120">Aqui está a equação para gerar a saída.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-120">Here's the equation to generate the output.</span></span>

![a equação para gerar a saída do efeito de histograma.](images/histogram-formula.png)

<span data-ttu-id="8cdbe-122">*eu* é avaliado de 0 para o número de compartimentos. O efeito gera um histograma para valores de pixel entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="8cdbe-123">Os valores fora desse intervalo são clamped para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="8cdbe-124">O intervalo de um Bucket específico depende do número de buckets.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="8cdbe-125">Esse efeito funciona em pixels de bitmap retos.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="8cdbe-126">Os canais de cores do bitmap de entrada são divididos pelo canal alfa para computar esse efeito.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="8cdbe-127">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="8cdbe-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="8cdbe-128">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="8cdbe-128">Type and default value</span></span>                                                   | <span data-ttu-id="8cdbe-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cdbe-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cdbe-130">NumBins</span><span class="sxs-lookup"><span data-stu-id="8cdbe-130">NumBins</span></span><br/> <span data-ttu-id="8cdbe-131">\_ \_ \_ Compartimentos de número da prop d2d1 histograma \_</span><span class="sxs-lookup"><span data-stu-id="8cdbe-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="8cdbe-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="8cdbe-132">UINT32</span></span><br/> <span data-ttu-id="8cdbe-133">256</span><span class="sxs-lookup"><span data-stu-id="8cdbe-133">256</span></span><br/>                                         | <span data-ttu-id="8cdbe-134">Especifica o número de compartimentos usados para o histograma.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="8cdbe-135">O intervalo de valores de intensidade que se enquadram em um Bucket específico depende do número de buckets especificados.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="8cdbe-136">ChannelSelect</span><span class="sxs-lookup"><span data-stu-id="8cdbe-136">ChannelSelect</span></span><br/> <span data-ttu-id="8cdbe-137">\_ \_ Selecionar canal de prop d2d1 histograma \_ \_</span><span class="sxs-lookup"><span data-stu-id="8cdbe-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="8cdbe-138">\_Seletor de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="8cdbe-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="8cdbe-139">\_Seletor de canal do d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="8cdbe-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="8cdbe-140">Especifica o canal usado para gerar o histograma.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="8cdbe-141">Esse efeito tem uma única saída de dados correspondente ao canal especificado.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="8cdbe-142">Consulte [seletores de canal](#channel-selectors) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="8cdbe-143">HistogramOutput</span><span class="sxs-lookup"><span data-stu-id="8cdbe-143">HistogramOutput</span></span><br/> <span data-ttu-id="8cdbe-144">\_Saída de \_ histograma de prop d2d1 histograma \_ \_</span><span class="sxs-lookup"><span data-stu-id="8cdbe-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="8cdbe-145">BARRA\[\]</span><span class="sxs-lookup"><span data-stu-id="8cdbe-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="8cdbe-146">Somente propriedade de saída.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-146">Output property only.</span></span><br/>                    | <span data-ttu-id="8cdbe-147">A matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="8cdbe-148">Seletores de canal</span><span class="sxs-lookup"><span data-stu-id="8cdbe-148">Channel selectors</span></span>



| <span data-ttu-id="8cdbe-149">Enumeração</span><span class="sxs-lookup"><span data-stu-id="8cdbe-149">Enumeration</span></span>                | <span data-ttu-id="8cdbe-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cdbe-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8cdbe-151">\_Seletor de canal do d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="8cdbe-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="8cdbe-152">O efeito gera a saída de histograma com base no canal vermelho.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="8cdbe-153">\_Seletor de canal d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="8cdbe-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="8cdbe-154">O efeito gera a saída do histograma com base no canal verde.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="8cdbe-155">\_Seletor de canal do d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="8cdbe-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="8cdbe-156">O efeito gera a saída de histograma com base no canal azul.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="8cdbe-157">\_ \_ Seletor de canal do d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="8cdbe-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="8cdbe-158">O efeito gera a saída de histograma com base no canal alfa.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="8cdbe-159">Saída de dados</span><span class="sxs-lookup"><span data-stu-id="8cdbe-159">Data output</span></span>

<span data-ttu-id="8cdbe-160">Esse efeito gera um FLOAT \[ \] , com o número de elementos correspondentes ao número de compartimentos especificados. Cada elemento em FLOAT \[ \] é um float.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="8cdbe-161">O valor do elemento corresponde ao número de elementos nessa bin.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cdbe-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cdbe-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8cdbe-163">O método [**createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) falhará se o dispositivo não oferecer suporte a DirectCompute e retornar HRESULT = D2DERR \_ recursos de dispositivo insuficientes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8cdbe-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="8cdbe-164">Todos os cartões DirectX11 e cartões DirectX10 que dão suporte ao DirectCompute podem usar o efeito.</span><span class="sxs-lookup"><span data-stu-id="8cdbe-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8cdbe-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cdbe-165">Requirements</span></span>



| <span data-ttu-id="8cdbe-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cdbe-166">Requirement</span></span> | <span data-ttu-id="8cdbe-167">Valor</span><span class="sxs-lookup"><span data-stu-id="8cdbe-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8cdbe-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cdbe-168">Minimum supported client</span></span> | <span data-ttu-id="8cdbe-169">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8cdbe-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8cdbe-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cdbe-170">Minimum supported server</span></span> | <span data-ttu-id="8cdbe-171">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8cdbe-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8cdbe-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cdbe-172">Header</span></span>                   | <span data-ttu-id="8cdbe-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8cdbe-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8cdbe-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cdbe-174">Library</span></span>                  | <span data-ttu-id="8cdbe-175">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8cdbe-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8cdbe-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cdbe-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cdbe-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8cdbe-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

