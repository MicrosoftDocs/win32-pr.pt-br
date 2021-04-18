---
description: Este tópico descreve como usar o MFPlay para visualizar o vídeo de uma câmera de vídeo.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Visualização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807970"
---
# <a name="video-preview"></a><span data-ttu-id="45eb9-103">Visualização de vídeo</span><span class="sxs-lookup"><span data-stu-id="45eb9-103">Video Preview</span></span>

<span data-ttu-id="45eb9-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="45eb9-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="45eb9-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="45eb9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="45eb9-106">\]</span><span class="sxs-lookup"><span data-stu-id="45eb9-106">\]</span></span>

<span data-ttu-id="45eb9-107">Este tópico descreve como usar o MFPlay para visualizar o vídeo de uma câmera de vídeo.</span><span class="sxs-lookup"><span data-stu-id="45eb9-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="45eb9-108">O MFPlay fornece a maneira mais simples de Microsoft Media Foundation Visualizar o vídeo de um dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="45eb9-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="45eb9-109">Você deve usar MFPlay se as seguintes condições forem todas verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="45eb9-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="45eb9-110">Você não precisa capturar o vídeo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45eb9-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="45eb9-111">Você não precisa de controle refinado sobre como o vídeo é renderizado.</span><span class="sxs-lookup"><span data-stu-id="45eb9-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="45eb9-112">(Por exemplo, você não precisa controlar a criação do dispositivo Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="45eb9-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="45eb9-113">Você não precisa processar os dados de vídeo da câmera antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="45eb9-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="45eb9-114">Caso contrário, o [leitor de origem](source-reader.md) pode ser uma opção melhor.</span><span class="sxs-lookup"><span data-stu-id="45eb9-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="45eb9-115">Para usar o MFPlay com um dispositivo de captura de vídeo, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="45eb9-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="45eb9-116">Crie uma origem de mídia para o dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="45eb9-116">Create a media source for the capture device.</span></span> <span data-ttu-id="45eb9-117">Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="45eb9-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="45eb9-118">Chame [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para criar uma instância do objeto Player.</span><span class="sxs-lookup"><span data-stu-id="45eb9-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="45eb9-119">Chame o método [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) .</span><span class="sxs-lookup"><span data-stu-id="45eb9-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="45eb9-120">Passe um ponteiro para a interface IMFMediaSource da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="45eb9-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="45eb9-121">O método recebe um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="45eb9-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="45eb9-122">Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="45eb9-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="45eb9-123">Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a visualização.</span><span class="sxs-lookup"><span data-stu-id="45eb9-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="45eb9-124">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="45eb9-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="45eb9-125">Em um aplicativo típico, você forneceria um ponteiro para uma interface de retorno de chamada na função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) e usará a interface de retorno de chamada para obter eventos do Player.</span><span class="sxs-lookup"><span data-stu-id="45eb9-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="45eb9-126">Para simplificar, o código mostrado aqui ignora estas etapas.</span><span class="sxs-lookup"><span data-stu-id="45eb9-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="45eb9-127">Para obter mais informações, consulte [introdução com MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="45eb9-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="45eb9-128">Desligando</span><span class="sxs-lookup"><span data-stu-id="45eb9-128">Shutting Down</span></span>

<span data-ttu-id="45eb9-129">Antes de o aplicativo sair, desligue a origem da mídia e o objeto do Player da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="45eb9-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="45eb9-130">Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="45eb9-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="45eb9-131">Chame [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) no objeto do Player.</span><span class="sxs-lookup"><span data-stu-id="45eb9-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="45eb9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45eb9-132">Requirements</span></span>

<span data-ttu-id="45eb9-133">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="45eb9-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45eb9-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45eb9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45eb9-135">MFPlay</span><span class="sxs-lookup"><span data-stu-id="45eb9-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="45eb9-136">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="45eb9-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



