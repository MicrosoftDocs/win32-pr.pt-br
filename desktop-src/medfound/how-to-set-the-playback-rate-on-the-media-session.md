---
description: Como definir a taxa de reprodução na sessão de mídia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Como definir a taxa de reprodução na sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663779"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="4609b-103">Como definir a taxa de reprodução na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="4609b-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="4609b-104">Para implementar a funcionalidade de reprodução, como avançar e retroceder, talvez os aplicativos precisem alterar a taxa de reprodução de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4609b-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="4609b-105">Media Foundation fornece o serviço de controle de taxa que os aplicativos devem usar para definir a taxa de reprodução dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="4609b-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="4609b-106">Antes de definir a taxa de reprodução, um aplicativo deve verificar se a taxa é suportada pela origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="4609b-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="4609b-107">Para obter informações sobre como consultar as taxas com suporte, consulte [como determinar as taxas com suporte](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="4609b-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="4609b-108">Para obter informações sobre taxas de reprodução, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4609b-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="4609b-109">Para definir a taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="4609b-109">To set the playback rate</span></span>

1.  <span data-ttu-id="4609b-110">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o objeto de controle de taxa da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="4609b-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="4609b-111">Aplicativos que chamam [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devem garantir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4609b-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="4609b-112">O parâmetro *punkObject* contém um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.</span><span class="sxs-lookup"><span data-stu-id="4609b-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="4609b-113">O objeto de controle de taxa recebido no parâmetro *ppvObject* é liberado para evitar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="4609b-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="4609b-114">Chame o método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para definir a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4609b-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="4609b-115">Após a conclusão da **taxa** de execução assíncrona, o aplicativo recebe o evento [MESessionRateChanged](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4609b-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="4609b-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4609b-116">Example</span></span>

<span data-ttu-id="4609b-117">O código a seguir mostra como definir a taxa de reprodução chamando o método [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .</span><span class="sxs-lookup"><span data-stu-id="4609b-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



<span data-ttu-id="4609b-118">O aplicativo deve ser interrompido ou pausado antes que possa fazer uma transição de uma taxa negativa ou zero para uma taxa positiva.</span><span class="sxs-lookup"><span data-stu-id="4609b-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="4609b-119">Para obter informações sobre esses Estados, consulte [como controlar os Estados de apresentação](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="4609b-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4609b-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4609b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4609b-121">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="4609b-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="4609b-122">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="4609b-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="4609b-123">Busca, avanço rápido e reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="4609b-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



