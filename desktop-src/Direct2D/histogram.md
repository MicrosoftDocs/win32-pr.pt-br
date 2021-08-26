---
title: Efeito histograma
description: Use o efeito de histograma para gerar um histograma para o bitmap de entrada com base no número especificado de compartimentos.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- efeito histograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08477a832b2dbf758d26a16e78905f8530d4d4525205cbc85e9d138f8b3bded7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044398"
---
# <a name="histogram-effect"></a>Efeito histograma

Use o efeito de histograma para gerar um histograma para o bitmap de entrada com base no número especificado de compartimentos.

O CLSID para esse efeito é CLSID \_ D2D1Histogram.

-   [Exemplo](#example)
-   [Propriedades de efeito](#effect-properties)
-   [Seletores de canal](#channel-selectors)
-   [Saída de dados](#data-output)
-   [Comentários](#remarks)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| Graph dos dados de saída do histograma                         |
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



## <a name="effect-properties"></a>Propriedades de efeito

Esta é a equação para gerar a saída.

![a equação para gerar a saída do efeito de histograma.](images/histogram-formula.png)

*i* é avaliado de 0 para o número de compartimentos. O efeito gera um histograma para valores de pixel entre 0 e 1. Os valores fora desse intervalo são fixados ao intervalo. O intervalo de um bucket específico depende do número de buckets. Esse efeito funciona em pixels de bitmap retos. Os canais de cores do bitmap de entrada são divididos pelo canal alfa para calcular esse efeito.



| Nome de exibição e enumeração de índice                                             | Tipo e valor padrão                                                   | Descrição                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> COMPARTIMENTOS NUM DE \_ \_ PROP DE HISTOGRAMA \_ D2D1 \_<br/>                 | UINT32<br/> 256<br/>                                         | Especifica o número de compartimentos usados para o histograma. O intervalo de valores de intensidade que se enquadram em um bucket específico depende do número de buckets especificados.                              |
| ChannelSelect<br/> D2D1 SELEÇÃO DE CANAL \_ \_ DE PROP DE \_ HISTOGRAMA \_<br/>     | SELETOR DE CANAL D2D1 \_ \_<br/> D2D1 \_ CHANNEL \_ SELECTOR \_ R<br/> | Especifica o canal usado para gerar o histograma. Esse efeito tem uma única saída de dados correspondente ao canal especificado. Confira [Seletores de canal](#channel-selectors) para obter mais informações. |
| HistogramOutput<br/> SAÍDA DE \_ \_ HISTOGRAMA DE PROP DE \_ \_ HISTOGRAMA D2D1<br/> | Flutuar\[\]<br/> Somente propriedade de saída.<br/>                    | A matriz de saída.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Seletores de canal



| Enumeração                | Descrição                                                           |
|----------------------------|-----------------------------------------------------------------------|
| D2D1 \_ CHANNEL \_ SELECTOR \_ R | O efeito gera a saída de histograma com base no canal vermelho.   |
| D2D1 \_ CHANNEL \_ SELECTOR \_ G | O efeito gera a saída de histograma com base no canal verde. |
| SELETOR DE \_ CANAL \_ D2D1 \_ B | O efeito gera a saída de histograma com base no canal azul.  |
| SELETOR DE CANAL D2D1 \_ \_ \_ A | O efeito gera a saída de histograma com base no canal alfa. |



 

## <a name="data-output"></a>Saída de dados

Esse efeito saída de um FLOAT \[ \] , com o número de elementos correspondente ao número de compartimentos especificados. Cada elemento no FLOAT \[ \] é um float. O valor do elemento corresponde ao número de elementos nesse compartimento.

## <a name="remarks"></a>Comentários

> [!Note]  
> O [**método CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) falhará se o dispositivo não der suporte ao DirectCompute e retornar HRESULT = D2DERR \_ INSUFFICIENT DEVICE \_ \_ CAPABILITIES. Todos os cartões DirectX11 e cartões DirectX10 que suportam DirectCompute podem usar o efeito .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

