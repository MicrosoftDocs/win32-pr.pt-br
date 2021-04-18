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
# <a name="video-preview"></a>Visualização de vídeo

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como usar o MFPlay para visualizar o vídeo de uma câmera de vídeo.

O MFPlay fornece a maneira mais simples de Microsoft Media Foundation Visualizar o vídeo de um dispositivo de captura. Você deve usar MFPlay se as seguintes condições forem todas verdadeiras:

-   Você não precisa capturar o vídeo em um arquivo.
-   Você não precisa de controle refinado sobre como o vídeo é renderizado. (Por exemplo, você não precisa controlar a criação do dispositivo Direct3D.)
-   Você não precisa processar os dados de vídeo da câmera antes da renderização.

Caso contrário, o [leitor de origem](source-reader.md) pode ser uma opção melhor.

Para usar o MFPlay com um dispositivo de captura de vídeo, execute as seguintes etapas:

1.  Crie uma origem de mídia para o dispositivo de captura. Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Chame [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para criar uma instância do objeto Player.
3.  Chame o método [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) . Passe um ponteiro para a interface IMFMediaSource da origem da mídia. O método recebe um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .
4.  Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a visualização.

O código a seguir mostra estas etapas:


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



Em um aplicativo típico, você forneceria um ponteiro para uma interface de retorno de chamada na função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) e usará a interface de retorno de chamada para obter eventos do Player. Para simplificar, o código mostrado aqui ignora estas etapas. Para obter mais informações, consulte [introdução com MFPlay](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Desligando

Antes de o aplicativo sair, desligue a origem da mídia e o objeto do Player da seguinte maneira:

1.  Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia.
2.  Chame [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) no objeto do Player.


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

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Captura de vídeo](audio-video-capture.md)
</dt> </dl>

 

 



