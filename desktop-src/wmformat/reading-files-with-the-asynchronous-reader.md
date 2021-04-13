---
title: Lendo arquivos com o leitor assíncrono
description: Lendo arquivos com o leitor assíncrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- SDK do Windows Media Format, lendo arquivos
- SDK do Windows Media Format, leitores assíncronos
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- leitores assíncronos, interface IWMReaderCallback
- IWMReaderCallback, leitores assíncronos
- leitores assíncronos, lendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365544"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lendo arquivos com o leitor assíncrono

O leitor assíncrono lê o conteúdo de arquivos ASF usando vários threads e chamadas assíncronas. Os recursos com suporte do leitor assíncrono o tornam adequado para aplicativos que processam o conteúdo para os usuários finais.

A funcionalidade mais básica do objeto leitor pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" se refere ao programa que você escreve usando o SDK do Windows Media Format.

1.  O aplicativo implementa a interface [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para lidar com mensagens do leitor. Isso inclui dois métodos de retorno de chamada: **OnStatus**, que recebe mensagens relacionadas ao status de vários aspectos do leitor e da **amostra**, que recebe amostras descompactadas do leitor.
2.  O aplicativo passa para o leitor o nome de um arquivo a ser lido. Quando o leitor abre o arquivo, ele atribui um número de saída a cada fluxo. Se o arquivo usar a exclusão mútua, o leitor atribuirá uma única saída para todos os fluxos mutuamente exclusivos.
3.  O aplicativo obtém informações sobre a configuração das várias saídas do leitor. As informações coletadas permitirão que o aplicativo processe amostras de mídia corretamente.
4.  O aplicativo instrui o leitor a começar a ler dados do arquivo. O leitor começa a fornecer amostras descompactadas para o retorno de chamada **onsample** , um por vez, em buffers encapsulados em objetos de buffer. Os exemplos entregues pelo leitor estão em ordem de tempo de apresentação. O leitor continuará fornecendo amostras até que seja interrompido pelo aplicativo ou até que o final do arquivo seja atingido.
5.  O aplicativo é responsável por renderizar dados depois que eles são entregues pelo leitor. O Windows Media Format SDK não fornece nenhuma rotina de renderização. Normalmente, os aplicativos usarão outros SDKs para renderizar dados, como o Microsoft DirectX® SDK ou as funções de multimídia do SDK da plataforma Microsoft Windows.
6.  Quando a leitura estiver concluída, o aplicativo instruirá o leitor a fechar o arquivo.

Essas etapas são ilustradas no aplicativo de exemplo AudioPlayer, entre outras. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

O leitor também dá suporte à funcionalidade mais avançada. O leitor permite que você faça o seguinte:

-   Pausar reprodução de um arquivo.
-   Recuperar estatísticas de desempenho do leitor.
-   Seleção de fluxo de controle para fluxos mutuamente exclusivos.
-   Aloque manualmente os buffers para saída.
-   Forneça seu próprio relógio.
-   Recupere o status das operações de arquivo (buffer, download ou salvamento).
-   Abra um arquivo usando a interface COM padrão, **IStream**.
-   Buscar pontos específicos em um arquivo ASF.
-   Ler dados de perfil do cabeçalho do arquivo.

As seções a seguir descrevem o uso do objeto leitor em detalhes.

-   [Para implementar mensagens de leitor no retorno de chamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Para implementar o retorno de chamada onsample](to-implement-the-onsample-callback.md)
-   [Para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md)
-   [Para recuperar amostras de mídia com o leitor assíncrono](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Para procurar por tempo usando o leitor assíncrono](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Para buscar por número de quadro usando o leitor assíncrono](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Para buscar pelo código de tempo SMPTE usando o leitor assíncrono](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Para buscar marcadores](to-seek-to-markers.md)
-   [Para pausar ou parar a reprodução](to-pause-or-stop-playback.md)
-   [Para obter estatísticas de desempenho do leitor](to-get-reader-performance-statistics.md)
-   [Para usar a seleção de fluxo manual](to-use-manual-stream-selection.md)
-   [Para fornecer amostras compactadas com o leitor assíncrono](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> </dl>

 

 




