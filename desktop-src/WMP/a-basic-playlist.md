---
title: Uma Playlist Básica
description: Uma Playlist Básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Windows Playlists de metarquivo de mídia, exemplos de playlist
- listas de reprodução, exemplos de playlist
- listas de reprodução de metarquivo, exemplos de playlist
- Windows Playlists de metarquivo de mídia, playlists de exemplo
- listas de reprodução, exemplos de listas de reprodução
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Windows Playlists de metarquivo de mídia, listas de reprodução de exemplo
- listas de reprodução, listas de reprodução de exemplo
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Windows Playlists de metarquivo de mídia, exemplo de código
- listas de reprodução, exemplo de código
- listas de reprodução de metarquivo, exemplo de código
- Windows Playlists de metarquivo de mídia, exemplo de playlist básica
- listas de reprodução, exemplo de playlist básica
- listas de reprodução de metarquivo, exemplo de playlist básica
- exemplos de Windows Media Player, playlist
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
ms.openlocfilehash: c8284acfe86cb204293902c0fb8664e74b12f3d2cc176d762f1aff079faac0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004576"
---
# <a name="a-basic-playlist"></a>Uma Playlist Básica

O exemplo de playlist a seguir mostra um conjunto básico de elementos da lista de reprodução. Ao escrever seu próprio código, você precisará alterar todas as URLs e nomes de arquivo para nomes de arquivo válidos que sejam acessíveis para seu Windows Media Player.

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
| \<ASX version = "3.0">                                                                     | o elemento [ASX](asx-element.md) identifica para o cliente (Windows Media Player) que esta é uma lista de reprodução de metarquivo de mídia Windows. O atributo **version** especifica o número de versão dos elementos de metarquivo.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demonstração de playlist básica\</TITLE>                                                  | O elemento [title](title-element--metafile.md) identifica o título da lista de reprodução como um todo. Windows Media Player exibe esses metadados como o título de exibição.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Inicia o elemento de [entrada](entry-element.md) . Um elemento de **entrada** é uma maneira de definir um clipe específico em uma lista de reprodução                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Uma entrada em uma playlist básica\</TITLE>                                         | Identifica o título do clipe da lista de reprodução. Ele é diferente do elemento **title** anterior porque este é aninhado dentro de um elemento **entry** . Windows Media Player exibe esses metadados como o título do clipe.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | O elemento [autor](author-element.md) identifica o autor do clipe de mídia. Windows Media Player exibe esses metadados como o **autor** do clipe.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Um comentário. Os [comentários](comments.md) são visíveis somente quando o código é exibido e estão no mesmo formato que os comentários **XML** .                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Ponteiro real para o arquivo de mídia. O elemento [ref](ref-element.md) identifica a linha como um ponteiro para conteúdo de mídia, enquanto o atributo **href** é a URL para o arquivo de mídia. nesse caso, a URL usa o protocolo MMS, portanto, aponta para um Windows servidor de mídia. Os arquivos de mídia no servidor de mídia geralmente não são mantidos no mesmo local que os documentos HTML.<br/> Observe o uso do fechamento do tipo XML do elemento, "/>", em vez de " &lt; /ref &gt; ". Como esse elemento não tem elementos filho, ele se fecha.<br/> |
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

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metarquivo de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





