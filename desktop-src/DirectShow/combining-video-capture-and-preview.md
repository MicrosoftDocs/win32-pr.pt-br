---
description: Combinando captura e visualização de vídeo
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinando captura e visualização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1894e9431cbfa9e7bbbd0ef0bcec48021055350030b54ffd2f3e2729db81c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084317"
---
# <a name="combining-video-capture-and-preview"></a>Combinando captura e visualização de vídeo

As seções anteriores descrevem como capturar vídeo em vários formatos de arquivo. A seção [Visualizando Vídeo](previewing-video.md) descreve como criar um grafo de visualização ao vivo. No entanto, muitos aplicativos devem fazer ambos de uma vez. Para criar uma visualização combinada e um grafo de escrita de arquivo, basta fazer duas chamadas para [**ICaptureGraphBuilder2::RenderStream:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



Neste código, o Construtor de Graph capture está ocultando alguns detalhes:

-   Se o filtro de captura tiver um pino de visualização ou um pino de porta de vídeo, além de um pino de captura, o [**método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplesmente renderizará os dois pinos, conforme mostrado na ilustração a seguir.

    ![grafo de captura e visualização](images/vidcap04.png)

-   Se o filtro tiver apenas um pin de captura, o Construtor Graph Capture usará o [filtro Smart Tee](smart-tee-filter.md) para dividir o fluxo de captura. A ilustração a seguir mostra o grafo com um Smart Tee.

    ![grafo de captura e visualização com filtro de smart tee](images/vidcap05.png)

O filtro Smart Tee tem um pin de captura e um pino de visualização. Ele pega um único fluxo de vídeo do filtro de captura e o divide em dois fluxos, um para captura e outro para visualização. Para manter a taxa de transferência no pin de captura, o pino de visualização descarta quadros conforme necessário. Ele também distribui os carimbos de data/hora de cada exemplo antes de entregar, pelos motivos discutidos no tópico DirectShow Filtros de Captura [de Vídeo](directshow-video-capture-filters.md).

Embora o Smart Tee divida o fluxo, ele não duplica fisicamente os dados de vídeo. Em vez disso, ele usa objetos de exemplo de mídia personalizados que compartilham os buffers. Os exemplos são marcados como "somente leitura" para garantir que os filtros downstream não sejam escritos nos dados.

Se o grafo de captura tiver uma janela de visualização, várias coisas poderão fazer com que o Gerenciador Graph filtro pare todo o grafo, incluindo o fluxo de captura:

-   Bloquear o computador.
-   Pressionar CTRL+ALT+DELETE em um computador que seja membro de um domínio.
-   Executar um aplicativo Direct3D de tela inteira, como um jogo ou uma economia de tela.
-   Alternando monitores ou alterando a resolução de exibição.
-   A execução de um programa que Windows exibir uma caixa de diálogo UAC (Controle de Conta de Usuário). (Windows Vista ou posterior.)
-   Executando uma janela dos DOS de tela inteira.

Qualquer um desses eventos pode interromper a sessão de captura, possivelmente causando perda de dados. (Veja o que acontece internamente: o renderador de vídeo perde os recursos direct3D ou DirectDraw necessários. No processo de recuperação desses recursos, o renderador de vídeo deve se reconectar ao filtro upstream, fazendo com que o Gerenciador Graph Filtro pare o grafo.)

Duas soluções possíveis para esse problema são as seguintes:

-   Não inclua um fluxo de visualização. No entanto, esteja ciente de que o [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adiciona automaticamente uma janela de visualização quando o dispositivo de captura tem um pino de porta de vídeo. Consulte [Pins de porta de vídeo na Captura de Arquivos](video-port-pins-in-file-capture.md).
-   Use o Mecanismo de Buffer de Fluxo para enviar o fluxo de visualização para um grafo em outro processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



