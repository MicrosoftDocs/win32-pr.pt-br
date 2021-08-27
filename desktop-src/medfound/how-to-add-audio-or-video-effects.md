---
description: Este tópico descreve como usar efeitos de áudio/vídeo com o MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Como adicionar efeitos de áudio ou vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af2bb310ab4818cac5dd2804d2bb696c284fdd868d916e4e543a205328e909e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061546"
---
# <a name="how-to-add-audio-or-video-effects"></a>Como adicionar efeitos de áudio ou vídeo

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como usar efeitos de áudio/vídeo com o MFPlay.

Para usar um efeito com MFPlay, o efeito deve ser implementado como uma Media Foundation transformação (MFT). Para obter mais informações, consulte [transformações de Media Foundation](media-foundation-transforms.md).

**Para adicionar um efeito de áudio ou vídeo**

1.  Crie uma instância do MFT que implemente o efeito.
2.  Chame [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Chame [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) antes de abrir o arquivo de mídia para reprodução. MFPlay determina automaticamente se o efeito é um efeito de vídeo ou de áudio.

O método [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) também usa um parâmetro booliano que especifica se o efeito é opcional ou obrigatório. Se MFPlay não puder adicionar um efeito necessário (por exemplo, porque o formato do fluxo é incompatível), ocorrerá um erro de reprodução. Na maioria dos casos, é melhor definir um efeito como opcional.

MFPlay continua a usar o efeito para toda a reprodução subsequente. Para remover o efeito, chame [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) ou [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


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



## <a name="requirements"></a>Requisitos

MFPlay requer Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



