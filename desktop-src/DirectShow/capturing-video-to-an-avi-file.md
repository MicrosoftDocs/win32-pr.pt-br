---
description: Capturando vídeo em um arquivo AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capturando vídeo em um arquivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564816"
---
# <a name="capturing-video-to-an-avi-file"></a>Capturando vídeo em um arquivo AVI

A ilustração a seguir mostra o grafo mais simples possível para capturar vídeo em um arquivo AVI.

![Grafo de captura de vídeo AVI](images/vidcap02.png)

O filtro [AVI Mux](avi-mux-filter.md) pega o fluxo de vídeo do PIN de captura e o empacota em um fluxo avi. Um fluxo de áudio também pode ser conectado ao filtro AVI Mux. nesse caso, o MUX intercalaria os dois fluxos. O filtro [gravador de arquivo](file-writer-filter.md) grava o fluxo AVI em disco.

Para criar o grafo, comece chamando o método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , da seguinte maneira:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



O primeiro parâmetro especifica o tipo de arquivo — nesse caso, AVI. O segundo parâmetro fornece o nome do arquivo. Para AVI, o método SetOutputFileName cocria o filtro AVI Mux e o filtro do gravador de arquivo e os adiciona ao grafo. Ele também define o nome do arquivo no filtro de gravador de arquivo, chamando o método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) e conecta os dois filtros. O método retorna um ponteiro para o multiplexado AVI no terceiro parâmetro. Opcionalmente, ele retorna um ponteiro para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) no quarto parâmetro. Se você não precisar dessa interface, poderá definir esse parâmetro como **NULL**, conforme mostrado no exemplo anterior.

Em seguida, chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura ao AVI Mux, da seguinte maneira:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



O primeiro parâmetro fornece a categoria de PIN, que é fixar a \_ \_ captura de categoria para captura. O segundo parâmetro fornece o tipo de mídia. O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura. O quarto parâmetro é opcional; Ele permite rotear o fluxo de vídeo por meio de um filtro intermediário, como um codificador, antes de passá-lo para o filtro Mux. Caso contrário, defina esse parâmetro como **NULL**, conforme mostrado no exemplo anterior. O quinto parâmetro é o ponteiro para o filtro Mux. Esse ponteiro é obtido chamando o método SetOutputFileName.

Para capturar áudio, chame RenderStream com o tipo de mídia \_ áudio de MediaType. Se você estiver capturando áudio e vídeo de dois dispositivos separados, é uma boa ideia fazer com que o fluxo de áudio seja o fluxo mestre. Isso ajuda a evitar descompasso entre os dois fluxos, pois o filtro AVI Mux ajusta a taxa de reprodução no fluxo de vídeo para corresponder ao fluxo de áudio. Para definir o fluxo mestre, chame o método [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) no filtro AVI Mux:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



O parâmetro para SetMasterStream é o número de fluxo, que é determinado pela ordem em que você chama RenderStream. Por exemplo, se você chamar RenderStream primeiro para vídeo e, em seguida, para áudio, o vídeo será o fluxo 0 e o áudio será o fluxo 1.

Talvez você também queira definir como o filtro AVI Mux intercala os fluxos de áudio e vídeo, chamando o método [**IConfigInterleaving::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Com o sinalizador de captura de intercalação \_ , o AVI Mux executa intercalação a uma taxa adequada para captura de vídeo. Você também pode usar intercalar \_ None, o que significa que não há intercalação – o AVI Mux simplesmente gravará os dados na ordem em que chegam. O sinalizador completo de intercalação \_ significa que o AVI Mux executa a intercalação completa; no entanto, esse modo é menos adequado para a captura de vídeo porque ele requer o mais ouvido.

Codificando o fluxo de vídeo

Você pode codificar o fluxo de vídeo inserindo um filtro de codificador entre o filtro de captura e o filtro AVI Mux. Use o [enumerador de dispositivo do sistema](system-device-enumerator.md) ou o [mapeador de filtro](filter-mapper.md) para selecionar um filtro de codificador. (Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).)

Especifique o filtro do codificador como o quarto parâmetro para RenderStream, mostrado em negrito no exemplo a seguir:


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



O filtro do codificador pode dar suporte a [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ou outras interfaces para definir os parâmetros de codificação. Para obter uma lista de interfaces possíveis, consulte [codificação de arquivos e decodificação de interfaces](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



