---
description: Criando um grafo de captura de áudio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Criando um grafo de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757023"
---
# <a name="creating-an-audio-capture-graph"></a>Criando um grafo de captura de áudio

A primeira etapa para um aplicativo de captura de áudio é criar um grafo de filtro. A configuração do grafo depende do tipo de arquivo que você deseja criar.

-   Arquivo AVI somente de áudio: filtro de captura de áudio para filtro [AVI Mux](avi-mux-filter.md) e AVI Mux para filtro de [gravador de arquivo](file-writer-filter.md) .
-   Arquivo WAV: filtro de captura de áudio para [exemplo de filtro WavDest](wavdest-filter-sample.md) para o filtro de gravador de arquivo
-   Arquivo de áudio do Windows Media (. WMA): filtro de captura de áudio para o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) .

O filtro WavDest é fornecido como um exemplo de SDK. Para usá-lo, você deve criar e registrar o filtro.

Para usar o filtro do gravador ASF, você deve instalar o SDK do Windows Media e obter uma chave de software para desbloquear o filtro. Para obter mais informações, consulte [usando o Windows Media no DirectShow](using-windows-media-in-directshow.md).

Você pode criar o grafo de filtro usando o objeto do [construtor do grafo de captura](capture-graph-builder.md) ou pode criar o grafo "manualmente"; ou seja, faça com que o aplicativo adicione e conecte cada filtro programaticamente. Este artigo descreve a abordagem manual. Para obter mais informações sobre como usar o construtor de gráficos de captura, consulte [captura de vídeo](video-capture.md). Grande parte das informações nesse artigo aplica-se a gráficos somente de áudio.

Adicionando o dispositivo de captura de áudio

Como o filtro de captura de áudio se comunica com um dispositivo de hardware específico, você não pode simplesmente chamar **CoCreateInstance** para criar o filtro. Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar todos os dispositivos na categoria "fontes de captura de áudio", que é identificada pelo CLSID AudioInputDeviceCategory do identificador de classe \_ .

O enumerador de dispositivo do sistema retorna uma lista de monikers para os dispositivos; o nome amigável de cada moniker corresponde ao nome do dispositivo. Escolha um dos monikers retornados e use-o para criar uma instância do filtro de captura de áudio para esse dispositivo. Adicione o filtro ao gráfico de filtro. O dispositivo de gravação de áudio preferencial do usuário aparece primeiro na lista moniker. (O usuário seleciona um dispositivo preferencial clicando em sons e multimídia no painel de controle.)

Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

Para especificar a entrada a ser capturada, obtenha a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) do filtro de captura de áudio e chame o método **Put \_ Enable** para especificar a entrada. No entanto, uma limitação desse método é que diferentes dispositivos de hardware podem usar cadeias de caracteres diferentes para identificar suas entradas. Por exemplo, um cartão pode usar "microfone" para identificar a entrada do microfone e outro cartão pode usar "MIC". Para determinar o identificador de cadeia de caracteres de uma determinada entrada, use as funções de multimídia do Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Consulte o tópico do MSDN no [mixer consultas de dispositivo](/windows/desktop/Multimedia/mixer-device-queries) para obter mais informações.

Adicionando o multiplexador e o gravador de arquivos

Um grafo de captura de áudio deve conter um multiplexador e um gravador de arquivo.

Um *multiplexador* é um filtro que combina um ou mais fluxos em um único fluxo com um formato específico. Por exemplo, o filtro AVI Mux combina fluxos de áudio e vídeo em um fluxo AVI intercalado. Para captura de áudio, normalmente há apenas um único fluxo de áudio, mas os dados de áudio ainda devem ser empacotados em um formato que possa ser salvo em disco, o que requer um multiplexador. A escolha do Multiplexador depende do formato de destino:

-   AVI: multiplexador AVI
-   WAV: WavDest
-   WMA: gravador ASF

Um *gravador de arquivo* é um filtro que grava dados de entrada em um arquivo. Para arquivos AVI ou WAV, use o [filtro gravador de arquivo](file-writer-filter.md). Para arquivos WMA, o gravador ASF atua como Multiplexador e gravador de arquivo.

Depois de criar os filtros e adicioná-los ao grafo, conecte o pino de saída do filtro de captura de áudio ao pino de entrada do Multiplexador e conecte o pino de saída do Multiplexador ao pino de entrada do gravador de filtro (supondo que eles sejam filtros separados). Para especificar o nome do arquivo, consulte o gravador de arquivo para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chame o método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .

### <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra como criar um grafo de captura de áudio usando o filtro WavDest. Os mesmos princípios se aplicam a outros tipos de arquivo.


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



Este exemplo usa a `AddFilterByCLSID` função descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md)e a `ConnectFilters` função descrita em [conectar dois filtros](connect-two-filters.md). Nenhuma delas é uma API do DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 
