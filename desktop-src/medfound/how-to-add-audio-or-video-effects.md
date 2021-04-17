---
description: Este tópico descreve como usar efeitos de áudio/vídeo com o MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Como adicionar efeitos de áudio ou vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798050"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="7ce54-103">Como adicionar efeitos de áudio ou vídeo</span><span class="sxs-lookup"><span data-stu-id="7ce54-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="7ce54-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="7ce54-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ce54-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7ce54-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7ce54-106">\]</span><span class="sxs-lookup"><span data-stu-id="7ce54-106">\]</span></span>

<span data-ttu-id="7ce54-107">Este tópico descreve como usar efeitos de áudio/vídeo com o MFPlay.</span><span class="sxs-lookup"><span data-stu-id="7ce54-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="7ce54-108">Para usar um efeito com MFPlay, o efeito deve ser implementado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="7ce54-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="7ce54-109">Para obter mais informações, consulte [transformações de Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="7ce54-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="7ce54-110">**Para adicionar um efeito de áudio ou vídeo**</span><span class="sxs-lookup"><span data-stu-id="7ce54-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="7ce54-111">Crie uma instância do MFT que implemente o efeito.</span><span class="sxs-lookup"><span data-stu-id="7ce54-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="7ce54-112">Chame [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span><span class="sxs-lookup"><span data-stu-id="7ce54-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="7ce54-113">Chame [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) antes de abrir o arquivo de mídia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="7ce54-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="7ce54-114">MFPlay determina automaticamente se o efeito é um efeito de vídeo ou de áudio.</span><span class="sxs-lookup"><span data-stu-id="7ce54-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="7ce54-115">O método [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) também usa um parâmetro booliano que especifica se o efeito é opcional ou obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7ce54-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="7ce54-116">Se MFPlay não puder adicionar um efeito necessário (por exemplo, porque o formato do fluxo é incompatível), ocorrerá um erro de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7ce54-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="7ce54-117">Na maioria dos casos, é melhor definir um efeito como opcional.</span><span class="sxs-lookup"><span data-stu-id="7ce54-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="7ce54-118">MFPlay continua a usar o efeito para toda a reprodução subsequente.</span><span class="sxs-lookup"><span data-stu-id="7ce54-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="7ce54-119">Para remover o efeito, chame [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) ou [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span><span class="sxs-lookup"><span data-stu-id="7ce54-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="7ce54-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce54-120">Requirements</span></span>

<span data-ttu-id="7ce54-121">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7ce54-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ce54-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ce54-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ce54-123">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="7ce54-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



