---
title: Usando os metaarquivos para alternância de fluxo contínuo
description: Usando os metaarquivos para alternância de fluxo contínuo
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Windows Playlists de metarquivo de mídia, alternância de fluxo de eventos ao vivo
- listas de reprodução, alternância de fluxo de eventos ao vivo
- listas de reprodução de metarquivo, alternância de fluxo de eventos ao vivo
- Windows Playlists de metarquivo de mídia, alternância de fluxo de eventos
- listas de reprodução, alternância de fluxo de eventos
- listas de reprodução de metarquivo, alternância de fluxo de eventos
- Windows Playlists de metarquivo de mídia, inserção de anúncio
- listas de reprodução, inserção de anúncio
- listas de reprodução de metarquivo, inserção de anúncio
- Windows Media Player, alternância de fluxo de eventos ao vivo
- Windows Media Player, alternância de fluxo de eventos
- Windows Media Player, inserção do ad
- alternância de fluxo de eventos ao vivo
- alternância de fluxo de eventos
- inserção de anúncio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4efc4a23f0464446675d9de20d57750bd230d2eef26d31714e2129e380ae9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001566"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Usando os metaarquivos para alternância de fluxo contínuo

Você pode facilitar a alternância de fluxo contínuo usando listas de reprodução de metarquivo. Normalmente, quando uma parte do conteúdo termina, o buffer ocorre no próximo clipe ou fluxo antes de ser aberto (se for o conteúdo recebido de um servidor de mídia de streaming). o Microsoft Windows Media Services permite eliminar, ou pelo menos minimizar, esse tempo de buffer e ter outra parte do conteúdo em fluxo começa a ser executada quase imediatamente. o modo normal de operação para Windows Media Player é abrir o próximo fluxo de mídia referenciado pela playlist 20 segundos antes do final do fluxo processado no momento. Isso geralmente fornece uma transição direta entre fluxos de mídia, dependendo de outros fatores, como tempos de acesso à Web.

Use o elemento **Event** em uma playlist em conjunto com comandos OpenEvent do codificador para facilitar a alternância direta entre fluxos ou arquivos. O envio de um comando OPENEVENT de 20 segundos ou mais antes do comando de evento pode minimizar atrasos na alternância de fluxo. em seguida, Windows Media Player é capaz de pré-carregar uma parte do próximo conteúdo de streaming em um buffer.

Use Windows o codificador de mídia para enviar um comando de script no fluxo usando o seguinte formato:


```XML
OPENEVENT eventname 

```



O nome do evento deve ser aquele definido no elemento **Event** na playlist. quando Windows Media Player recebe um comando de script OPENEVENT do codificador, ele procura o elemento **event** na lista de reprodução e começa a armazenar em buffer o clipe ou fluxo definido no elemento **event** . Windows Media Player, em seguida, mantém essas informações até o evento real de mesmo nome. quando o evento nomeado é recebido, Windows Media Player alterna para o conteúdo anteriormente armazenado em buffer.

> [!Note]  
> Você não pode usar caracteres Unicode para o comando de script OPENEVENT no arquivo de mídia ou no elemento de **evento** na lista de reprodução.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metarquivo de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




