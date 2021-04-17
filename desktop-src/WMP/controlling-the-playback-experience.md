---
title: Controlando a experiência de reprodução
description: Controlando a experiência de reprodução
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Playlists do metarquivo do Windows Media, controlando a reprodução
- listas de reprodução, controlando a reprodução
- listas de reprodução de metarquivo, controlando a reprodução
- Playlists do metarquivo do Windows Media, problemas de reprodução
- listas de reprodução, problemas de reprodução
- listas de reprodução de metarquivo, problemas de reprodução
- controlando a reprodução
- Windows Media Player, controlando a reprodução
- Windows Media Player, problemas de reprodução
- HTMLView, problemas de reprodução
- HTMLView, controle de reprodução
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759729"
---
# <a name="controlling-the-playback-experience"></a>Controlando a experiência de reprodução

Esta seção aborda alguns dos problemas de reprodução que você pode encontrar ao usar o recurso HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Exigindo que o usuário exiba o conteúdo baseado na Web

Você pode decidir que só deseja que os usuários possam desfrutar do conteúdo de mídia digital quando o conteúdo baseado na Web do HTMLView também é exibido. Você pode incluir o código de script em sua página da Web do HTMLView que parará a reprodução do conteúdo de mídia digital se o usuário mudar para o recurso que agora está em **execução** . Para fazer isso, você pode especificar um manipulador de eventos para o evento **Unload** como parte do elemento **Body** , como demonstra o código HTML a seguir:


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



Quando o usuário sai do **momento em execução** clicando em um botão para abrir outro recurso do Windows Media Player, como a biblioteca, o Player fecha o navegador inserido. Isso faz com que o evento **OnUnload** ocorra, executando o script na função chamada **UnloadMe**. O método [Player. Close](player-close.md) interrompe a reprodução e descarrega o arquivo de mídia digital atual. Para exibir o conteúdo novamente, o usuário deve reabrir o arquivo. asx original. Essa técnica também interrompe a reprodução quando o usuário navega para fora da página da Web HTMLView. Observe que essa técnica não pode impedir que o usuário exiba o conteúdo de mídia digital quando ele alterna para o modo de capa.

Você se lembrará de que o parâmetro HTMLView pode ser aplicado a cada elemento de **entrada** em um arquivo. asx. Você pode aproveitar esse recurso para garantir que o conteúdo do HTMLView seja exibido toda vez que um novo arquivo de mídia digital for iniciado. Para fazer isso, associe um elemento **param** para HtmlView com cada entrada na sua lista de reprodução. asx. Quando cada entrada é reproduzida, o Player retorna para o modo completo e exibe o conteúdo de HTMLView especificado na lista de reprodução.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Os tipos de comando de script de URL e arquivo estão desabilitados por padrão

O Windows Media Player 9 Series ou posterior fornece configurações que permitem que o usuário especifique se os comandos de script de tipo de arquivo e URL podem ser executados. Por padrão, ambos os tipos de comando de script não são executados. Se você usar tipos de comando de script personalizados, eles continuarão a ser executados, independentemente da configuração do usuário. Se for necessário usar comandos de script de tipo de URL e de arquivo, você deverá solicitar que o usuário altere as configurações. Para alterar as configurações, clique em **ferramentas**, em **Opções** e em **segurança**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>A reabertura de um HTMLView não recarrega a página da Web

Quando o usuário abre um arquivo. asx que inclui um parâmetro HTMLView e, subsequentemente, reabre o mesmo arquivo, o Windows Media Player não atualiza a página da Web HTMLView. Isso também significa que, se você tiver permitido que os usuários naveguem para longe da página da Web do HTMLView, o Player não retornará o navegador incorporado para a página da Web HTMLView inicial.

## <a name="hiding-the-content-location"></a>Ocultando o local do conteúdo

Você pode decidir que não quer que o Windows Media Player exiba o local do seu conteúdo de mídia digital enquanto ele está reproduzindo um arquivo. asx. Normalmente, o Windows Media Player mostra apenas informações sobre a própria lista de reprodução ao transmitir conteúdo da Internet. No entanto, há outras etapas que você pode executar para impedir que os usuários determinem o local do seu conteúdo. Por exemplo, uma maneira de garantir que o Player não exiba o caminho para seu conteúdo é transmitir seu conteúdo usando as listas de reprodução do lado do servidor dos serviços de mídia do Windows. Dessa forma, quando o usuário exibir as propriedades do conteúdo, ele verá a URL do servidor e não a URL do seu conteúdo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




