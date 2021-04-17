---
description: Como executar a depuração
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Como executar a depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502200"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="bc996-103">Como executar a depuração</span><span class="sxs-lookup"><span data-stu-id="bc996-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="bc996-104">A depuração é executada para buscar instantaneamente pontos específicos dentro de um arquivo interagindo com uma representação visual de tempo, como uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="bc996-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="bc996-105">No Media Foundation, a depuração significa procurar em um arquivo e obter um quadro atualizado.</span><span class="sxs-lookup"><span data-stu-id="bc996-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="bc996-106">Para obter informações sobre a depuração, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="bc996-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="bc996-107">Para executar a depuração</span><span class="sxs-lookup"><span data-stu-id="bc996-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="bc996-108">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="bc996-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="bc996-109">Não obtenha a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="bc996-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="bc996-110">Sempre obtenha a interface da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="bc996-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="bc996-111">Chame [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para definir a taxa de reprodução como zero.</span><span class="sxs-lookup"><span data-stu-id="bc996-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="bc996-112">Para obter mais informações sobre como chamar esse método, consulte [como definir a taxa de reprodução na sessão de mídia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="bc996-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="bc996-113">Crie uma posição de busca em um **PROPVARIANT** especificando o tempo de apresentação a ser buscado em um tipo **MFTIME** .</span><span class="sxs-lookup"><span data-stu-id="bc996-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="bc996-114">Chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) com a posição de busca para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bc996-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="bc996-115">Quando a operação de depuração for concluída, a sessão de mídia enviará um evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="bc996-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="bc996-116">Aguarde esse evento antes de chamar [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) novamente para outra operação de depuração.</span><span class="sxs-lookup"><span data-stu-id="bc996-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="bc996-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bc996-117">Example</span></span>

<span data-ttu-id="bc996-118">O exemplo de código a seguir mostra como executar a depuração.</span><span class="sxs-lookup"><span data-stu-id="bc996-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="bc996-119">Uma operação de depuração bem-sucedida gera o evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) depois que todos os coletores de fluxo são atualizados com o novo quadro e a operação de depuração é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="bc996-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="bc996-120">Depurar um arquivo de vídeo exibe o quadro que foi buscado, mas não gera uma saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="bc996-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="bc996-121">O aplicativo pode executar a revisão do quadro definindo a taxa de reprodução como zero e, em seguida, passando um **PROPVARIANT** que está definido como **VT \_ vazio** na chamada para [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="bc996-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc996-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc996-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc996-123">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="bc996-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="bc996-124">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="bc996-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



