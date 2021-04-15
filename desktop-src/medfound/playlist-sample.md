---
description: Exemplo de playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Exemplo de playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761626"
---
# <a name="playlist-sample"></a>Exemplo de playlist

Mostra como usar Microsoft Media Foundation para reproduzir uma sequência de arquivos de áudio em uma lista de reprodução. O exemplo usa a [origem do sequenciador](sequencer-source.md) para criar e gerenciar a lista de reprodução.

> [!Note]  
> Este exemplo não está mais incluído no SDK.

 

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Uso

O exemplo de playlist cria um aplicativo do Windows.

-   Para criar uma nova lista de reprodução, selecione **Adicionar à lista de reprodução** no menu **arquivo** . Na caixa de diálogo **Abrir arquivo** , selecione um ou mais arquivos de áudio. Os arquivos são adicionados à playlist.
-   Para reproduzir a sequência, clique em **reproduzir**.
-   Para pausar o segmento atual, clique em **Pausar**.
-   Para parar o segmento atual, clique em **parar**.
-   Para ignorar um arquivo, clique duas vezes no item na lista de reprodução.
-   Para excluir um arquivo da lista de reprodução, selecione o item na lista de reprodução. Em seguida, selecione **remover da lista de reprodução** no menu **arquivo** .

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local                                                     | Caminho/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [SDK do Windows](https://www.microsoft.com/download/details.aspx?id=8279) | *Raiz* \\ do SDK Exemplos de \\ playlist de multimídia \\ mediafoundation \\ |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 
