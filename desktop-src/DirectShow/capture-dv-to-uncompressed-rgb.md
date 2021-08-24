---
description: Capturar DV para RGB descompactado
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturar DV para RGB descompactado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb721dba2912774dd7cad18871484a9d578458161d78ea402261858cac03aa65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966757"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Capturar DV para RGB descompactado

Este exemplo mostra como capturar DV da gravação e salvá-lo em um arquivo como RGB descompactado durante a visualização. Use o grafo de filtro mostrado no diagrama a seguir.

![capturando rgb descompactado no arquivo](images/dv-rgb-cap.png)

O filtro Divisor de DV divide o áudio/vídeo intercalado em fluxos de áudio e vídeo separados O vídeo codificado em DV vai para o filtro de Decodificador de Vídeo [DV,](dv-video-decoder-filter.md) que saída de vídeo RGB descompactado. O vídeo RGB é roteado por meio do filtro Smart Tee para o filtro AVI Mux (para captura) e o renderador de vídeo (para versão prévia). Enquanto isso, o fluxo de áudio do divisor dv passa pelo filtro Tee de pino infinito para o AVI Mux e o renderador de áudio. O Gerenciador Graph Filtro mantém todos esses fluxos sincronizados, usando os carimbos de data/hora nos exemplos e no relógio de referência do grafo.

Esse grafo pode parecer desnecessariamente complicado, mas garante que o fluxo de vídeo codificado em DV seja decodificado apenas uma vez, o que minimiza os requisitos de CPU. Além disso, observe que o vídeo passa pelo filtro Smart Tee enquanto o áudio passa pelo filtro Tee de Pino Infinito. O Smart Tee pode soltar quadros de visualização para melhorar o desempenho da captura, o que é desejável para vídeo, mas não para áudio, em que exemplos descartados são altamente perceptíveis. Além disso, como o áudio requer largura de banda muito menor do que o vídeo, há relativamente pouca chance de soltar áudio no arquivo.

Você deve criar esse grafo uma seção por vez, mas o método RenderStream ainda pode ajudar. Use o seguinte código:


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



Você deve criar os filtros Dv Splitter, Dv Video Decoder, Smart Tee e Infinite Pin Tee e adicionar cada um ao grafo de filtro. (Para brevidade, essas etapas são omitidas do código anterior.) Este exemplo usa o [**método ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para encontrar os pinos de captura e visualização no filtro Smart Tee; capture é sempre o pino de saída 0 e a versão prévia é o pino de saída 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



