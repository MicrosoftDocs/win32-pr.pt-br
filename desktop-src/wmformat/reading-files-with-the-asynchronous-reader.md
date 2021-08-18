---
title: Lendo arquivos com o Leitor Assíncrono
description: Lendo arquivos com o Leitor Assíncrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows SDK de Formato de Mídia, lendo arquivos
- Windows SDK de Formato de Mídia, leitores assíncronos
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (Formato de Sistemas Avançados), leitores assíncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (Formato de Sistemas Avançados), lendo arquivos
- leitores assíncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores assíncronos
- leitores assíncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea24a8f09cff8fe3e4a1f1cfb383f5569e968200bbbe6f25f2c8f225b3c18f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084503"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lendo arquivos com o Leitor Assíncrono

O leitor assíncrono lê o conteúdo de arquivos ASF usando vários threads e chamadas assíncronas. Os recursos com suporte do leitor assíncrono o tornam adequado para aplicativos que renderizam conteúdo para usuários finais.

A funcionalidade mais básica do objeto de leitor pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" refere-se ao programa que você escreve usando o SDK Windows Formato de Mídia.

1.  O aplicativo implementa a interface [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para manipular mensagens do leitor. Isso inclui dois métodos de retorno de chamada: **OnStatus**, que recebe mensagens relacionadas ao status de vários aspectos do leitor e **OnSample**, que recebe amostras descompactadas do leitor.
2.  O aplicativo passa para o leitor o nome de um arquivo a ser lido. Quando o leitor abre o arquivo, ele atribui um número de saída a cada fluxo. Se o arquivo usar exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.
3.  O aplicativo obtém informações sobre a configuração das várias saídas do leitor. As informações coletadas permitirão que o aplicativo renderizar corretamente exemplos de mídia.
4.  O aplicativo instrui o leitor a começar a ler dados do arquivo. O leitor começa a fornecer exemplos descompactados para o retorno de chamada **OnSample** um de cada vez em buffers envolvidos em objetos de buffer. Os exemplos entregues pelo leitor estão em ordem de tempo de apresentação. O leitor continuará entregando exemplos até que seja interrompido pelo aplicativo ou até que o final do arquivo seja atingido.
5.  O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor. O Windows SDK de Formato de Mídia não fornece nenhuma rotina de renderização. Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o SDK do Microsoft DirectX® ou as funções multimídia do SDK do Microsoft Windows Platform.
6.  Quando a leitura for concluída, o aplicativo instrui o leitor a fechar o arquivo.

Essas etapas são ilustradas no aplicativo de exemplo AudioPlayer, entre outros. Para obter mais informações, consulte [Aplicativos de exemplo](sample-applications.md).

O leitor também dá suporte a funcionalidades mais avançadas. O leitor permite que você faça o seguinte:

-   Pausar a reprodução de um arquivo.
-   Recuperar estatísticas de desempenho do leitor.
-   Seleção de fluxo de controle para fluxos mutuamente exclusivos.
-   Aloce manualmente buffers para saída.
-   Forneça seu próprio relógio.
-   Recupere o status das operações de arquivo (buffer, download ou salvar).
-   Abra um arquivo usando a interface COM padrão, **IStream.**
-   Procure pontos específicos em um arquivo ASF.
-   Ler dados de perfil do header do arquivo.

As seções a seguir descrevem o uso do objeto de leitor em detalhes.

-   [Para implementar mensagens de leitor no retorno de chamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Para implementar o retorno de chamada OnSample](to-implement-the-onsample-callback.md)
-   [Para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md)
-   [Para recuperar exemplos de mídia com o Leitor Assíncrono](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Para buscar por tempo usando o leitor assíncrono](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Para buscar por número de quadro usando o leitor assíncrono](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Para buscar pelo código de tempo SMPTE usando o leitor assíncrono](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Para buscar marcadores](to-seek-to-markers.md)
-   [Para pausar ou parar a reprodução](to-pause-or-stop-playback.md)
-   [Para obter estatísticas de desempenho do leitor](to-get-reader-performance-statistics.md)
-   [Para usar a seleção manual de fluxo](to-use-manual-stream-selection.md)
-   [Para fornecer exemplos compactados com o Leitor Assíncrono](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> </dl>

 

 




