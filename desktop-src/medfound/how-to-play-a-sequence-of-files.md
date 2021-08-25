---
description: Este tópico descreve como reproduzir uma sequência de arquivos de áudio/vídeo usando o MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Como reproduzir uma sequência de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf9cfc6fe48caf5eb185a19ec98ac119fcfbbb78d5e2363bd2db9607a4875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828156"
---
# <a name="how-to-play-a-sequence-of-files"></a>Como reproduzir uma sequência de arquivos

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como reproduzir uma sequência de arquivos de áudio/vídeo usando o MFPlay.


O tópico [Ponto de Partida com MFPlay](getting-started-with-mfplay.md) mostra como reproduzir um único arquivo de mídia. Você também pode usar o MFPlay para reproduzir uma sequência de arquivos.

### <a name="synchronous-blocking-method"></a>Método síncrono (bloqueio)

1.  Chame o [**método IMFPMediaPlayer::CreateMediaItemFromURL.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) O método cria um item de mídia.
2.  Chame [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para colocar o item de mídia na fila para reprodução.
3.  Chame [**IMFPMediaPlayer::P lay para**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) iniciar a reprodução.

Essas etapas são mostradas no código a seguir.


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



O [**método CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) assume os seguintes parâmetros:

-   O primeiro parâmetro é a URL do arquivo.
-   O segundo parâmetro especifica se o método é bloco. Especificar o valor **TRUE**, conforme mostrado aqui, faz com que o método seja bloqueado até que o item de mídia seja criado.
-   O terceiro parâmetro associa um valor **\_ arbitrário de PTR DWORD** ao item de mídia. Você pode obter esse valor posteriormente chamando [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   O quarto parâmetro recebe um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) do item de mídia.

### <a name="asynchronous-non-blocking-method"></a>Método assíncrono (sem bloqueio)

Evite a opção de bloqueio se você chamar [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) do thread da interface do usuário, pois pode levar um tempo perceptível para ser concluído. O método normalmente abre uma conexão de arquivo ou rede e lê dados suficientes para analisar os headers de arquivo, que podem levar tempo. Portanto, geralmente é melhor definir o segundo parâmetro como **FALSE.** Essa opção faz com que o método seja usado de forma assíncrona. Quando a opção assíncrona é usada, o último parâmetro deve ser **NULL:**


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Quando o item de mídia é criado, seu aplicativo recebe um **evento MFP \_ EVENT TYPE \_ \_ MEDIAITEM \_ CREATED.** A estrutura de dados para esse evento contém um ponteiro para o item de mídia. Passe esse ponteiro para o [**método SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para enfilerar o item para reprodução.


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



## <a name="requirements"></a>Requisitos

O MFPlay requer Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



