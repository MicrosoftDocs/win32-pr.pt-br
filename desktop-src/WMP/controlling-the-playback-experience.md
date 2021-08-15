---
title: Controlando a experiência de reprodução
description: Controlando a experiência de reprodução
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Playlists de metadados de mídia, controlando a reprodução
- playlists, controlando a reprodução
- playlists de metadados, controlando a reprodução
- Windows Playlists de metadados de mídia, problemas de reprodução
- playlists, problemas de reprodução
- playlists de metadados, problemas de reprodução
- controlando a reprodução
- Windows Media Player, controlando a reprodução
- Windows Media Player, problemas de reprodução
- HTMLView, problemas de reprodução
- HTMLView, controlando a reprodução
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341883"
---
# <a name="controlling-the-playback-experience"></a>Controlando a experiência de reprodução

Esta seção aborda alguns dos problemas de reprodução que você pode encontrar ao usar o recurso HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Exigir que o usuário veja o conteúdo baseado na Web

Você pode decidir que só deseja que os usuários possam aproveitar seu conteúdo de mídia digital quando o conteúdo baseado na Web HTMLView também for exibido. Você pode incluir o código de script em sua página da Web HTMLView que interrompe a reprodução do conteúdo de mídia digital se o usuário alterna do **recurso Agora Reproduzir.** Para fazer isso, você pode especificar um manipulador de eventos para o evento **de** descarregamento como parte do elemento **BODY,** como demonstra o código HTML a seguir:


```XML
<BODY onunload = "UnloadMe();">

```



Em seguida, você pode incluir o código de script em sua função de manipulador de eventos para fechar o arquivo no Player. O código de exemplo a seguir faz isso:


```XML
function UnloadMe()
{
   Player.close();
}

```



Quando o usuário alterna para fora do **Now Playing** clicando em um botão para abrir outro recurso de Windows Media Player, como a biblioteca, o Player fecha o navegador inserido. Isso faz com **que o evento onunload** ocorra, executando o script na função chamada **UnloadMe**. O [método Player.close](player-close.md) interrompe a reprodução e descarrega o arquivo de mídia digital atual. Para exibir o conteúdo novamente, o usuário deve reabrir o arquivo .asx original. Essa técnica também interrompe a reprodução quando o usuário navega para fora da página da Web HTMLView. Observe que essa técnica não pode impedir que o usuário veja o conteúdo da mídia digital quando ele alterna para o modo de capa.

Você se lembrará de que o parâmetro HTMLView pode ser aplicado a cada **elemento ENTRY** em um arquivo .asx. Você pode aproveitar esse recurso para garantir que seu conteúdo HTMLView seja exibido sempre que um novo arquivo de mídia digital for iniciado. Para fazer isso, associe **um elemento PARAM** para HTMLView a cada entrada em sua playlist .asx. Quando cada entrada é reproduzida, o Player retorna para o modo completo e exibe o conteúdo HTMLView especificado na playlist.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Os tipos de comando URL e script FILE são desabilitados por padrão

Windows Media Player Série 9 ou posterior fornece configurações que permitem que o usuário especifique se os comandos de script de tipo URL e FILE podem ser executados. Por padrão, esses dois tipos de comando de script não são executados. Se você usar tipos de comando de script personalizados, eles continuarão a ser executados, independentemente da configuração do usuário. Se você precisa usar comandos de script de tipo URL e FILE, você deve solicitar que o usuário altere as configurações. Para alterar as configurações, clique em **Ferramentas**, **opções** e **segurança.**

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>A reabertura de um HTMLView não recarrega a página da Web

Quando o usuário abre um arquivo .asx que inclui um parâmetro HTMLView e, posteriormente, reabre o mesmo arquivo, Windows Media Player atualize a página da Web HTMLView. Isso também significa que, se você tiver permitido que os usuários naveguem para fora de sua página da Web HTMLView, o Player não retornará o navegador inserido para a página inicial do HTMLView.

## <a name="hiding-the-content-location"></a>Ocultando o local do conteúdo

Você pode decidir que não deseja que Windows Media Player o local do conteúdo da mídia digital enquanto ele está sendo exibido em um arquivo .asx. Normalmente, Windows Media Player mostra informações sobre a própria playlist ao transmitir conteúdo da Internet. No entanto, há outras etapas que você pode seguir para impedir que os usuários determinem o local do conteúdo. Por exemplo, uma maneira de garantir que o Player não exibe o caminho para seu conteúdo é transmitir seu conteúdo usando Windows Media Services playlists do lado do servidor. Dessa forma, quando o usuário visualiza as propriedades do conteúdo, ele vê a URL do servidor e não a URL do seu conteúdo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




