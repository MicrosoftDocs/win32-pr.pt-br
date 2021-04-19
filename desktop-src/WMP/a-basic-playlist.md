---
title: Uma lista de reprodução básica
description: Uma lista de reprodução básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Playlists do metarquivo do Windows Media, exemplo de playlist básica
- listas de reprodução, exemplo de playlist básica
- listas de reprodução de metarquivo, exemplo de playlist básica
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist básica
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314779"
---
# <a name="a-basic-playlist"></a>Uma lista de reprodução básica

O exemplo de playlist a seguir mostra um conjunto básico de elementos da lista de reprodução. Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivos para nomes de arquivos válidos que sejam acessíveis ao seu Windows Media Player.

**Exemplo de código**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



A tabela a seguir fornece detalhes sobre o uso de cada elemento no código de exemplo.



| Linha                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | O elemento [ASX](asx-element.md) identifica o cliente do (Windows Media Player) que esta é uma lista de reprodução do metarquivo do Windows Media. O atributo **version** especifica o número de versão dos elementos de metarquivo.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demonstração de playlist básica\</TITLE>                                                  | O elemento [title](title-element--metafile.md) identifica o título da lista de reprodução como um todo. O Windows Media Player exibe esses metadados como o título de exibição.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Inicia o elemento de [entrada](entry-element.md) . Um elemento de **entrada** é uma maneira de definir um clipe específico em uma lista de reprodução                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Uma entrada em uma playlist básica\</TITLE>                                         | Identifica o título do clipe da lista de reprodução. Ele é diferente do elemento **title** anterior porque este é aninhado dentro de um elemento **entry** . O Windows Media Player exibe esses metadados como o título do clipe.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | O elemento [autor](author-element.md) identifica o autor do clipe de mídia. O Windows Media Player exibe esses metadados como o **autor** do clipe.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Um comentário. Os [comentários](comments.md) são visíveis somente quando o código é exibido e estão no mesmo formato que os comentários **XML** .                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Ponteiro real para o arquivo de mídia. O elemento [ref](ref-element.md) identifica a linha como um ponteiro para conteúdo de mídia, enquanto o atributo **href** é a URL para o arquivo de mídia. Nesse caso, a URL usa o protocolo MMS e, portanto, aponta para um Windows Media Server. Os arquivos de mídia no servidor de mídia geralmente não são mantidos no mesmo local que os documentos HTML.<br/> Observe o uso do fechamento do tipo XML do elemento, "/>", em vez de " &lt; /ref &gt; ". Como esse elemento não tem elementos filho, ele se fecha.<br/> |
| \</ENTRY>                                                                                  | Especifica o final do elemento de **entrada** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Especifica o fim da lista de reprodução.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

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

 

 





