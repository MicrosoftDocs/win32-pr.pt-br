---
description: Importante preterido.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Exemplo de MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827545"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="ff1e0-103">Exemplo de MFPlayer2</span><span class="sxs-lookup"><span data-stu-id="ff1e0-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff1e0-104">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-104">Deprecated.</span></span> <span data-ttu-id="ff1e0-105">Essa API pode ser removida de versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="ff1e0-106">Os aplicativos devem usar a [sessão de mídia](media-session.md) para reprodução.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="ff1e0-107">Demonstra alguns dos recursos de reprodução que são omitidos do exemplo [SimplePlay](simpleplay-sample.md) , como:</span><span class="sxs-lookup"><span data-stu-id="ff1e0-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="ff1e0-108">Atingir</span><span class="sxs-lookup"><span data-stu-id="ff1e0-108">Seeking</span></span>
-   <span data-ttu-id="ff1e0-109">Controle de taxa (avanço rápido e retrocesso)</span><span class="sxs-lookup"><span data-stu-id="ff1e0-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="ff1e0-110">Controles de áudio e áudio</span><span class="sxs-lookup"><span data-stu-id="ff1e0-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="ff1e0-111">Zoom de vídeo</span><span class="sxs-lookup"><span data-stu-id="ff1e0-111">Video zoom</span></span>

<span data-ttu-id="ff1e0-112">A imagem a seguir mostra os controles usados para esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="ff1e0-113">captura de tela do exemplo de mfplayer</span><span class="sxs-lookup"><span data-stu-id="ff1e0-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="ff1e0-114">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="ff1e0-114">APIs Demonstrated</span></span>

<span data-ttu-id="ff1e0-115">Este exemplo demonstra as APIs a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="ff1e0-116">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="ff1e0-117">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="ff1e0-118">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="ff1e0-119">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="ff1e0-120">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="ff1e0-121">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="ff1e0-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="ff1e0-123">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="ff1e0-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="ff1e0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff1e0-124">Requirements</span></span>



| <span data-ttu-id="ff1e0-125">Produto</span><span class="sxs-lookup"><span data-stu-id="ff1e0-125">Product</span></span>                                                        | <span data-ttu-id="ff1e0-126">Versão</span><span class="sxs-lookup"><span data-stu-id="ff1e0-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="ff1e0-127">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="ff1e0-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="ff1e0-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff1e0-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ff1e0-129">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ff1e0-129">Downloading the Sample</span></span>

<span data-ttu-id="ff1e0-130">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span><span class="sxs-lookup"><span data-stu-id="ff1e0-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff1e0-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff1e0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff1e0-132">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ff1e0-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="ff1e0-133">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="ff1e0-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
