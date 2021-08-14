---
title: Criando playlists de metadados
description: Criando playlists de metadados
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Playlists de metadados de mídia, criando
- playlists, criando
- listas de reprodução de metadados, criando
- criando Windows playlists de metadados de mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 765d8ab507c2ce502f1cad021696b0fc2ecfd110da8dfa95ccc84a43a8987561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750463"
---
# <a name="creating-metafile-playlists"></a>Criando playlists de metadados

Você pode criar uma playlist usando qualquer editor de texto, como o Microsoft Bloco de notas. Abra seu editor de texto. Digite as entradas de script que você deseja implementar. Depois de terminar de digitar em Bloco de notas, salve o arquivo com um nome de arquivo e uma extensão de nome de arquivo apropriados. Para obter mais informações sobre extensões, consulte [Metafile Extension Guidelines](metafile-extension-guidelines.md). Normalmente, o nome do arquivo é o nome do arquivo Windows mídia ou fluxo seguido por uma extensão de .sempre, .wvx ou .asx. Por exemplo, se o conteúdo da mídia for um arquivo de áudio Windows Media que tenha uma extensão .wma, use a extensão .extension ao nomear a playlist. As playlists não devem incluir códigos de formatação de um processador de palavras, como Microsoft Word. Para ter certeza de que nenhum código de formatação está incluído na playlist, salve o arquivo como um arquivo ASCII ou texto sem formatação.

> [!Note]  
> Elementos e atributos não são sensíveis a minúsculas. O texto usado na playlist para definir um elemento ou atributo pode ser em letras maiúsculas ou minúsculas ou uma combinação de ambos.

 

Se um elemento não tiver nenhum elemento filho (aqueles que modificam ou estão contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura, logo antes do '>', no lugar de uma marca de fechamento. Elementos filho de um elemento devem aparecer entre a marca de abertura e fechamento para esse elemento; caso contrário, eles não são elementos filho para esse elemento e são ignorados ou causam um erro na sintaxe da playlist.

Os quatro primeiros caracteres de uma playlist devem ser " &lt; ASX". O **elemento ASX** é usado em todas as playlists, independentemente de sua extensão ser ., .wvx ou .asx. Deve haver apenas um elemento **ASX** por playlist. Esse elemento identifica o arquivo como uma lista de reprodução Windows metadados de mídia. Ele não especifica o tipo de playlist.

O **elemento ASX** tem três atributos possíveis:

**VERSION**

O **atributo VERSION** é necessário e deve seguir imediatamente após o elemento **ASX,** por exemplo " <versão ASX = "3.0" &gt; ". O número de versão atual é 3.0. Windows Media Player dá suporte a todas as versões anteriores. Os valores aceitáveis para **o atributo VERSION** incluem 3.0 e 3 (sem ponto decimal).

**PREVIEWMODE**

O **atributo PREVIEWMODE** é opcional. Ele fornece outro mecanismo para especificar por quanto tempo renderizar um clipe. Se o valor do atributo **PREVIEWMODE** for YES, Windows Media Player renderizará cada clipe durante a duração especificada pelo **elemento PREVIEWDURATION**. Cada clipe pode ter **uma PREVIEWDURATION** especificada.

**BANNERBAR**

O atributo **BANNERBAR** opcional define se o controle Windows Media Player reserva espaço para um gráfico de faixa. (Use o **elemento BANNER** para especificar o gráfico a ser exibido.) Se o valor de **BANNERBAR** for FIXED, Windows Media Player reserva espaço de faixa para o show e para cada clipe, independentemente de a playlist de metadados especificar uma faixa para o show ou clip. Isso manterá o tamanho da janela Windows Media Player igual (exceto quando o tamanho do vídeo mudar), independentemente da ausência ou da presença de um gráfico de faixa. Se o show ou clip não tiver uma faixa associada a ela, o espaço reservado para um será preto. Se o valor do atributo **BANNERBAR** for AUTO, Windows Media Player reserva espaço para a faixa somente quando o show ou clip incluir um.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Para obter mais informações sobre os três atributos do **elemento ASX,** consulte a entrada de referência para o [elemento ASX](asx-element.md).

Um **elemento ASX** contém **elementos filho ENTRY** que definem informações sobre os arquivos de mídia a serem acessados. Cada **elemento ENTRY** deve conter um elemento **REF** que especifica o caminho para o arquivo de mídia a ser transmitido. Deve haver pelo menos um **elemento ENTRY** ou **ENTRYREF** dentro de um **elemento ASX.**

Outros elementos definidos dentro do escopo do **elemento ASX,** como **TITLE** e **AUTHOR**, são associados aos metadados exibidos por Windows Media Player.

As listas de reprodução mais simples são criadas adicionando vários **elementos ENTRY** com um único **elemento REF** a um metarquivo. Cada **elemento ENTRY** em uma playlist de metadados é renderizado na ordem em que aparece no arquivo como se o usuário tivesse aberto manualmente cada clipe.

Código de exemplo


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



Certifique-se de que a playlist está funcionando clicando duas vezes nele no Windows Explorer. Windows Media Player deve abrir e iniciar o streaming do conteúdo de mídia. Depois de confirmar que a playlist funciona, salve-a no servidor Web juntamente com suas páginas da Web e vincule-a por meio de um elemento **HREF** ou insira-a em uma página da Web usando o elemento Windows Media Player **OBJECT.**

As seções a seguir contêm mais informações:

-   [Aninhando metadados](nesting-metafiles.md)
-   [Usando páginas ASP para criar dinamicamente Windows playlists de metadados de mídia](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Playlists de exemplo**](example-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




