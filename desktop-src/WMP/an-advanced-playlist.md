---
title: Uma lista de reprodução avançada
description: Uma lista de reprodução avançada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Listas de reprodução do metarquivo do Windows Media, exemplos de playlist
- listas de reprodução, exemplos de playlist
- listas de reprodução de metarquivo, exemplos de playlist
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, exemplos de listas de reprodução
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, listas de reprodução de exemplo
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, exemplo de código
- listas de reprodução, exemplo de código
- listas de reprodução de metarquivo, exemplo de código
- Playlists do metarquivo do Windows Media, exemplo de playlist avançada
- listas de reprodução, exemplo de playlist avançada
- playlists de metarquivo, exemplo de playlist avançada
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist avançada
- exemplos de playlist
- exemplos de playlist
- listas de reprodução de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005308"
---
# <a name="an-advanced-playlist"></a>Uma lista de reprodução avançada

O exemplo de playlist a seguir mostra como usar um conjunto mais completo de elementos de playlist. Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivos para nomes de arquivos válidos que sejam acessíveis ao seu Windows Media Player.

Código de exemplo


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



A tabela a seguir descreve a lista de reprodução avançada anterior.



| Linha                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | O elemento [ASX](asx-element.md) identifica o cliente do (Windows Media Player) que esta é uma lista de reprodução do metarquivo do Windows Media. O atributo **version** especifica o número de versão dos elementos de metarquivo.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | O elemento [title](title-element--metafile.md) identifica o título da lista de reprodução como um todo. O Windows Media Player exibe esses metadados como o título de exibição.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | O elemento [abstract](abstract-element.md) fornece a dica de ferramenta para o título show.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | O elemento [moreinfo](moreinfo-element.md) vincula o título de mostrar a uma URL. Pausar o ponteiro do mouse sobre o título mostrar acessa a dica de ferramenta, se definido. Selecionar o título mostrar irá abrir a URL designada.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | O elemento [banner](banner-element.md) cria uma faixa de anúncio no Windows Media Player. O atributo **href** especifica o gráfico de faixa (que deve ter de 194 pixels de largura por 32 pixels de altura).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | O elemento [abstract](abstract-element.md) fornece a dica de ferramenta para a **faixa**.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | O elemento [moreinfo](moreinfo-element.md) vincula o gráfico de **faixa** a uma URL. Manter o ponteiro do mouse sobre a **faixa** acessa uma dica de ferramenta, se definido. A seleção da **faixa** abrirá a URL designada.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | O elemento [param](param-element.md) define um parâmetro personalizado. O atributo **Name** define o nome do parâmetro personalizado como "Track". O atributo **Value** define o valor de "Track" como "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Fecha o elemento de **faixa**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Inicia o bloco do elemento de [entrada](entry-element.md) . Esse elemento define um clipe em uma lista de reprodução especificando um link no elemento **ref** . Definir **ClientSkip** como "não" significa que o usuário não pode avançar ou ir para o próximo clipe                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Cria uma faixa de anúncio. O **href** é o gráfico de faixa (194x32 pixels).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Fornece a dica de ferramenta para a faixa.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornece um link para a URL da faixa. A seleção da faixa se conecta à URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Fecha o elemento de **faixa**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornece um link para a URL do texto do **título** do clipe.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Um comentário. Os [comentários](comments.md) só estarão visíveis quando o código for exibido.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Fornece a dica de ferramenta para o texto do **título** do clipe.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica o título do clipe. É o **título** do clipe porque ele está aninhado dentro de um elemento de **entrada** . O Windows Media Player exibe esses metadados como o título do clipe.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica o autor do clipe de mídia. Esses metadados são exibidos como o **autor** do clipe pelo Windows Media Player.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | O elemento de [direitos autorais](copyright-element.md) especifica os direitos autorais associados ao clipe de mídia. O Windows Media Player exibe esses metadados como o clipe COPYRIGHT.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Um comentário, no mesmo formato que comentários **XML** .                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL para o conteúdo de mídia. O elemento [ref](ref-element.md) identifica a linha como um ponteiro para conteúdo de mídia. O atributo **href** é a URL para o arquivo. Observe o uso do fechamento do tipo XML do elemento "/>" em vez de " &lt; /ref &gt; ". Como esse elemento não tem elementos filho, ele se fecha.<br/> |
| `</ENTRY>`                                                                                  | Especifica o final do primeiro elemento de **entrada** .                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Inicia o segundo elemento de **entrada** .                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica o título do segundo clipe.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica o autor do segundo clipe de mídia.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Um comentário. Ele só ficará visível quando o código for exibido.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Este é o texto de dica de ferramenta para o texto do **título** do clipe.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Um comentário. Ele só ficará visível quando o código for exibido.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica a linha como um ponteiro para conteúdo de mídia. O atributo **href** é a URL para o arquivo.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Especifica o final do segundo elemento de **entrada** .                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Especifica o fim da lista de reprodução.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Exemplos de playlist**](example-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





