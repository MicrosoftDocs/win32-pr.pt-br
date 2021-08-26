---
description: Reconexão dinâmica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconexão dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966147"
---
# <a name="dynamic-reconnection"></a>Reconexão dinâmica

na maioria dos filtros de DirectShow, os pins não podem ser reconectados enquanto o grafo está transmitindo dados ativamente. O aplicativo deve parar o grafo antes de reconectar os Pins. No entanto, alguns filtros dão suporte a reconexões de PIN enquanto o grafo está em execução, um processo conhecido como reconexão dinâmica. Isso pode ser feito pelo aplicativo ou por um filtro no grafo.

Como exemplo, considere o grafo na ilustração a seguir.

![gráfico dinâmico-diagrama de construção](images/dyngraph.png)

Um cenário para reconexão dinâmica pode ser remover o filtro 2 do grafo, enquanto o grafo está em execução e substituí-lo por outro filtro. Para que esse cenário funcione, o seguinte deve ser verdadeiro:

-   O pino de entrada no filtro 3 (pino D) deve oferecer suporte à interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Essa interface permite que o PIN seja reconectado sem interromper o filtro.
-   O pino de saída no filtro 1 (pino A) deve ser capaz de bloquear o fluxo de dados de mídia enquanto a reconexão ocorre. Nenhum dado pode viajar entre o pino A e o PIN D durante a reconexão. Em geral, isso significa que o pino de saída deve dar suporte à interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . No entanto, se o filtro 1 for o filtro que inicia a reconexão, ele poderá ter um mecanismo interno para bloquear seu próprio fluxo de dados.

A reconexão dinâmica envolverá as seguintes etapas:

1.  Bloquear o fluxo de dados do PIN A.
2.  Reconecte o PIN A ao PIN D, possivelmente por meio de um novo filtro intermediário.
3.  Desbloqueie o PIN A para que os dados comecem a fluir novamente.

**Etapa 1. Bloquear o fluxo de dados**

Para bloquear o fluxo de dados, chame [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) no PIN A. Esse método pode ser chamado de forma assíncrona ou síncrona. Para chamar o método de *forma assíncrona*, crie um objeto de evento do Win32 e passe o identificador de evento para o método **Block** . O método retornará imediatamente. Aguarde até que o evento seja sinalizado, usando uma função como **WaitForSingleObject**. O PIN sinaliza o evento quando ele bloqueou o fluxo de dados. Por exemplo:


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



Para chamar o método de forma *síncrona*, basta passar o valor **NULL** em vez do identificador de evento. Agora, o método será bloqueado até que a operação seja concluída. Isso pode não acontecer até que o PIN esteja pronto para entregar um novo exemplo. Se o filtro estiver em pausa, isso poderá levar um período arbitrário. Portanto, não faça a chamada síncrona do seu thread de aplicativo principal. Use um thread de trabalho ou, caso contrário, chame o método de forma assíncrona.

**Etapa 2. Reconectar os Pins**

para reconectar os pins, consulte o filtro Graph Manager para a interface **IGraphConfig** e chame [**IGraphConfig:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) ou [**IGraphConfig:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). O método **reconnect** é mais simples de usar; Ele faz o seguinte:

-   Interrompe os filtros intermediários (filtro 2 no exemplo) e os remove do grafo.
-   Adiciona novos filtros intermediários, se necessário.
-   Conecta todos os Pins.
-   Pausa ou executa quaisquer filtros novos, para corresponder ao estado do grafo.

O método **reconnect** tem vários parâmetros opcionais que podem ser usados para especificar o tipo de mídia para a conexão de PIN e o filtro intermediário a ser usado. Por exemplo:


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



Para obter detalhes, consulte a página de referência. Se o método **reconnect** não for flexível o suficiente, você poderá usar o método **reconfigure** , que chama um método de retorno de chamada definido pelo aplicativo para reconectar os Pins. Para usar esse método, implemente a interface [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) em seu aplicativo.

Antes de chamar **reconfigure**, bloqueie o fluxo de dados do pino de saída, conforme descrito anteriormente. Em seguida, envie por push todos os dados que ainda estão pendentes na seção do grafo que você está reconectando, da seguinte maneira:

1.  Chame [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) no pino de entrada mais distante do downstream na cadeia de reconexão (pino D no exemplo). Passe um identificador para um evento do Win32.
2.  Chame [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada que é imediatamente downstream do pino de saída onde você bloqueou o fluxo de dados. (Neste exemplo, o fluxo de dados foi bloqueado no PIN A, portanto, você chamaria **EndOfStream** no pino B.)
3.  Aguarde até que o evento seja sinalizado. O pino de entrada (pino D) sinaliza o evento quando ele recebe a notificação de fim de fluxo. Isso indica que nenhum dado está viajando entre os PINs e que o chamador pode reconectar os Pins com segurança.

Observe que o método **IGraphConfig:: Reconnect** manipula automaticamente as etapas anteriores. Você só precisa executar essas etapas se estiver usando o método **reconfigure** .

Depois que os dados são enviados por push pelo grafo, chame **reconfigure** e passe um ponteiro para sua interface de retorno de chamada do **IGraphConfigCallback** . o filtro Graph Manager chamará o método [**IGraphConfigCallback:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que você forneceu.

**Etapa 3. Desbloquear os dados Flow**

Depois de reconectar os Pins, desbloqueie o fluxo de dados chamando **IPinFlowControl:: Block** com um valor de zero para o primeiro parâmetro.

> [!Note]  
> Se uma reconexão dinâmica for executada por um filtro, haverá alguns problemas de Threading dos quais você deve estar atento. se o filtro Graph Manager tentar parar o filtro, ele poderá ser bloqueado, pois o grafo aguarda que o filtro pare, enquanto, ao mesmo tempo, o filtro pode estar aguardando que os dados sejam enviados por push pelo grafo. Para evitar o deadlock possível, alguns dos métodos descritos nesta seção levam um identificador a um evento do Win32. o filtro deve sinalizar o evento se o filtro Graph Manager tentar parar o filtro. Para obter mais informações, consulte [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[criação de Graph dinâmico](dynamic-graph-building.md)
</dt> </dl>

 

 



