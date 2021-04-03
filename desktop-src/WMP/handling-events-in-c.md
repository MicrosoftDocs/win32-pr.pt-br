---
title: Manipulando eventos em C++
description: Manipulando eventos em C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Modelo de objeto do Windows Media Player, C++
- modelo de objeto, C++
- Windows Media Player Mobile, C++
- Controle ActiveX do Windows Media Player, C++
- Controle ActiveX móvel do Windows Media Player, C++
- Controle ActiveX, C++
- Incorporação de programa C++
- incorporando, programas em C++
- Controle ActiveX do Windows Media Player, manipulação de eventos
- Controle ActiveX móvel do Windows Media Player, manipulação de eventos
- Controle ActiveX, manipulação de eventos
- eventos, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084095"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="142e6-116">Manipulando eventos em C++</span><span class="sxs-lookup"><span data-stu-id="142e6-116">Handling Events in C++</span></span>

<span data-ttu-id="142e6-117">Você pode receber eventos do Windows Media Player de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="142e6-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="142e6-118">Por meio de **IDispatch** usando a interface **\_ WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="142e6-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="142e6-119">Essa é a interface a ser usada para a maioria dos cenários de inserção.</span><span class="sxs-lookup"><span data-stu-id="142e6-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="142e6-120">Por meio da interface **IWMPEvents** .</span><span class="sxs-lookup"><span data-stu-id="142e6-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="142e6-121">Essa interface está disponível quando seu código está conectado ao Player de modo completo, como quando você faz a comunicação remota do controle do Windows Media Player ou de um plug-in de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="142e6-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="142e6-122">Em cada cenário, você começa a escutar eventos usando pontos de conexão COM.</span><span class="sxs-lookup"><span data-stu-id="142e6-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="142e6-123">O código de exemplo a seguir usa três variáveis de membro:</span><span class="sxs-lookup"><span data-stu-id="142e6-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="142e6-124">Para recuperar um ponto de conexão, você primeiro **QueryInterface** para o contêiner de ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="142e6-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="142e6-125">Em seguida, solicite o ponto de conexão para a interface de evento que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="142e6-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="142e6-126">O seguinte código de exemplo tenta primeiro usar **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="142e6-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="142e6-127">Se essa interface não estiver disponível, ela usará **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="142e6-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



<span data-ttu-id="142e6-128">Por fim, chame **IConnectionPoint:: Advise** para solicitar eventos.</span><span class="sxs-lookup"><span data-stu-id="142e6-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="142e6-129">No exemplo anterior, o primeiro parâmetro pressupõe que a classe de chamada implemente **IWMPEvents** e **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="142e6-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="142e6-130">O segundo parâmetro é um valor de retorno que você usa para interromper a escuta de eventos, como quando o programa sai, usando um código semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="142e6-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="142e6-131">A implementação dos manipuladores de eventos para **IWMPEvents** e **\_ WMPOCXEvents** difere.</span><span class="sxs-lookup"><span data-stu-id="142e6-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="142e6-132">Para **IWMPEvents**, você deve implementar uma função para lidar com cada evento definido pela interface, mesmo que não pretenda usar o evento.</span><span class="sxs-lookup"><span data-stu-id="142e6-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="142e6-133">Para implementar manipuladores **\_ WMPOCXEvents** , você deve usar **IDispatch:: Invoke**, que é uma única implementação de manipulador de eventos para todos os eventos que ocorrem na interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="142e6-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="142e6-134">Isso significa que você pode optar por lidar apenas com determinados eventos e ignorar outros.</span><span class="sxs-lookup"><span data-stu-id="142e6-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="142e6-135">O código de exemplo a seguir mostra um manipulador **\_ WMPOCXEvents** , usando **Invoke**, que manipula somente os eventos **OpenStateChange** e **PlayStateChange** :</span><span class="sxs-lookup"><span data-stu-id="142e6-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



<span data-ttu-id="142e6-136">No código de exemplo anterior, cada caso simplesmente chama o manipulador **IWMPEvents** para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="142e6-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="142e6-137">Se o código só tratar **\_ WMPOCXEvents**, você poderá simplesmente chamar uma função personalizada ou manipular o evento embutido após a instrução **Case** .</span><span class="sxs-lookup"><span data-stu-id="142e6-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="142e6-138">Recebendo eventos do Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="142e6-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="142e6-139">O controle móvel do Windows Media Player 10 dá suporte apenas ao recebimento de determinados eventos por meio de **\_ WMPOCXEvents** e **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="142e6-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="142e6-140">Para obter mais informações, consulte a documentação do **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="142e6-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="142e6-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="142e6-141">Samples</span></span>

<span data-ttu-id="142e6-142">O pacote de instalação do Windows Media Player instala um exemplo que demonstra a manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="142e6-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="142e6-143">Consulte o exemplo de WMPHost para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="142e6-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="142e6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="142e6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="142e6-145">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="142e6-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="142e6-146">**Usando o controle do Windows Media Player em um programa C++**</span><span class="sxs-lookup"><span data-stu-id="142e6-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




