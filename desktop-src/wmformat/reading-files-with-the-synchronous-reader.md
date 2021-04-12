---
title: Lendo arquivos com o leitor síncrono
description: Lendo arquivos com o leitor síncrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- SDK do Windows Media Format, lendo arquivos
- SDK do Windows Media Format, leitores síncronos
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- leitores síncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores síncronos
- leitores síncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365543"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lendo arquivos com o leitor síncrono

Você pode usar o leitor síncrono para ler um arquivo ASF usando chamadas síncronas em vez dos métodos assíncronos no objeto leitor. O uso de chamadas síncronas reduz o número de threads necessários para ler um arquivo. O leitor assíncrono usa vários threads para processar fluxos. Para arquivos com vários fluxos, o número de threads usados pode se tornar muito grande. O leitor síncrono usa apenas um thread.

O leitor síncrono foi projetado para atender às necessidades de criação de conteúdo e aplicativos de edição de arquivos. Você pode usar o leitor síncrono para outros aplicativos, mas sua funcionalidade é limitada.

O leitor síncrono pode abrir arquivos que são locais ou arquivos em uma rede usando o nome do caminho UNC (como " \\ \\ someshare \\ somedirectory \\ somefile. wmv"). Não é possível transmitir arquivos para o leitor síncrono ou abrir arquivos de um local da Internet. O leitor síncrono também fornece suporte para usar a interface com de **IStream** como uma origem.

O leitor síncrono fornece mais versatilidade para recuperar amostras de um arquivo ASF do que o leitor assíncrono. O leitor síncrono pode fornecer amostras por número de fluxo, bem como por saída. Exemplos entregues por número de fluxo podem ser compactados ou descompactados. O leitor síncrono também pode alternar entre entregas compactadas e não compactadas durante a reprodução; Esse recurso é conhecido como "edição rápida". Esse recurso permite que um aplicativo de edição Leia o conteúdo baseado no Windows Media e passe-o diretamente para o gravador até que um quadro desejado seja atingido. Nesse ponto, o aplicativo pode instruir o leitor a iniciar o fornecimento de conteúdo descompactado, que o aplicativo pode modificar e passar para o gravador para recompactação. Quando o aplicativo terminar de modificar os quadros especificados, ele poderá instruir o leitor a começar a entregar quadros compactados novamente.

A funcionalidade mais básica do objeto leitor síncrono pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" se refere ao programa que você escreve usando o SDK do Windows Media Format.

1.  O aplicativo passa para o leitor síncrono o nome de um arquivo a ser lido. Quando o leitor síncrono abre o arquivo, ele atribui um número de saída a cada fluxo. Se o arquivo usar a exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.
2.  O aplicativo obtém informações sobre a configuração das várias saídas do leitor. As informações coletadas permitirão que o aplicativo processe amostras de mídia corretamente.
3.  O aplicativo começa a solicitar exemplos, um de cada vez, do leitor síncrono. O leitor síncrono entrega cada exemplo em um objeto de buffer para o qual ele fornece a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .
4.  O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor. O Windows Media Format SDK não fornece nenhuma rotina de renderização. Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o SDK do Microsoft Direct X ou as funções de multimídia do SDK da plataforma Microsoft Windows.

Essas etapas são ilustradas no aplicativo de exemplo WMSyncReader. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

O leitor síncrono também dá suporte à funcionalidade mais avançada. O leitor síncrono permite que você faça o seguinte:

-   Especifique um intervalo de amostras para recuperar por hora ou por número de quadro.
-   Seleção de fluxo de controle para fluxos mutuamente exclusivos.
-   Abra um arquivo usando a interface COM padrão, **IStream**.
-   Ler dados de perfil do cabeçalho do arquivo.
-   Ler metadados do cabeçalho do arquivo.
-   Alternar entre exemplos de fluxo e saída durante a reprodução.
-   Alternar entre amostras de fluxo compactadas e não compactadas durante a reprodução.

As seções a seguir descrevem o uso do objeto leitor síncrono em detalhes.

-   [Para criar um leitor síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Para localizar números de fluxo e números de saída](to-find-stream-numbers-and-output-numbers.md)
-   [Para recuperar amostras de mídia com o leitor síncrono](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Para buscar por tempo usando o leitor síncrono](to-seek-by-time-using-the-synchronous-reader.md)
-   [Para buscar por número de quadro usando o leitor síncrono](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Para buscar pelo código de tempo SMPTE usando o leitor síncrono](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Para recuperar exemplos de fluxo com o leitor síncrono](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Para recuperar amostras compactadas com o leitor síncrono](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Código de exemplo**

O código de exemplo a seguir mostra como ler exemplos de um arquivo ASF usando o leitor síncrono. Especifica por número de quadro um intervalo de amostras a serem entregues.


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto de leitor síncrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




