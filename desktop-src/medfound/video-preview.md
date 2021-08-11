---
description: Este tópico descreve como usar o MFPlay para visualizar o vídeo de uma câmera de vídeo.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Visualização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a58e6c7c70469492ffef38173f0447e19dcf3fe324307e51f3b19609b7d2865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237412"
---
# <a name="video-preview"></a>Visualização de vídeo

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como usar o MFPlay para visualizar o vídeo de uma câmera de vídeo.

O MFPlay fornece a maneira mais simples de Microsoft Media Foundation visualizar o vídeo de um dispositivo de captura. Você deverá usar o MFPlay se as seguintes condições são verdadeiras:

-   Você não precisa capturar o vídeo em um arquivo.
-   Você não precisa de controle fino sobre como o vídeo é renderizado. (Por exemplo, você não precisa controlar a criação do dispositivo Direct3D.)
-   Você não precisa processar os dados de vídeo da câmera antes da renderização.

Caso contrário, [o Leitor de](source-reader.md) Origem pode ser uma opção melhor.

Para usar o MFPlay com um dispositivo de captura de vídeo, execute as seguintes etapas:

1.  Crie uma fonte de mídia para o dispositivo de captura. Consulte [Enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Chame [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para criar uma instância do objeto do player.
3.  Chame o [**método IMFPMediaPlayer::CreateMediaItemFromObject.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) Passe um ponteiro para a interface IMFMediaSource da fonte de mídia. O método recebe um ponteiro para a interface [**IMFPMediaItem.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
4.  Chame [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Chame [**IMFPMediaPlayer::P lay para**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) começar a visualização.

O código a seguir mostra essas etapas:


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



Em um aplicativo típico, você forneceria um ponteiro para uma interface de retorno de chamada na função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) e usaria a interface de retorno de chamada para obter eventos do player. Para simplificar, o código mostrado aqui ignora essas etapas. Para obter mais informações, [consulte Ponto de Partida com MFPlay](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Desligar

Antes que o aplicativo seja encerrado, desligue a fonte de mídia e o objeto do player da seguinte forma:

1.  Chame [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na fonte de mídia.
2.  Chame [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) no objeto do player.


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



## <a name="requirements"></a>Requisitos

O MFPlay requer Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Captura de vídeo](audio-video-capture.md)
</dt> </dl>

 

 



