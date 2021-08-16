---
title: Lendo arquivos com o Leitor Síncrono
description: Lendo arquivos com o Leitor Síncrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows SDK de Formato de Mídia, lendo arquivos
- Windows SDK de Formato de Mídia, leitores síncronos
- ASF (Advanced Systems Format), leitores síncronos
- ASF (Formato de Sistemas Avançados), leitores síncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (Formato de Sistemas Avançados), lendo arquivos
- leitores síncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores síncronos
- leitores síncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c30ed2f9af78c9643f269adb24f740f2fe9227bc2e5b8a36d5c9d29606564176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197468"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lendo arquivos com o Leitor Síncrono

Você pode usar o leitor síncrono para ler um arquivo ASF usando chamadas síncronas em vez dos métodos assíncronos no objeto de leitor. O uso de chamadas síncronas reduz o número de threads necessários para ler um arquivo. O leitor assíncrono usa vários threads para processar fluxos. Para arquivos com vários fluxos, o número de threads usados pode se tornar muito grande. O leitor síncrono usa apenas um thread.

O leitor síncrono foi projetado para atender às necessidades de criação de conteúdo e aplicativos de edição de arquivo. Você pode usar o leitor síncrono para outros aplicativos, mas sua funcionalidade é limitada.

O leitor síncrono pode abrir arquivos locais ou arquivos em uma rede usando o nome do caminho UNC (como " \\ \\ someshare \\ somedirectory \\ somefile.wmv"). Você não pode transmitir arquivos para o leitor síncrono ou abrir arquivos de um local da Internet. O leitor síncrono também fornece suporte para usar a interface COM **IStream** como uma origem.

O leitor síncrono fornece mais versatilidade para recuperar amostras de um arquivo ASF do que o leitor assíncrono. O leitor síncrono pode fornecer exemplos por número de fluxo, bem como por saída. Exemplos entregues por número de fluxo podem ser compactados ou descompactados. O leitor síncrono também pode alternar entre a entrega compactada e descompactada durante a reprodução; esse recurso é conhecido como "edição rápida". Esse recurso permite que um aplicativo de edição leia Windows conteúdo baseado em mídia e passe-o diretamente para o autor até que um quadro desejado seja atingido. Nesse ponto, o aplicativo pode dizer ao leitor para começar a fornecer conteúdo descompactado, que o aplicativo pode modificar e passar para o autor para recompactação. Quando o aplicativo terminar de modificar os quadros especificados, ele poderá dizer ao leitor para começar a entregar quadros compactados novamente.

A funcionalidade mais básica do objeto de leitor síncrono pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" refere-se ao programa que você escreve usando o SDK Windows Formato de Mídia.

1.  O aplicativo passa para o leitor síncrono o nome de um arquivo a ser lido. Quando o leitor síncrono abre o arquivo, ele atribui um número de saída a cada fluxo. Se o arquivo usar exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.
2.  O aplicativo obtém informações sobre a configuração das várias saídas do leitor. As informações coletadas permitirão que o aplicativo renderizar corretamente exemplos de mídia.
3.  O aplicativo começa a solicitar exemplos, um de cada vez, do leitor síncrono. O leitor síncrono fornece cada amostra em um objeto de buffer para o qual ele fornece a interface [**INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
4.  O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor. O Windows SDK de Formato de Mídia não fornece nenhuma rotina de renderização. Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o SDK do Microsoft Direct X ou as funções multimídia do SDK do Microsoft Windows Platform.

Essas etapas são ilustradas no aplicativo de exemplo WMSyncReader. Para obter mais informações, consulte [Aplicativos de exemplo](sample-applications.md).

O leitor síncrono também dá suporte à funcionalidade mais avançada. O leitor síncrono permite que você faça o seguinte:

-   Especifique um intervalo de exemplos a ser recuperado por hora ou por número de quadro.
-   Seleção de fluxo de controle para fluxos mutuamente exclusivos.
-   Abra um arquivo usando a interface COM padrão, **IStream.**
-   Ler dados de perfil do header do arquivo.
-   Ler metadados do header do arquivo.
-   Alternar entre amostras de fluxo e saída durante a reprodução.
-   Alternar entre amostras de fluxo compactadas e descompactados durante a reprodução.

As seções a seguir descrevem o uso do objeto de leitor síncrono em detalhes.

-   [Para criar um leitor síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Para encontrar números de fluxo e números de saída](to-find-stream-numbers-and-output-numbers.md)
-   [Para recuperar exemplos de mídia com o Leitor Síncrono](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Para buscar por tempo usando o leitor síncrono](to-seek-by-time-using-the-synchronous-reader.md)
-   [Para buscar por número de quadro usando o leitor síncrono](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Para buscar pelo código de tempo SMPTE usando o leitor síncrono](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Para recuperar exemplos de fluxo com o Leitor Síncrono](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Para recuperar exemplos compactados com o Leitor Síncrono](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Código de exemplo**

O código de exemplo a seguir mostra como ler exemplos de um arquivo ASF usando o leitor síncrono. Especifica por número de quadro um intervalo de amostras a ser entregue.


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

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto de leitor síncrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




