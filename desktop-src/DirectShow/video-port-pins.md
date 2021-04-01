---
description: Pins de porta de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Pins de porta de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829047"
---
# <a name="video-port-pins"></a>Pins de porta de vídeo

Um dispositivo de captura com uma porta de vídeo de hardware pode usar as VPE (extensões de porta de vídeo) no Microsoft® DirectX®. Nesse caso, o filtro de captura terá um PIN de porta de vídeo (VP). Nenhum dado de vídeo viaja do VP do pino por meio do gráfico de filtro. Em vez disso, os quadros de vídeo são produzidos em hardware e enviados diretamente para a memória de vídeo. O VP de fixação permite que as mensagens de controle sejam enviadas ao hardware.

É importante conectar o VP de fixação, mesmo que seu aplicativo execute apenas a captura de arquivos sem visualização. Se você deixar o PIN desconectado, o grafo não será executado corretamente. Isso é diferente dos Pins de visualização, que não precisam ser conectados.

Os diferentes renderizadores de vídeo do DirectShow fornecem suporte variado para os Pins de VP:

-   Renderizador de vídeo: Conecte o VP de fixação ao pino 0 no filtro de [mixer de sobreposição](overlay-mixer-filter.md) e conecte o filtro do mixer de sobreposição ao processador de vídeo.
-   VMR-7: Conecte o pino VP ao filtro do [Gerenciador de portas de vídeo](video-port-manager.md) e conecte o Gerenciador de portas de vídeo ao VMR-7.
-   VMR-9: você não poderá usar o VMR-9 se o dispositivo tiver um VP PIN, pois o Direct3D 9 não oferece suporte a portas de vídeo. Use o renderizador de vídeo ou o VMR-7.

Para cenários de porta de vídeo, o mixer de sobreposição e o processador de vídeo são recomendados no Gerenciador de portas de vídeo e no VMR-7, pois nem todos os drivers dão suporte ao Gerenciador de portas de vídeo. Em geral, o mixer de sobreposição é a opção mais confiável para portas de vídeo.

O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente o mixer de sobreposição, se houver um pino VP. Se você estiver criando o grafo sem usar esse método, deverá verificar se há um PIN de porta de vídeo no filtro de captura e, se houver, conectá-lo ao filtro de mixer de sobreposição, como mostrado no diagrama a seguir.

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



Depois de adicionar o mixer de sobreposição ao grafo, chame **FindPin** novamente para localizar o pino 0 no mixer de sobreposição. O PIN 0 é sempre o primeiro PIN de entrada no filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Conecte os dois Pins chamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Em seguida, conecte o pino de saída do mixer de sobreposição ao filtro de processador de vídeo. Você pode ocultar o vídeo chamando os métodos [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::P UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) no Gerenciador de gráficos de filtro.

Para sintonizadores de TV, o filtro de captura também pode ter uma porta de vídeo VBI PIN (PIN \_ Category \_ VIDEOPORT \_ VBI). Nesse caso, conecte esse PIN ao filtro de [alocador de superfície VBI](vbi-surface-allocator.md) . Para obter mais informações, consulte [exibindo legendas ocultas](viewing-closed-captions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Usando o mixer de sobreposição na captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



