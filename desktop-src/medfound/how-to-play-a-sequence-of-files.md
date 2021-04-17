---
description: Este tópico descreve como reproduzir uma sequência de arquivos de áudio/vídeo usando o MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Como reproduzir uma sequência de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748943"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="fe562-103">Como reproduzir uma sequência de arquivos</span><span class="sxs-lookup"><span data-stu-id="fe562-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="fe562-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fe562-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe562-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fe562-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fe562-106">\]</span><span class="sxs-lookup"><span data-stu-id="fe562-106">\]</span></span>

<span data-ttu-id="fe562-107">Este tópico descreve como reproduzir uma sequência de arquivos de áudio/vídeo usando o MFPlay.</span><span class="sxs-lookup"><span data-stu-id="fe562-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="fe562-108">O tópico [introdução com MFPlay](getting-started-with-mfplay.md) mostra como reproduzir um único arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe562-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="fe562-109">Você também pode usar MFPlay para reproduzir uma sequência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fe562-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="fe562-110">Método síncrono (bloqueio)</span><span class="sxs-lookup"><span data-stu-id="fe562-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="fe562-111">Chame o método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="fe562-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="fe562-112">O método cria um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe562-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="fe562-113">Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para enfileirar o item de mídia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="fe562-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="fe562-114">Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="fe562-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="fe562-115">Essas etapas são mostradas no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe562-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="fe562-116">O método [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="fe562-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="fe562-117">O primeiro parâmetro é a URL do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe562-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="fe562-118">O segundo parâmetro especifica se o método é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="fe562-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="fe562-119">Especificar o valor **true**, como mostrado aqui, faz com que o método seja bloqueado até que o item de mídia seja criado.</span><span class="sxs-lookup"><span data-stu-id="fe562-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="fe562-120">O terceiro parâmetro associa um valor **\_ PTR de DWORD** arbitrário ao item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe562-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="fe562-121">Você pode obter esse valor mais tarde chamando [**IMFPMediaItem:: getuserdata**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span><span class="sxs-lookup"><span data-stu-id="fe562-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="fe562-122">O quarto parâmetro recebe um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe562-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="fe562-123">Método assíncrono (sem bloqueio)</span><span class="sxs-lookup"><span data-stu-id="fe562-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="fe562-124">Evite a opção de bloqueio se você chamar [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) do seu thread de interface do usuário, pois pode levar uma quantidade perceptível de tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="fe562-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="fe562-125">O método normalmente abre um arquivo ou uma conexão de rede e lê dados suficientes para analisar os cabeçalhos de arquivo, que podem levar tempo.</span><span class="sxs-lookup"><span data-stu-id="fe562-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="fe562-126">Portanto, geralmente é melhor definir o segundo parâmetro como **false**.</span><span class="sxs-lookup"><span data-stu-id="fe562-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="fe562-127">Essa opção faz com que o método seja executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fe562-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="fe562-128">Quando a opção assíncrona é usada, o último parâmetro deve ser **nulo**:</span><span class="sxs-lookup"><span data-stu-id="fe562-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="fe562-129">Quando o item de mídia é criado, seu aplicativo recebe um evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ created** .</span><span class="sxs-lookup"><span data-stu-id="fe562-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="fe562-130">A estrutura de dados para esse evento contém um ponteiro para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe562-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="fe562-131">Passe esse ponteiro para o método [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para enfileirar o item para reprodução.</span><span class="sxs-lookup"><span data-stu-id="fe562-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="fe562-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe562-132">Requirements</span></span>

<span data-ttu-id="fe562-133">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe562-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe562-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe562-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe562-135">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="fe562-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



