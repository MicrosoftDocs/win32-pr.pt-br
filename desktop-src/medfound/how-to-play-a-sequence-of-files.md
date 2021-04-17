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
# <a name="how-to-play-a-sequence-of-files"></a>Como reproduzir uma sequência de arquivos

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como reproduzir uma sequência de arquivos de áudio/vídeo usando o MFPlay.


O tópico [introdução com MFPlay](getting-started-with-mfplay.md) mostra como reproduzir um único arquivo de mídia. Você também pode usar MFPlay para reproduzir uma sequência de arquivos.

### <a name="synchronous-blocking-method"></a>Método síncrono (bloqueio)

1.  Chame o método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . O método cria um item de mídia.
2.  Chame [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para enfileirar o item de mídia para reprodução.
3.  Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a reprodução.

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



O método [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) usa os seguintes parâmetros:

-   O primeiro parâmetro é a URL do arquivo.
-   O segundo parâmetro especifica se o método é bloqueado. Especificar o valor **true**, como mostrado aqui, faz com que o método seja bloqueado até que o item de mídia seja criado.
-   O terceiro parâmetro associa um valor **\_ PTR de DWORD** arbitrário ao item de mídia. Você pode obter esse valor mais tarde chamando [**IMFPMediaItem:: getuserdata**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   O quarto parâmetro recebe um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) do item de mídia.

### <a name="asynchronous-non-blocking-method"></a>Método assíncrono (sem bloqueio)

Evite a opção de bloqueio se você chamar [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) do seu thread de interface do usuário, pois pode levar uma quantidade perceptível de tempo para ser concluída. O método normalmente abre um arquivo ou uma conexão de rede e lê dados suficientes para analisar os cabeçalhos de arquivo, que podem levar tempo. Portanto, geralmente é melhor definir o segundo parâmetro como **false**. Essa opção faz com que o método seja executado de forma assíncrona. Quando a opção assíncrona é usada, o último parâmetro deve ser **nulo**:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Quando o item de mídia é criado, seu aplicativo recebe um evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ created** . A estrutura de dados para esse evento contém um ponteiro para o item de mídia. Passe esse ponteiro para o método [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para enfileirar o item para reprodução.


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

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



