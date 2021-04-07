---
description: Este tópico descreve como reproduzir um segmento de um arquivo de mídia no MFPlay, definindo os horários de início e de parada para reprodução.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Como reproduzir um clipe de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827475"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="b818e-103">Como reproduzir um clipe de arquivo</span><span class="sxs-lookup"><span data-stu-id="b818e-103">How to Play a File Clip</span></span>

<span data-ttu-id="b818e-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b818e-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b818e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b818e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b818e-106">\]</span><span class="sxs-lookup"><span data-stu-id="b818e-106">\]</span></span>

<span data-ttu-id="b818e-107">Este tópico descreve como reproduzir um segmento de um arquivo de mídia no MFPlay, definindo os horários de início e de parada para reprodução.</span><span class="sxs-lookup"><span data-stu-id="b818e-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="b818e-108">**Para reproduzir um clipe de arquivo**</span><span class="sxs-lookup"><span data-stu-id="b818e-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="b818e-109">Chame [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para criar um item de mídia para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b818e-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="b818e-110">Opcionalmente, obtenha a duração total do arquivo, conforme descrito em [como obter a duração da reprodução](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="b818e-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="b818e-111">Chame [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) para definir os horários de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="b818e-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="b818e-112">A hora de parada não deve exceder a duração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b818e-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="b818e-113">Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="b818e-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="b818e-114">O exemplo a seguir usa a versão de bloqueio do [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="b818e-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="b818e-115">Se a versão sem bloqueio for usada, o código que aparece após **CreateMediaItemFromURL** deve ser colocado no manipulador para o evento de **tipo de evento de MFP \_ \_ \_ MEDIAITEM \_ criado** .</span><span class="sxs-lookup"><span data-stu-id="b818e-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="b818e-116">Para obter mais informações sobre eventos em MFPlay, consulte [recebendo eventos do Player](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="b818e-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="b818e-117">Para obter a duração do arquivo, este exemplo chama a `GetPlaybackDuration` função mostrada no tópico [como obter a duração da reprodução](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="b818e-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b818e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b818e-118">Requirements</span></span>

<span data-ttu-id="b818e-119">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b818e-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b818e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b818e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b818e-121">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="b818e-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



