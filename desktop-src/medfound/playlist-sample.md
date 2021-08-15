---
description: Exemplo de playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Exemplo de playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cad2ef96c76512947a5b74e7eac54e3ad5787218e625f30fea5b8e5164177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239123"
---
# <a name="playlist-sample"></a>Exemplo de playlist

Mostra como usar o Microsoft Media Foundation para reproduzir uma sequência de arquivos de áudio em uma playlist. O exemplo usa a [Origem do Sequencer](sequencer-source.md) para criar e gerenciar a playlist.

> [!Note]  
> Este exemplo não está mais incluído no SDK.

 

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes Media Foundation interfaces:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Uso

O exemplo playlist cria um Windows aplicativo.

-   Para criar uma nova playlist, selecione **Adicionar à Playlist** no menu Arquivo.  Na caixa **de diálogo Abrir Arquivo,** selecione um ou mais arquivos de áudio. Os arquivos são adicionados à playlist.
-   Para reproduzir a sequência, clique em **Reproduzir**.
-   Para pausar o segmento atual, clique em **Pausar**.
-   Para interromper o segmento atual, clique em **Parar**.
-   Para pular para um arquivo, clique duas vezes no item na playlist.
-   Para excluir um arquivo da playlist, selecione o item na playlist. Em seguida, **selecione Remover da Playlist** no menu Arquivo. 

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local                                                     | Caminho/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [SDK do Windows](https://www.microsoft.com/download/details.aspx?id=8279) | *Raiz do SDK* \\ Playlist de \\ \\ mídia multimídia de exemplos \\ |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Origem do Sequencer](sequencer-source.md)
</dt> </dl>

 

 
