---
description: Criando um sistema de captura de Graph
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Criando um sistema de captura de Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ff89cff8662bb5da81860053221596b18e89ab2300134cf2ff8826ae99b787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108216"
---
# <a name="creating-an-audio-capture-graph"></a>Criando um sistema de captura de Graph

A primeira etapa para um aplicativo de captura de áudio é criar um grafo de filtro. A configuração do grafo depende do tipo de arquivo que você deseja criar.

-   Arquivo AVI somente áudio: filtro de captura de áudio para [filtro Mux AVI](avi-mux-filter.md) e filtro AVI Mux para [File Writer.](file-writer-filter.md)
-   Arquivo WAV: Filtro de captura de áudio para [exemplo de filtro wavDest](wavdest-filter-sample.md) para filtro de gravação de arquivo
-   Windows Arquivo de áudio de mídia (.wma) : filtro de captura de áudio para [filtro de Gravação DO ASF](wm-asf-writer-filter.md) WM.

O filtro WavDest é fornecido como um exemplo do SDK. Para usá-lo, você deve criar e registrar o filtro.

Para usar o filtro AsF Writer, você deve instalar o SDK Windows Mídia e obter uma chave de software para desbloquear o filtro. Para obter mais informações, [consulte Using Windows Media in DirectShow](using-windows-media-in-directshow.md).

Você pode criar o grafo de filtro usando o objeto [Capture Graph Builder](capture-graph-builder.md) ou pode criar o grafo "manualmente"; ou seja, fazer com que o aplicativo adicione e conecte cada filtro programaticamente. Este artigo descreve a abordagem manual. Para obter mais informações sobre como usar o Capture Graph Builder, consulte [Captura de vídeo](video-capture.md). Grande parte das informações nesse artigo se aplica a grafos somente de áudio.

Adicionando o dispositivo de captura de áudio

Como o Filtro de Captura de Áudio se comunica com um dispositivo de hardware específico, você não pode simplesmente chamar **CoCreateInstance** para criar o filtro. Em vez disso, use o [Enumerador](system-device-enumerator.md) de Dispositivo do Sistema para enumerar todos os dispositivos na categoria "Fontes de Captura de Áudio", que é identificada pelo identificador de classe CLSID \_ AudioInputDeviceCategory.

O Enumerador de Dispositivo do Sistema retorna uma lista de monikers para os dispositivos; O nome amigável de cada moniker corresponde ao nome do dispositivo. Escolha um dos monikers retornados e use-o para criar uma instância do Filtro de Captura de Áudio para esse dispositivo. Adicione o filtro ao grafo de filtro. O dispositivo de gravação de áudio preferencial do usuário aparece primeiro na lista de monikers. (O usuário seleciona um dispositivo preferencial clicando em Sons e Multimídia Painel de Controle.)

Para obter mais informações, [consulte Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

Para especificar de qual entrada capturar, obtenha a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) do filtro Captura de Áudio e chame o método **put \_ Enable** para especificar a entrada. No entanto, uma limitação desse método é que diferentes dispositivos de hardware podem usar cadeias de caracteres diferentes para identificar suas entradas. Por exemplo, um cartão pode usar "Microfone" para identificar a entrada do microfone e outro cartão pode usar "Mic". Para determinar o identificador de cadeia de caracteres para uma determinada entrada, use as funções Windows Multimídia [**waveOutOpen,**](/previous-versions//dd743866(v=vs.85)) [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Consulte o tópico MSDN [Mixer consultas de dispositivo](/windows/desktop/Multimedia/mixer-device-queries) para obter mais informações.

Adicionando o multiplexador e o File Writer

Um grafo de captura de áudio deve conter um multiplexador e um gravação de arquivo.

Um *multiplexador* é um filtro que combina um ou mais fluxos em um único fluxo com um formato específico. Por exemplo, o filtro AVI Mux combina fluxos de áudio e vídeo em um fluxo AVI intercalado. Para captura de áudio, normalmente há apenas um único fluxo de áudio, mas os dados de áudio ainda devem ser empacotados em um formato que pode ser salvo no disco, o que requer um multiplexador. A escolha do multiplexador depende do formato de destino:

-   AVI: Multiplexador AVI
-   WAV: WavDest
-   WMA: ASF Writer

Um *file writer é* um filtro que grava dados de entrada em um arquivo. Para arquivos AVI ou WAV, use o [Filtro de Autor de Arquivos](file-writer-filter.md). Para arquivos WMA, o AsF Writer atua como multiplexador e autor de arquivos.

Depois de criar os filtros e adicioná-los ao grafo, conecte o pino de saída do Filtro de Captura de Áudio ao pino de entrada do multiplexador e conecte o pino de saída do multiplexador ao pino de entrada do autor do filtro (supondo que eles sejam filtros separados). Para especificar o nome do arquivo, consulte o autor do arquivo para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chame o [**método IFileSinkFilter::SetFileName.**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename)

### <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra como criar um grafo de captura de áudio usando o filtro WavDest. Os mesmos princípios se aplicam aos outros tipos de arquivo.


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



Este exemplo usa a `AddFilterByCLSID` função descrita em Adicionar um filtro por [CLSID](add-a-filter-by-clsid.md)e a `ConnectFilters` função descrita em Conexão Dois [Filtros](connect-two-filters.md). Nenhum deles é uma API DirectShow dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 
