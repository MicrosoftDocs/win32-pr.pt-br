---
description: Pins de porta de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Pins de porta de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94202e05cc467eabb77719a145a77310a62482e6f82772261b57e5ff544d2b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696776"
---
# <a name="video-port-pins"></a>Pins de porta de vídeo

Um dispositivo de captura com uma porta de vídeo de hardware pode usar as VPE (extensões de porta de vídeo) no Microsoft® DirectX®. Nesse caso, o filtro de captura terá um PIN de porta de vídeo (VP). Nenhum dado de vídeo viaja do VP do pino por meio do gráfico de filtro. Em vez disso, os quadros de vídeo são produzidos em hardware e enviados diretamente para a memória de vídeo. O VP de fixação permite que as mensagens de controle sejam enviadas ao hardware.

É importante conectar o VP de fixação, mesmo que seu aplicativo execute apenas a captura de arquivos sem visualização. Se você deixar o PIN desconectado, o grafo não será executado corretamente. Isso é diferente dos Pins de visualização, que não precisam ser conectados.

os diferentes renderizadores de vídeo DirectShow fornecem suporte variado para os pins de VP:

-   renderizador de vídeo: Conexão o pino VP para fixar 0 na [sobreposição Mixer](overlay-mixer-filter.md) filtro e conecte a sobreposição Mixer filtro ao processador de vídeo.
-   VMR-7: Conexão o pino de VP para o filtro do [gerenciador de porta de vídeo](video-port-manager.md) e conecte o gerenciador de portas de vídeo ao VMR-7.
-   VMR-9: você não poderá usar o VMR-9 se o dispositivo tiver um VP PIN, pois o Direct3D 9 não oferece suporte a portas de vídeo. Use o renderizador de vídeo ou o VMR-7.

para cenários de porta de vídeo, o Mixer de sobreposição e o processador de vídeo são recomendados no gerenciador de portas de vídeo e no VMR-7, pois nem todos os drivers dão suporte ao gerenciador de portas de vídeo. em geral, a sobreposição Mixer é a opção mais confiável para portas de vídeo.

o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente a sobreposição Mixer se houver um pino VP. se você estiver criando o grafo sem usar esse método, deverá verificar um pin de porta de vídeo no filtro de captura e, se houver, conectá-lo ao filtro de Mixer de sobreposição, conforme mostrado no diagrama a seguir.

![Conectando um PIN de porta de vídeo ao filtro de mixer de sobreposição.](images/vidcap11.png)

Você pode usar o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para procurar um VP Pin no filtro de captura:


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



depois de adicionar a sobreposição Mixer ao grafo, chame **FindPin** novamente para localizar o pino 0 no Mixer de sobreposição. O PIN 0 é sempre o primeiro PIN de entrada no filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Conexão os dois pins chamando [**IGraphBuilder:: Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



em seguida, conecte o pino de saída do Mixer de sobreposição ao filtro de processador de vídeo. você pode ocultar o vídeo chamando os métodos [**IVideoWindow::p ut \_ autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) no filtro Graph Manager.

Para sintonizadores de TV, o filtro de captura também pode ter uma porta de vídeo VBI PIN (PIN \_ Category \_ VIDEOPORT \_ VBI). Nesse caso, conecte esse PIN ao filtro de [alocador de superfície VBI](vbi-surface-allocator.md) . Para obter mais informações, consulte [exibindo legendas ocultas](viewing-closed-captions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[usando o Mixer de sobreposição na captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



