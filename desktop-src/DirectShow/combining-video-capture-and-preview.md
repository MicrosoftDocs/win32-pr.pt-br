---
description: Combinando captura de vídeo e visualização
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinando captura de vídeo e visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456488"
---
# <a name="combining-video-capture-and-preview"></a>Combinando captura de vídeo e visualização

As seções anteriores descrevem como capturar vídeos para vários formatos de arquivo. A seção [vídeo](previewing-video.md) de visualização descreve como criar um grafo de visualização dinâmica. No entanto, muitos aplicativos devem fazer ambos ao mesmo tempo. Para criar uma visualização combinada e um grafo de gravação de arquivos, basta fazer duas chamadas para [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



Nesse código, o construtor do grafo de captura está ocultando alguns detalhes:

-   Se o filtro de captura tiver um PIN de visualização ou um PIN de porta de vídeo, além de um PIN de captura, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplesmente renderiza ambos os Pins, conforme mostrado na ilustração a seguir.

    ![Grafo de captura e visualização](images/vidcap04.png)

-   Se o filtro tiver apenas um PIN de captura, o construtor de gráficos de captura usará o filtro de uso [inteligente](smart-tee-filter.md) para dividir o fluxo de captura. A ilustração a seguir mostra o grafo com um "t" inteligente.

    ![capturar e visualizar o grafo com o filtro de "t" inteligente](images/vidcap05.png)

O filtro de "t" inteligente tem um PIN de captura e um PIN de visualização. Ele usa um fluxo de vídeo único do filtro de captura e o divide em dois fluxos, um para captura e outro para visualização. Para manter a taxa de transferência no pino de captura, o pino de visualização descarta os quadros conforme necessário. Ele também retira os carimbos de data/hora de cada amostra antes de entregá-lo, pelos motivos discutidos no tópico [filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md).

Embora o monitor inteligente divida o fluxo, ele não duplica fisicamente os dados de vídeo. Em vez disso, ele usa objetos de exemplo de mídia personalizados que compartilham os buffers. Os exemplos são marcados como "somente leitura" para garantir que os filtros downstream não sejam gravados nos dados.

Se o grafo de captura tiver uma janela de visualização, várias coisas poderão fazer com que o Gerenciador de gráfico de filtro interrompa todo o grafo, incluindo o fluxo de captura:

-   Bloqueando o computador.
-   Pressionar CTRL + ALT + DELETE em um computador que seja membro de um domínio.
-   Execução de um aplicativo Direct3D de tela inteira, como um jogo ou uma proteção de tela.
-   Alternando monitores ou alterando a resolução de vídeo.
-   Executar um programa que faz com que o Windows exiba uma caixa de diálogo UAC (controle de conta de usuário). (Windows Vista ou posterior.)
-   Executando uma janela do DOS em tela inteira.

Qualquer um desses eventos pode interromper a sessão de captura, possivelmente causando perda de dados. (Aqui está o que acontece internamente: o renderizador de vídeo perde os recursos de Direct3D ou DirectDraw necessários. No processo de recuperação desses recursos, o renderizador de vídeo deve se reconectar com o filtro upstream, fazendo com que o Gerenciador do grafo de filtro pare o grafo.)

Duas soluções possíveis para esse problema são as seguintes:

-   Não inclua um fluxo de visualização. No entanto, lembre-se de que o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adiciona automaticamente uma janela de visualização quando o dispositivo de captura tem um PIN de porta de vídeo. Consulte [Pins de porta de vídeo na captura de arquivo](video-port-pins-in-file-capture.md).
-   Use o mecanismo de buffer de fluxo para enviar o fluxo de visualização para um grafo em outro processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



