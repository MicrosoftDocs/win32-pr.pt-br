---
description: Como obter eventos da fonte de rede
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Como obter eventos da fonte de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec85877a928a2f63648ec0dedded1c383988bf80a4182f83062fd296e68bcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958316"
---
# <a name="how-to-get-events-from-the-network-source"></a>Como obter eventos da fonte de rede

O resolvedor de origem permite que um aplicativo crie uma fonte de rede e abra uma conexão com uma URL específica. A fonte de rede gera eventos para marcar o início e o fim da operação assíncrona de abertura de uma conexão. Um aplicativo pode se registrar para esses eventos usando a interface [**IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)

Essa interface expõe o método [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) que a fonte de rede chama diretamente quando abre a URL de forma assíncrona. A origem da rede notifica o aplicativo quando ele começa a abrir a URL ificando o [evento MEConnectStart.](meconnectstart.md) Em seguida, a origem da rede gera [o evento MEConnectEnd](meconnectend.md) quando conclui a operação aberta.

> [!Note]  
> Para enviar esses eventos para o aplicativo, a fonte de rede não usa a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) porque esses eventos são gerados antes da origem da rede ser criada. O aplicativo pode obter todos os outros eventos de origem de rede usando a interface **IMFMediaEventGenerator** da Sessão de Mídia.

 

## <a name="to-get-events-from-the-network-source"></a>Para obter eventos da fonte de rede

1.  Implemente a interface [**IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) Em sua implementação do [**método IMFSourceOpenMonitor::OnSourceEvent,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) faça o seguinte:
    1.  Obter o status do evento chamando [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus). Esse método indica se a operação que disparou o evento, como uma chamada de método resolvedor de origem, foi bem-sucedida. Se a operação não for bem-sucedida, o status será um código de falha.
    2.  Processe o evento com base no tipo de evento: [MEConnectStart](meconnectstart.md) ou [MEConnectEnd](meconnectend.md), que o aplicativo pode obter chamando [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).
2.  Configure um par chave-valor em um objeto de armazenamento de propriedades para armazenar um ponteiro para a implementação [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) descrita na etapa 1.
    1.  Crie um objeto de repositório de propriedades chamando a **função PSCreateMemoryPropertyStore.**
    2.  Definir a [**propriedade MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) em uma **estrutura PROPERTYKEY.**
    3.  Forneça o valor de dados de tipo DESCONHECIDO da VT em uma estrutura PROPVARIANT definindo o ponteiro IUnknown para a implementação do aplicativo da \_ interface [**IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)  
    4.  De definir o par chave-valor no repositório de propriedades chamando **IPropertyStore::SetValue**.
3.  Passe o ponteiro do armazenamento de propriedades para os métodos do resolvedor de origem que o aplicativo está usando para criar a fonte de rede, como [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) e outros.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como implementar a interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) para obter eventos da fonte de rede.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



O exemplo a seguir mostra como definir a [**propriedade \_ MFPKEY SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) na origem da rede quando você abre a URL:


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



