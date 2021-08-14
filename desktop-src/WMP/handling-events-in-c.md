---
title: Manipulando eventos em C++
description: Manipulando eventos em C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- modelo de objeto Windows Media Player, C++
- modelo de objeto, C++
- Windows Media Player Móvel, C++
- Windows Media Player ActiveX controle, C++
- Windows Media Player controle de ActiveX móvel, C++
- controle de ActiveX, C++
- Incorporação de programa C++
- incorporando, programas em C++
- controle de ActiveX de Windows Media Player, manipulação de eventos
- Windows Media Player controle de ActiveX móvel, manipulação de eventos
- controle de ActiveX, manipulação de eventos
- eventos, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5d50be4622cee9ee455710f8b9d2e4cafc63d6560e08faf5c3deaddcdaccc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748401"
---
# <a name="handling-events-in-c"></a>Manipulando eventos em C++

você pode receber eventos de Windows Media Player de duas maneiras.

-   Por meio de **IDispatch** usando a interface **\_ WMPOCXEvents** . Essa é a interface a ser usada para a maioria dos cenários de inserção.
-   Por meio da interface **IWMPEvents** . essa interface está disponível quando seu código está conectado ao Player de modo completo, como quando o controle de Windows Media Player de comunicação remota ou um plug-in de interface do usuário é remoto.

Em cada cenário, você começa a escutar eventos usando pontos de conexão COM.

O código de exemplo a seguir usa três variáveis de membro:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Para recuperar um ponto de conexão, você primeiro **QueryInterface** para o contêiner de ponto de conexão.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Em seguida, solicite o ponto de conexão para a interface de evento que você deseja usar. O seguinte código de exemplo tenta primeiro usar **IWMPEvents**. Se essa interface não estiver disponível, ela usará **\_ WMPOCXEvents**.


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



Por fim, chame **IConnectionPoint:: Advise** para solicitar eventos.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



No exemplo anterior, o primeiro parâmetro pressupõe que a classe de chamada implemente **IWMPEvents** e **\_ WMPOCXEvents**. O segundo parâmetro é um valor de retorno que você usa para interromper a escuta de eventos, como quando o programa sai, usando um código semelhante ao seguinte:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



A implementação dos manipuladores de eventos para **IWMPEvents** e **\_ WMPOCXEvents** difere. Para **IWMPEvents**, você deve implementar uma função para lidar com cada evento definido pela interface, mesmo que não pretenda usar o evento.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Para implementar manipuladores **\_ WMPOCXEvents** , você deve usar **IDispatch:: Invoke**, que é uma única implementação de manipulador de eventos para todos os eventos que ocorrem na interface **IDispatch** . Isso significa que você pode optar por lidar apenas com determinados eventos e ignorar outros. O código de exemplo a seguir mostra um manipulador **\_ WMPOCXEvents** , usando **Invoke**, que manipula somente os eventos **OpenStateChange** e **PlayStateChange** :


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



No código de exemplo anterior, cada caso simplesmente chama o manipulador **IWMPEvents** para o evento correspondente. Se o código só tratar **\_ WMPOCXEvents**, você poderá simplesmente chamar uma função personalizada ou manipular o evento embutido após a instrução **Case** .

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>recebendo eventos do Windows Media Player 10 Mobile

o controle móvel Windows Media Player 10 dá suporte apenas ao recebimento de determinados eventos por meio de **\_ WMPOCXEvents** e **IWMPEvents**. Para obter mais informações, consulte a documentação do **IWMPEvents**.

## <a name="samples"></a>Exemplos

o pacote de instalação do Windows Media Player instala um exemplo que demonstra a manipulação de eventos. Consulte o exemplo de WMPHost para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**usando o controle Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




