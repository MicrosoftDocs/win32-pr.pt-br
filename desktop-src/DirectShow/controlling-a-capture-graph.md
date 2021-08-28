---
description: Controlando um Graph de captura
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlando um Graph de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d678e00452fbf90591fbc187039ddbbc37cc4fde446e2e285c77fcaab415e815
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652136"
---
# <a name="controlling-a-capture-graph"></a>Controlando um Graph de captura

o filtro Graph interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) do gerenciador tem métodos para executar, parar e pausar todo o grafo. No entanto, se o grafo de filtro tiver fluxos de captura e visualização, provavelmente você desejará controlar os dois fluxos de forma independente. Por exemplo, talvez você queira Visualizar o vídeo sem capturá-lo. Você pode fazer isso por meio do método [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .

> [!Note]  
> Esse método não funciona ao capturar para um arquivo ASF (Advanced Systems Format).

 

Controlando o fluxo de captura

O código a seguir define o fluxo de captura de vídeo para ser executado por quatro segundos, iniciando um segundo após a execução do grafo:


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



O primeiro parâmetro especifica qual fluxo controlar, como um GUID de categoria de PIN. O segundo parâmetro fornece o tipo de mídia. O terceiro parâmetro é um ponteiro para o filtro de captura. Para controlar todos os fluxos de captura no grafo, defina o segundo e terceiro parâmetros como **NULL**.

Os próximos dois parâmetros definem os horários em que o fluxo será iniciado e interrompido, em relação à hora em que o grafo começa a ser executado. Chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o grafo. Até que você execute o grafo, o método **ControlStream** não terá efeito. Se o grafo já estiver em execução, as configurações entrarão em vigor imediatamente.

Os dois últimos parâmetros são usados para obter notificações de eventos quando o fluxo é iniciado e interrompido. Para cada fluxo que você controla usando esse método, o grafo de filtro envia um par de eventos: o [**controle de fluxo do EC \_ \_ \_ foi iniciado**](ec-stream-control-started.md) quando o fluxo é iniciado e o [**controle de fluxo do EC \_ \_ \_ foi interrompido**](ec-stream-control-stopped.md) quando o fluxo é interrompido. Os valores de **wStartCookie** e **wStopCookie** são usados como o segundo parâmetro de evento. Portanto, *lParam2* no evento de início é igual a **wStartCookie** e *lParam2* no evento Stop é igual a **wStopCookie**. O código a seguir mostra como obter esses eventos:


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



O método **ControlStream** define alguns valores especiais para os horários de início e de parada.



| Valor | Iniciar                                  | Stop                               |
|-------------|----------------------------------------|---------|
| MAXLONGLONG | Nunca inicie este fluxo.               | Não pare até que o grafo pare. |
| **NULL**    | Inicie imediatamente quando o grafo for executado. | Pare imediatamente.                  |



 

Por exemplo, o código a seguir interrompe o fluxo de captura imediatamente:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Embora você possa parar o fluxo de captura e reiniciá-lo mais tarde, isso criará uma lacuna nos carimbos de data/hora. Na reprodução, o vídeo aparecerá paralisado durante a lacuna (dependendo do formato de arquivo).

Controlando o fluxo de visualização

Para controlar o pino de visualização, chame **ControlStream** , mas defina o primeiro parâmetro como fixar a \_ Visualização da categoria \_ . Isso funciona exatamente como faz para \_ a captura de categoria de PIN \_ , exceto que você não pode usar tempos de referência para especificar o início e parar, pois os quadros de visualização não têm carimbos de data/hora. Portanto, você deve usar **NULL** ou MAXLONGLONG. Use **NULL** para iniciar o fluxo de visualização:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Use MAXLONGLONG para interromper o fluxo de visualização:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



Não importa se o fluxo de visualização é proveniente de um PIN de visualização no filtro de captura ou do filtro de "t" inteligente. O método **ControlStream** funciona de qualquer forma.

Para Pins de porta de vídeo, no entanto, o método falhará. Nesse caso, outra abordagem é ocultar a janela de vídeo. Consulte o grafo para **IVideoWindow** e use o método [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar ou ocultar a janela.


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



Além disso, se você chamar [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) com o valor OAFALSE antes de executar o grafo, o filtro de processamento de vídeo ocultará a janela até que você especifique o contrário. Por padrão, o renderizador de vídeo mostra a janela quando você executa o grafo.

Comentários sobre o controle de fluxo

O comportamento padrão de um PIN é fornecer exemplos quando o grafo é executado. Por exemplo, suponha que você chame **ControlStream** com a \_ captura de categoria de PIN \_ , mas não com a visualização de categoria de PIN \_ \_ . Quando você executa o grafo, o fluxo de visualização será executado imediatamente, enquanto o fluxo de captura será executado em qualquer momento que você especificar em **ControlStream**.

Se você estiver capturando mais de um fluxo e enviando-os a um filtro Mux — por exemplo, se você estiver capturando áudio e vídeo em um arquivo AVI, você deve controlar ambos os fluxos em tandem. Caso contrário, o filtro Mux pode bloquear a espera de um fluxo, pois ele tenta intercalar os dois fluxos. Defina os mesmos horários de início e de término em todos os fluxos de captura antes de executar o grafo:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Internamente, o método **ControlStream** usa a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , que é exposta nos Pins do filtro de captura, no filtro de "t" inteligente (se presente) e possivelmente no filtro Mux. Você pode usar essa interface diretamente, em vez de chamar **ControlStream**, embora não haja nenhuma vantagem específica para fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



