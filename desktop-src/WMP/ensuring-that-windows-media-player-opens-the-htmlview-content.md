---
title: Garantindo que o Windows Media Player Abra o conteúdo do HTMLView
description: Garantindo que o Windows Media Player Abra o conteúdo do HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Listas de reprodução do metarquivo do Windows Media, Windows Media Player abrindo conteúdo do HTMLView
- listas de reprodução, Windows Media Player abrindo conteúdo do HTMLView
- listas de reprodução de metarquivo, Windows Media Player abrindo conteúdo HTMLView
- Playlists do metarquivo do Windows Media, abrindo conteúdo do HTMLView
- listas de reprodução, abrindo conteúdo do HTMLView
- listas de reprodução de metarquivo, abrindo conteúdo de HTMLView
- abrindo conteúdo do HTMLView
- Windows Media Player, abrindo conteúdo do HTMLView
- Windows Media Player, conteúdo do HTMLView
- HTMLView, abrindo conteúdo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636060"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>Garantindo que o Windows Media Player Abra o conteúdo do HTMLView

Atualmente, o Windows Media Player 9 Series e o Windows Media Player 10 são os únicos players que oferecem suporte ao parâmetro *HtmlView* em arquivos. asx. Isso significa que você deve tomar medidas para garantir que o conteúdo do HTMLView seja reproduzido nessas versões do Windows Media Player.

Primeiro, você deve determinar se o Windows Media Player 9 Series ou o Windows Media Player 10 está instalado no computador do usuário. O SDK do Windows Media Player inclui um exemplo abrangente que demonstra como detectar diferentes versões do Windows Media Player em diferentes navegadores da Web. Embora uma análise completa da amostra de detecção esteja além do escopo desta seção, há algumas etapas básicas que podem ser seguidas para determinar qual versão do Windows Media Player o computador do usuário está executando.

Em sua forma mais simples, detectar o Windows Media Player envolve inserir o controle do jogador na página da Web que vincula ao conteúdo do HTMLView e, em seguida, inspecionando o valor recuperado pelo *Player*. Propriedade **versionInfo** . Depois de verificar se o usuário tem o Windows Media Player 9 Series ou o Windows Media Player 10 instalado, você pode usar o método [Player. openPlayer](player-openplayer.md) para abrir o conteúdo no player de modo completo. O método **openPlayer** garante que seu conteúdo seja inicialmente exibido no recurso em **execução** do player de modo completo, em vez de em uma capa, no modo de mini Player ou em outro player que se registrou como programa padrão para arquivos com uma extensão de nome de arquivo. ASX, mas não dá suporte a HtmlView. No entanto, quando o conteúdo é exibido, o usuário tem o controle total do Windows Media Player, o que significa que ele pode optar por exibir um recurso diferente de **agora em execução**, alternar para o modo de capa ou até mesmo sair do Player.

O código de exemplo a seguir cria uma página da Web para o Internet Explorer. Essa página abre um arquivo. ASX, que especifica uma página da Web HTMLView que aparece no player de modo completo quando o Windows Media Player 9 Series ou posterior está instalado.


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



O código no exemplo anterior incorpora o controle do Windows Media Player com a propriedade **UIMODE** definida como "invisível" e os atributos de altura e largura do Player são definidos como zero. Isso ocorre porque a página da Web não exige que a interface do usuário de controle do jogador seja exibida inicialmente — ela só requer acesso ao modelo de objeto do Player. A página também exibe um botão de entrada que permite ao usuário reproduzir o arquivo. asx.

Quando o usuário clica no botão reproduzir ASX, a função PlayASX do Microsoft JScript é executada. Essa função primeiro recupera o valor para a propriedade **versionInfo** do Player, usando o método **parseInt** do JScript para inspecionar o valor numérico da cadeia de caracteres recuperada. Se o valor numérico for maior ou igual a 9 (o que significa que o usuário tem o Windows Media Player 9 Series instalado), o código do script chamará o método **openPlayer** , passando a URL do arquivo. asx que contém o parâmetro HtmlView. Esse método abre o arquivo. asx usando o Windows Media Player no modo completo, desempenha o conteúdo de mídia digital na lista de reprodução. ASX e exibe o conteúdo baseado na Web do HTMLView no recurso de **agora em execução** .

Se o valor numérico da cadeia de caracteres da versão não for maior ou igual a 9 (o que significa que o usuário não tem o Windows Media Player 9 Series ou posterior instalado em seu computador), o código de script altera o **UIMODE** do controle Player para "Full", define uma nova largura e altura para o controle e, em seguida, abre o arquivo. ASX no player incorporado especificando um valor para a propriedade **URL** . Quando isso acontece, o conteúdo de mídia digital é executado na página da Web, mas todos os valores de HTMLView especificados no arquivo. asx são ignorados.

Como o conteúdo é reproduzido quando o usuário não tem o Windows Media Player 9 Series ou o Windows Media Player 10 instalado cabe a você. O exemplo anterior mostra como especificar que o conteúdo é tocado na página da Web em vez do player de modo completo, ignorando qualquer conteúdo de HTMLView no processo. Há outras abordagens que você pode tomar. Por exemplo, você pode solicitar que o usuário instale uma versão mais recente do Windows Media Player, tornando essa versão do Player um requisito para reproduzir seu conteúdo de mídia digital.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




