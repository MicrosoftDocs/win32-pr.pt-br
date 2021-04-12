---
title: Adicionando um controle do Windows Media Player inserido
description: Adicionando um controle do Windows Media Player inserido
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Playlists do metarquivo do Windows Media, adicionando controles do Windows Media Player inseridos
- listas de reprodução, adicionando controles do Windows Media Player inseridos
- listas de reprodução de metarquivo, adicionando controles do Windows Media Player inseridos
- Listas de reprodução do metarquivo do Windows Media, controles do Windows Media Player inseridos
- listas de reprodução, controles do Windows Media Player inseridos
- listas de reprodução de metarquivo, controles do Windows Media Player inseridos
- Adicionando controles do Windows Media Player inseridos
- controles do Windows Media Player inseridos
- Windows Media Player, adicionando controles inseridos
- Windows Media Player, controles inseridos
- HTMLView, adicionando controles incorporados do Windows Media Player
- HTMLView, controles do Windows Media Player inseridos
- HTMLView, modelo de objeto do Windows Media Player
- HTMLView, modelo de objeto do Player
- Modelo de objeto do Windows Media Player, sobre
- modelo de objeto, sobre
- Objeto de jogador
- Windows Media, modelo de objeto do Player
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364202"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Adicionando um controle do Windows Media Player inserido

Há dois motivos pelos quais você pode considerar adicionar uma instância incorporada do Windows Media Player à sua apresentação HTMLView. Primeiro, se você quiser exibir conteúdo de vídeo, precisará usar o controle ActiveX do Windows Media Player. Em segundo lugar, se você quiser aproveitar os recursos do modelo de objeto do Windows Media Player de dentro de sua página da Web do HTMLView, deverá usar uma instância do controle de jogador para fazer isso.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Usando o controle Player para exibir o vídeo no conteúdo do HTMLView

Normalmente, o Windows Media Player exibe vídeo usando o painel vídeo e visualização do recurso de **agora em execução** . Como o HTMLView usa essa área para exibir sua página da Web, você deverá fornecer uma área de exibição de vídeo adicional se quiser que o jogador reproduza vídeo. Isso é fácil de usar usando o controle ActiveX do Windows Media Player.

Para usar o controle de jogador para exibir vídeo, incorpore o controle em sua página da Web do HTMLView usando a marca de **objeto** . Essa é a mesma técnica usada para inserir o controle do jogador em qualquer página da Web na qual você deseja exibir o vídeo. O código de exemplo a seguir mostra a sintaxe básica para inserir o controle de jogador no Internet Explorer:


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



O parâmetro *AutoStart* garante que o conteúdo seja reproduzido automaticamente sempre que uma nova URL for especificada. O valor especificado para *UIMODE* depende de você, mas geralmente você desejará especificar "None" ao criar conteúdo para apresentações HtmlView. Quando você insere o controle do Windows Media Player para exibir vídeo dessa maneira, o usuário pode controlar a reprodução usando os controles do player de modo completo, portanto, não há necessidade de fornecer controles de transporte adicionais na página da Web. Você pode usar o espaço que normalmente aloca para controles de transporte para exibir mais texto, gráficos ou links para outro conteúdo.

Não especifique um parâmetro de *URL* ao inserir o controle do Windows Media Player em uma página da Web criada para ser exibida em uma apresentação do HtmlView. Em vez disso, especifique os arquivos de mídia digital no arquivo. asx que abre o conteúdo.

Como você fornece a região de exibição de vídeo em sua página da Web do HTMLView, você pode decidir onde posicionar o vídeo e o tamanho desejado para a região de exibição. Por exemplo, você pode conter o objeto **Player** dentro de um elemento HTML **div** e, em seguida, especificar a posição do **div** para Posicione a exibição do vídeo na página da Web. Você pode alterar as dimensões da exibição do vídeo especificando valores para os atributos Height e Width do elemento **Object** . Você também pode especificar esses valores usando o código de script.

## <a name="using-the-player-object-model"></a>Usando o modelo de objeto do Player

O modelo de objeto do Windows Media Player expõe propriedades, métodos e eventos que você pode usar em suas páginas da Web do HTMLView. Ao inserir o controle ActiveX do Windows Media Player em sua página da Web do HTMLView, você terá acesso automaticamente ao modelo de objeto do Player.

Se você inserir o controle do Windows Media Player em sua página da Web do HTMLView, não use o modelo de objeto do Player para especificar o arquivo de mídia digital a ser reproduzido. Por exemplo, se você usar o código de script para especificar um valor para a propriedade **URL** do controle incorporado, sua página da Web HtmlView será descarregada do recurso em **execução** quando o arquivo de mídia digital for reproduzido. Para evitar que isso aconteça, sempre abra arquivos. asx que incluem parâmetros HTMLView quando você precisa usar o script para abrir o conteúdo de mídia digital na sua página da Web do HTMLView.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Settings. AutoStart**](settings-autostart.md)
</dt> </dl>

 

 




