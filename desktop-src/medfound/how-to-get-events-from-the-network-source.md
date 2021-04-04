---
description: Como obter eventos da fonte de rede
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Como obter eventos da fonte de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647670"
---
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="91936-103">Como obter eventos da fonte de rede</span><span class="sxs-lookup"><span data-stu-id="91936-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="91936-104">O resolvedor de origem permite que um aplicativo crie uma fonte de rede e abra uma conexão com uma URL específica.</span><span class="sxs-lookup"><span data-stu-id="91936-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="91936-105">A origem da rede gera eventos para marcar o início e o fim da operação assíncrona de abrir uma conexão.</span><span class="sxs-lookup"><span data-stu-id="91936-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="91936-106">Um aplicativo pode se registrar para esses eventos usando a interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="91936-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="91936-107">Essa interface expõe o método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) que a origem da rede chama diretamente quando abre a URL de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="91936-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="91936-108">A origem da rede notifica o aplicativo quando ele começa a abrir a URL, gerando o evento [MEConnectStart](meconnectstart.md) .</span><span class="sxs-lookup"><span data-stu-id="91936-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="91936-109">Em seguida, a origem da rede gera o evento [MEConnectEnd](meconnectend.md) quando conclui a operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="91936-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="91936-110">Para enviar esses eventos para o aplicativo, a origem da rede não usa a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) porque esses eventos são gerados antes da criação da fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="91936-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="91936-111">O aplicativo pode obter todos os outros eventos de origem da rede usando a interface **IMFMediaEventGenerator** da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="91936-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="91936-112">Para obter eventos da fonte de rede</span><span class="sxs-lookup"><span data-stu-id="91936-112">To get events from the network source</span></span>

1.  <span data-ttu-id="91936-113">Implemente a interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="91936-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="91936-114">Em sua implementação do método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="91936-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="91936-115">Obtenha o status do evento chamando [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span><span class="sxs-lookup"><span data-stu-id="91936-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="91936-116">Esse método indica se a operação que disparou o evento, como uma chamada de método de resolvedor de origem, teve êxito.</span><span class="sxs-lookup"><span data-stu-id="91936-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="91936-117">Se a operação não for bem-sucedida, o status será um código de falha.</span><span class="sxs-lookup"><span data-stu-id="91936-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="91936-118">Processe o evento com base no tipo de evento: [MEConnectStart](meconnectstart.md) ou [MEConnectEnd](meconnectend.md), que o aplicativo pode obter chamando [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span><span class="sxs-lookup"><span data-stu-id="91936-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="91936-119">Configure um par chave-valor em um objeto de repositório de propriedades para armazenar um ponteiro para a implementação [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) descrita na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="91936-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="91936-120">Crie um objeto de repositório de propriedades chamando a função **PSCreateMemoryPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="91936-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="91936-121">Defina a propriedade [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) em uma estrutura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="91936-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="91936-122">Forneça o \_ valor de dados de tipo desconhecido de VT em uma estrutura **PROPVARIANT** definindo o ponteiro **IUnknown** para a implementação do aplicativo da interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="91936-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="91936-123">Defina o par chave-valor no repositório de propriedades chamando **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="91936-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="91936-124">Passe o ponteiro do repositório de propriedades para os métodos do resolvedor de origem que o aplicativo está usando para criar a origem da rede, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) e outros.</span><span class="sxs-lookup"><span data-stu-id="91936-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="91936-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="91936-125">Example</span></span>

<span data-ttu-id="91936-126">O exemplo a seguir mostra como implementar a interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) para obter eventos da origem da rede.</span><span class="sxs-lookup"><span data-stu-id="91936-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="91936-127">O exemplo a seguir mostra como definir a propriedade [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) na origem da rede quando você abre a URL:</span><span class="sxs-lookup"><span data-stu-id="91936-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="91936-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91936-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91936-129">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91936-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



