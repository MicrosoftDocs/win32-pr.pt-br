---
title: Uma playlist avançada
description: Uma playlist avançada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows Playlists de metadados de mídia, exemplos de playlist
- playlists, exemplos de playlist
- playlists de metadados, exemplos de playlist
- Windows Playlists de metadados de mídia, playlists de exemplo
- playlists, playlists de exemplo
- playlists de metadados, playlists de exemplo
- Windows Playlists de metadados de mídia, playlists de exemplo
- playlists, playlists de exemplo
- playlists de metadados, playlists de exemplo
- Windows Playlists de metadados de mídia, exemplo de código
- playlists, exemplo de código
- playlists de metadados, exemplo de código
- Windows Playlists de metadados de mídia, exemplo de playlist avançada
- playlists, exemplo de playlist avançada
- playlists de metadados, exemplo de playlist avançada
- Windows Media Player,exemplos de playlist
- Windows Media Player, exemplos de playlists
- Windows Media Player, playlists de exemplo
- Windows Media Player exemplo de playlist avançada
- exemplos de playlist
- exemplos de playlists
- playlists de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583253"
---
# <a name="an-advanced-playlist"></a>Uma playlist avançada

O exemplo de playlist a seguir mostra como usar um conjunto mais completo de elementos de playlist. Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivo para nomes de arquivo válidos acessíveis ao seu Windows Media Player.

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



A tabela a seguir descreve a playlist avançada anterior.



| Linha                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | O [elemento ASX](asx-element.md) identifica para o cliente (Windows Media Player) que esta é uma playlist Windows metadados de mídia. O **atributo** version especifica o número de versão dos elementos de metadados.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | O [elemento TITLE](title-element--metafile.md) identifica o título da playlist como um todo. Windows Media Player exibe os metadados como o título show.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | O [elemento ABSTRACT](abstract-element.md) fornece a Dica de Ferramenta para o título show.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | O [elemento MOREINFO](moreinfo-element.md) vincula o título show a uma URL. Pausar o ponteiro do mouse sobre o título show acessa a Dica de Ferramenta, se definido. Selecionar o título mostrar abrirá a URL designada.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | O [elemento BANNER](banner-element.md) cria uma faixa de anúncio Windows Media Player. O **atributo HREF** especifica o gráfico de faixa (que deve ter 194 pixels de largura por 32 pixels de altura).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | O [elemento ABSTRACT](abstract-element.md) fornece a Dica de Ferramenta para o **BANNER.**                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | O [elemento MOREINFO](moreinfo-element.md) vincula o **gráfico BANNER** a uma URL. Manter o ponteiro do mouse sobre **o BANNER** acessa uma Dica de Ferramenta, se definido. Selecionar a **FAIXA** abrirá a URL designada.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | O [elemento PARAM](param-element.md) define um parâmetro personalizado. O **atributo** name define o nome do parâmetro personalizado como "track". O **atributo** value define o valor de "track" como "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Fecha o **elemento BANNER**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Inicia o bloco [de elemento ENTRY.](entry-element.md) Esse elemento define um clipe em uma playlist especificando um link no **elemento REF.** Definir **ClientSkip** como "não" significa que o usuário não pode avançar ou ir para o próximo clipe                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Cria uma faixa de anúncio. O **HREF** é o gráfico de faixa (194 x 32 pixels).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Fornece a Dica de Ferramenta para a faixa.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornece um link para a URL da faixa. Selecionar a faixa conecta-se à URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Fecha o **elemento BANNER**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornece um link para a URL para o texto título **do** clipe.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Um comentário. [Os](comments.md) comentários só ficam visíveis quando o código é exibido.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Fornece a Dica de Ferramenta para o texto **título do** clipe.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica o título do clipe. É o **título** do clipe porque ele está aninhado dentro de um **elemento ENTRY.** Windows Media Player exibe os metadados como o título do clipe.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica o autor do clipe de mídia. Os metadados são exibidos como o clipe **AUTHOR** por Windows Media Player.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | O [elemento COPYRIGHT](copyright-element.md) especifica os direitos autorais associados ao clipe de mídia. Windows Media Player exibe os metadados como o clipe COPYRIGHT.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Um comentário, no mesmo formato que comentários **XML.**                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL para o conteúdo da mídia. O [elemento REF](ref-element.md) identifica a linha como um ponteiro para o conteúdo da mídia. O **atributo HREF** é a URL para o arquivo. Observe o uso do fechamento como XML do elemento , "/>" em vez de " &lt; /REF &gt; ". Como esse elemento não tem elementos filho, ele se fecha.<br/> |
| `</ENTRY>`                                                                                  | Especifica o final do do primeiro **elemento ENTRY.**                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Inicia o segundo **elemento ENTRY.**                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica o título do segundo clipe.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica o autor do segundo clipe de mídia.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Um comentário. Ele só ficará visível quando o código for exibido.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Este é o texto da Dica de Ferramenta para **o texto TITLE** do clipe.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Um comentário. Ele só ficará visível quando o código for exibido.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica a linha como um ponteiro para o conteúdo da mídia. O **atributo HREF** é a URL para o arquivo.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Especifica o final do segundo **elemento ENTRY.**                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Especifica o final da playlist.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando playlists de metadados**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de exemplo**](example-playlists.md)
</dt> <dt>

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





