---
description: Este tópico descreve como obter a duração da reprodução de um arquivo de mídia usando o MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Como obter a duração da reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749955"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="00b19-103">Como obter a duração da reprodução</span><span class="sxs-lookup"><span data-stu-id="00b19-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="00b19-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="00b19-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00b19-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="00b19-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="00b19-106">\]</span><span class="sxs-lookup"><span data-stu-id="00b19-106">\]</span></span>

<span data-ttu-id="00b19-107">Este tópico descreve como obter a duração da reprodução de um arquivo de mídia usando o MFPlay.</span><span class="sxs-lookup"><span data-stu-id="00b19-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="00b19-108">**Para obter a duração da reprodução**</span><span class="sxs-lookup"><span data-stu-id="00b19-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="00b19-109">Chame [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para criar um item de mídia para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="00b19-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="00b19-110">Chame [**IMFPMediaItem:: getDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span><span class="sxs-lookup"><span data-stu-id="00b19-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="00b19-111">Especifique **o \_ PositionType do MFP de \_ 100 NS** para o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="00b19-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="00b19-112">A duração é retornada como um **PROPVARIANT** que contém um **valor \_ inteiro grande** .</span><span class="sxs-lookup"><span data-stu-id="00b19-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="00b19-113">A duração é fornecida em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="00b19-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="00b19-114">O exemplo a seguir mostra a etapa 2:</span><span class="sxs-lookup"><span data-stu-id="00b19-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="00b19-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b19-115">Requirements</span></span>

<span data-ttu-id="00b19-116">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="00b19-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b19-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00b19-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b19-118">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="00b19-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



