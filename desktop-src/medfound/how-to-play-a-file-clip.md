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
# <a name="how-to-play-a-file-clip"></a>Como reproduzir um clipe de arquivo

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como reproduzir um segmento de um arquivo de mídia no MFPlay, definindo os horários de início e de parada para reprodução.

**Para reproduzir um clipe de arquivo**

1.  Chame [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para criar um item de mídia para o arquivo.
2.  Opcionalmente, obtenha a duração total do arquivo, conforme descrito em [como obter a duração da reprodução](how-to-get-the-playback-duration.md).
3.  Chame [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) para definir os horários de início e de parada. A hora de parada não deve exceder a duração do arquivo.
4.  Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para iniciar a reprodução.

O exemplo a seguir usa a versão de bloqueio do [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl). Se a versão sem bloqueio for usada, o código que aparece após **CreateMediaItemFromURL** deve ser colocado no manipulador para o evento de **tipo de evento de MFP \_ \_ \_ MEDIAITEM \_ criado** . Para obter mais informações sobre eventos em MFPlay, consulte [recebendo eventos do Player](getting-started-with-mfplay.md).

Para obter a duração do arquivo, este exemplo chama a `GetPlaybackDuration` função mostrada no tópico [como obter a duração da reprodução](how-to-get-the-playback-duration.md).


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



## <a name="requirements"></a>Requisitos

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



