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
# <a name="histogram-effect"></a>Efeito de histograma

Use o efeito de histograma para gerar um histograma para o bitmap de entrada com base no número especificado de compartimentos.

O CLSID para esse efeito é CLSID \_ D2D1Histogram.

-   [Exemplo](#example)
-   [Propriedades do efeito](#effect-properties)
-   [Seletores de canal](#channel-selectors)
-   [Saída de dados](#data-output)
-   [Comentários](#remarks)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| Grafo dos dados de saída do histograma                         |
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



## <a name="effect-properties"></a>Propriedades do efeito

Aqui está a equação para gerar a saída.

![a equação para gerar a saída do efeito de histograma.](images/histogram-formula.png)

*eu* é avaliado de 0 para o número de compartimentos. O efeito gera um histograma para valores de pixel entre 0 e 1. Os valores fora desse intervalo são clamped para o intervalo. O intervalo de um Bucket específico depende do número de buckets. Esse efeito funciona em pixels de bitmap retos. Os canais de cores do bitmap de entrada são divididos pelo canal alfa para computar esse efeito.



| Nome de exibição e enumeração de índice                                             | Tipo e valor padrão                                                   | Descrição                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> \_ \_ \_ Compartimentos de número da prop d2d1 histograma \_<br/>                 | UINT32<br/> 256<br/>                                         | Especifica o número de compartimentos usados para o histograma. O intervalo de valores de intensidade que se enquadram em um Bucket específico depende do número de buckets especificados.                              |
| ChannelSelect<br/> \_ \_ Selecionar canal de prop d2d1 histograma \_ \_<br/>     | \_Seletor de canal d2d1 \_<br/> \_Seletor de canal do d2d1 \_ \_ R<br/> | Especifica o canal usado para gerar o histograma. Esse efeito tem uma única saída de dados correspondente ao canal especificado. Consulte [seletores de canal](#channel-selectors) para obter mais informações. |
| HistogramOutput<br/> \_Saída de \_ histograma de prop d2d1 histograma \_ \_<br/> | BARRA\[\]<br/> Somente propriedade de saída.<br/>                    | A matriz de saída.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Seletores de canal



| Enumeração                | Descrição                                                           |
|----------------------------|-----------------------------------------------------------------------|
| \_Seletor de canal do d2d1 \_ \_ R | O efeito gera a saída de histograma com base no canal vermelho.   |
| \_Seletor de canal d2d1 \_ \_ G | O efeito gera a saída do histograma com base no canal verde. |
| \_Seletor de canal do d2d1 \_ \_ B | O efeito gera a saída de histograma com base no canal azul.  |
| \_ \_ Seletor de canal do d2d1 \_ A | O efeito gera a saída de histograma com base no canal alfa. |



 

## <a name="data-output"></a>Saída de dados

Esse efeito gera um FLOAT \[ \] , com o número de elementos correspondentes ao número de compartimentos especificados. Cada elemento em FLOAT \[ \] é um float. O valor do elemento corresponde ao número de elementos nessa bin.

## <a name="remarks"></a>Comentários

> [!Note]  
> O método [**createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) falhará se o dispositivo não oferecer suporte a DirectCompute e retornar HRESULT = D2DERR \_ recursos de dispositivo insuficientes \_ \_ . Todos os cartões DirectX11 e cartões DirectX10 que dão suporte ao DirectCompute podem usar o efeito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

