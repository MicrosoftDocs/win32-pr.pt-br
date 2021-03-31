---
description: Capturar DV para RGB descompactado
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturar DV para RGB descompactado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087314"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Capturar DV para RGB descompactado

Este exemplo mostra como capturar DV da camcorder e salvá-la em um arquivo como RGB descompactado durante a visualização. Use o gráfico de filtro mostrado no diagrama a seguir.

![capturando RGB descompactado para o arquivo](images/dv-rgb-cap.png)

O filtro de Splitter de DV divide o áudio/vídeo intercalado em fluxos de áudio e vídeo separados o vídeo codificado em DV vai para o filtro de [codificador de vídeo DV](dv-video-decoder-filter.md) , que gera vídeo RGB não compactado. O vídeo RGB é roteado por meio do filtro de monitoração inteligente para o filtro AVI Mux (para captura) e o processador de vídeo (para visualização). Enquanto isso, o fluxo de áudio do divisor de DV passa pelo filtro de t de PIN infinito para o AVI Mux e o processador de áudio. O Gerenciador de gráfico de filtro mantém todos esses fluxos sincronizados, usando os carimbos de data/hora nos exemplos e no relógio de referência do grafo.

Esse grafo pode parecer desnecessariamente complicado, mas garante que o fluxo de vídeo codificado em DV seja decodificado apenas uma vez, o que minimiza os requisitos de CPU. Além disso, observe que o vídeo passa pelo filtro de monitoração inteligente enquanto o áudio passa pelo filtro de t de PIN infinito. O monitor inteligente pode descartar quadros de visualização para melhorar o desempenho da captura, o que é desejável para vídeo, mas não para áudio, onde as amostras descartadas são altamente perceptíveis. Além disso, como o áudio requer uma largura de banda muito menor do que o vídeo, há relativamente pouca chance de remover o áudio no arquivo.

Você deve criar esse gráfico uma seção por vez, mas o método RenderStream ainda pode ajudar. Use o seguinte código:


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



Você deve criar os filtros de visor DV, decodificador de vídeo DV, monitoração inteligente e de t PIN infinito e adicionar cada um ao gráfico de filtro. (Para fins de brevidade, essas etapas são omitidas do código anterior.) Este exemplo usa o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para localizar os Pins de captura e visualização no filtro de "inteligente"; a captura sempre é o pino de saída 0 e a visualização é o pino de saída 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



