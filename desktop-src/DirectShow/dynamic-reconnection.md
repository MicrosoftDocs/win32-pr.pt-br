---
description: Reconexão dinâmica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconexão dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456657"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="a0bdc-103">Reconexão dinâmica</span><span class="sxs-lookup"><span data-stu-id="a0bdc-103">Dynamic Reconnection</span></span>

<span data-ttu-id="a0bdc-104">Na maioria dos filtros do DirectShow, os Pins não podem ser reconectados enquanto o grafo está transmitindo dados ativamente.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="a0bdc-105">O aplicativo deve parar o grafo antes de reconectar os Pins.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="a0bdc-106">No entanto, alguns filtros dão suporte a reconexões de PIN enquanto o grafo está em execução, um processo conhecido como reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="a0bdc-107">Isso pode ser feito pelo aplicativo ou por um filtro no grafo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="a0bdc-108">Como exemplo, considere o grafo na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-108">As an example, consider the graph in the following illustration.</span></span>

![gráfico dinâmico-diagrama de construção](images/dyngraph.png)

<span data-ttu-id="a0bdc-110">Um cenário para reconexão dinâmica pode ser remover o filtro 2 do grafo, enquanto o grafo está em execução e substituí-lo por outro filtro.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="a0bdc-111">Para que esse cenário funcione, o seguinte deve ser verdadeiro:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="a0bdc-112">O pino de entrada no filtro 3 (pino D) deve oferecer suporte à interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="a0bdc-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="a0bdc-113">Essa interface permite que o PIN seja reconectado sem interromper o filtro.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="a0bdc-114">O pino de saída no filtro 1 (pino A) deve ser capaz de bloquear o fluxo de dados de mídia enquanto a reconexão ocorre.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="a0bdc-115">Nenhum dado pode viajar entre o pino A e o PIN D durante a reconexão.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="a0bdc-116">Em geral, isso significa que o pino de saída deve dar suporte à interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) .</span><span class="sxs-lookup"><span data-stu-id="a0bdc-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="a0bdc-117">No entanto, se o filtro 1 for o filtro que inicia a reconexão, ele poderá ter um mecanismo interno para bloquear seu próprio fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="a0bdc-118">A reconexão dinâmica envolverá as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="a0bdc-119">Bloquear o fluxo de dados do PIN A.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="a0bdc-120">Reconecte o PIN A ao PIN D, possivelmente por meio de um novo filtro intermediário.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="a0bdc-121">Desbloqueie o PIN A para que os dados comecem a fluir novamente.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="a0bdc-122">**Etapa 1. Bloquear o fluxo de dados**</span><span class="sxs-lookup"><span data-stu-id="a0bdc-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="a0bdc-123">Para bloquear o fluxo de dados, chame [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) no PIN A. Esse método pode ser chamado de forma assíncrona ou síncrona.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="a0bdc-124">Para chamar o método de *forma assíncrona*, crie um objeto de evento do Win32 e passe o identificador de evento para o método **Block** .</span><span class="sxs-lookup"><span data-stu-id="a0bdc-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="a0bdc-125">O método retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-125">The method will return immediately.</span></span> <span data-ttu-id="a0bdc-126">Aguarde até que o evento seja sinalizado, usando uma função como **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="a0bdc-127">O PIN sinaliza o evento quando ele bloqueou o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="a0bdc-128">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-128">For example:</span></span>


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



<span data-ttu-id="a0bdc-129">Para chamar o método de forma *síncrona*, basta passar o valor **NULL** em vez do identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="a0bdc-130">Agora, o método será bloqueado até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="a0bdc-131">Isso pode não acontecer até que o PIN esteja pronto para entregar um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="a0bdc-132">Se o filtro estiver em pausa, isso poderá levar um período arbitrário.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="a0bdc-133">Portanto, não faça a chamada síncrona do seu thread de aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="a0bdc-134">Use um thread de trabalho ou, caso contrário, chame o método de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="a0bdc-135">**Etapa 2. Reconectar os Pins**</span><span class="sxs-lookup"><span data-stu-id="a0bdc-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="a0bdc-136">Para reconectar os Pins, consulte o Gerenciador de gráficos de filtro para a interface **IGraphConfig** e chame [**IGraphConfig:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) ou [**IGraphConfig:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span><span class="sxs-lookup"><span data-stu-id="a0bdc-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="a0bdc-137">O método **reconnect** é mais simples de usar; Ele faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="a0bdc-138">Interrompe os filtros intermediários (filtro 2 no exemplo) e os remove do grafo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="a0bdc-139">Adiciona novos filtros intermediários, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="a0bdc-140">Conecta todos os Pins.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-140">Connects all the pins.</span></span>
-   <span data-ttu-id="a0bdc-141">Pausa ou executa quaisquer filtros novos, para corresponder ao estado do grafo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="a0bdc-142">O método **reconnect** tem vários parâmetros opcionais que podem ser usados para especificar o tipo de mídia para a conexão de PIN e o filtro intermediário a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="a0bdc-143">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-143">For example:</span></span>


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



<span data-ttu-id="a0bdc-144">Para obter detalhes, consulte a página de referência.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-144">For details, consult the reference page.</span></span> <span data-ttu-id="a0bdc-145">Se o método **reconnect** não for flexível o suficiente, você poderá usar o método **reconfigure** , que chama um método de retorno de chamada definido pelo aplicativo para reconectar os Pins.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="a0bdc-146">Para usar esse método, implemente a interface [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="a0bdc-147">Antes de chamar **reconfigure**, bloqueie o fluxo de dados do pino de saída, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="a0bdc-148">Em seguida, envie por push todos os dados que ainda estão pendentes na seção do grafo que você está reconectando, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a0bdc-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="a0bdc-149">Chame [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) no pino de entrada mais distante do downstream na cadeia de reconexão (pino D no exemplo).</span><span class="sxs-lookup"><span data-stu-id="a0bdc-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="a0bdc-150">Passe um identificador para um evento do Win32.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="a0bdc-151">Chame [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada que é imediatamente downstream do pino de saída onde você bloqueou o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="a0bdc-152">(Neste exemplo, o fluxo de dados foi bloqueado no PIN A, portanto, você chamaria **EndOfStream** no pino B.)</span><span class="sxs-lookup"><span data-stu-id="a0bdc-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="a0bdc-153">Aguarde até que o evento seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="a0bdc-154">O pino de entrada (pino D) sinaliza o evento quando ele recebe a notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="a0bdc-155">Isso indica que nenhum dado está viajando entre os PINs e que o chamador pode reconectar os Pins com segurança.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="a0bdc-156">Observe que o método **IGraphConfig:: Reconnect** manipula automaticamente as etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="a0bdc-157">Você só precisa executar essas etapas se estiver usando o método **reconfigure** .</span><span class="sxs-lookup"><span data-stu-id="a0bdc-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="a0bdc-158">Depois que os dados são enviados por push pelo grafo, chame **reconfigure** e passe um ponteiro para sua interface de retorno de chamada do **IGraphConfigCallback** .</span><span class="sxs-lookup"><span data-stu-id="a0bdc-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="a0bdc-159">O Gerenciador de gráfico de filtro chamará o método [**IGraphConfigCallback:: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que você forneceu.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="a0bdc-160">**Etapa 3. Desbloquear o fluxo de dados**</span><span class="sxs-lookup"><span data-stu-id="a0bdc-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="a0bdc-161">Depois de reconectar os Pins, desbloqueie o fluxo de dados chamando **IPinFlowControl:: Block** com um valor de zero para o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="a0bdc-162">Se uma reconexão dinâmica for executada por um filtro, haverá alguns problemas de Threading dos quais você deve estar atento.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="a0bdc-163">Se o Gerenciador do grafo de filtro tentar parar o filtro, ele poderá ser bloqueado, pois o grafo aguardará a interrupção do filtro, enquanto, ao mesmo tempo, o filtro pode estar aguardando que os dados sejam enviados por push pelo grafo.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="a0bdc-164">Para evitar o deadlock possível, alguns dos métodos descritos nesta seção levam um identificador a um evento do Win32.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="a0bdc-165">O filtro deve sinalizar o evento se o Gerenciador do grafo de filtro tentar parar o filtro.</span><span class="sxs-lookup"><span data-stu-id="a0bdc-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="a0bdc-166">Para obter mais informações, consulte [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="a0bdc-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a0bdc-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0bdc-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0bdc-168">Criação de grafo dinâmico</span><span class="sxs-lookup"><span data-stu-id="a0bdc-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



