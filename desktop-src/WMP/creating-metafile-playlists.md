---
title: Criando listas de reprodução de metarquivo
description: Criando listas de reprodução de metarquivo
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Playlists do metarquivo do Windows Media, criando
- listas de reprodução, criando
- listas de reprodução de metarquivo, criando
- Criando listas de reprodução do metarquivo do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160165"
---
# <a name="creating-metafile-playlists"></a>Criando listas de reprodução de metarquivo

Você pode criar uma lista de reprodução usando qualquer editor de texto, como o bloco de notas da Microsoft. Abra seu editor de texto. Digite as entradas de script que você deseja implementar. Depois de terminar de digitar no bloco de notas, salve o arquivo com um nome de arquivo e uma extensão de nome de arquivo apropriados. Para obter mais informações sobre extensões, consulte [diretrizes de extensão de metarquivo](metafile-extension-guidelines.md). Normalmente, o nome do arquivo é o nome do arquivo de mídia do Windows ou fluxo seguido por uma extensão de. Wax,. wvx ou. asx. Por exemplo, se o conteúdo de mídia for um arquivo de áudio do Windows Media que tem uma extensão. WMA, use a extensão. Wax ao nomear a lista de reprodução. As listas de reprodução não devem incluir códigos de formatação de um processador de texto, como o Microsoft Word. Para ter certeza de que nenhum código de formatação está incluído na lista de reprodução, salve o arquivo como um arquivo de texto sem formatação ou ASCII.

> [!Note]  
> Elementos e atributos não diferenciam maiúsculas de minúsculas. O texto usado na lista de reprodução para definir um elemento ou atributo pode ser maiúsculo ou minúsculo, ou uma mistura de ambos.

 

Se um elemento não tiver elementos filho (aqueles que modificam ou estiverem contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura, logo antes de ' > ', no lugar de uma marca de fechamento. Os elementos filho de um elemento devem aparecer entre a marca de abertura e de fechamento para esse elemento; caso contrário, eles não são elementos filho para esse elemento e são ignorados ou causam um erro na sintaxe da lista de reprodução.

Os primeiros quatro caracteres de uma lista de reprodução devem ser " &lt; ASX". O elemento **ASX** é usado em todas as listas de reprodução se sua extensão é. Wax,. wvx ou. asx. Deve haver apenas um elemento **ASX** por playlist. Esse elemento identifica o arquivo como uma lista de reprodução do metarquivo do Windows Media. Ele não especifica o tipo de lista de reprodução.

O elemento **ASX** tem três atributos possíveis:

**VERSION**

O atributo **version** é necessário e deve seguir imediatamente após o elemento **ASX** , por exemplo "<ASX Version =" 3,0 " &gt; ". O número da versão atual é 3,0. O Windows Media Player dá suporte a todas as versões anteriores. Os valores aceitáveis para o atributo **version** incluem 3,0 e 3 (sem ponto decimal).

**PREVIEWMODE**

O atributo **PREviewmode** é opcional. Ele fornece outro mecanismo para especificar por quanto tempo renderizar um clipe. Se o valor do atributo **PREviewmode** for sim, o Windows Media Player processará cada clipe pela duração especificada pelo elemento **PREVIEWDURATION**. Cada clipe pode ter um **PREVIEWDURATION** especificado.

**BANNERBAR**

O atributo opcional **BANNERBAR** define se o controle do Windows Media Player reserva espaço para um gráfico de faixa. (Use o elemento **banner** para especificar o gráfico a ser exibido.) Se o valor de **BANNERBAR** for corrigido, o Windows Media Player reserva espaço em faixa para a apresentação e para cada clipe, independentemente de a lista de reprodução do metarquivo especificar uma faixa para a exibição ou o clipe. Isso manterá o tamanho da janela do Windows Media Player o mesmo (exceto quando o tamanho do vídeo for alterado), independentemente da ausência ou presença de um gráfico de faixa. Se a exibição ou o clipe não tiver uma faixa associada a ele, o espaço reservado para um será preto. Se o valor do atributo **BANNERBAR** for auto, o Windows Media Player reserva espaço para a faixa somente quando a apresentação ou o clipe inclui um.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Para obter mais informações sobre os três atributos do elemento **ASX** , consulte a entrada de referência para o [elemento ASX](asx-element.md).

Um elemento **ASX** contém elementos filho de **entrada** que definem informações sobre os arquivos de mídia a serem acessados. Cada elemento de **entrada** deve conter um elemento **ref** que especifica o caminho para o arquivo de mídia a ser transmitido. Deve haver pelo menos um elemento de **entrada** ou **ENTRYREF** dentro de um elemento **ASX** .

Outros elementos definidos no escopo do elemento **ASX** , como **título** e **autor**, são associados aos metadados exibidos pelo Windows Media Player.

As listas de reprodução mais simples são criadas adicionando-se vários elementos de **entrada** com um único elemento **ref** a um metarquivo. Cada elemento de **entrada** em uma lista de reprodução de metarquivo é renderizado na ordem em que aparece no arquivo, como se o usuário tivesse aberto manualmente cada clipe.

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



Certifique-se de que a lista de reprodução está funcionando clicando duas vezes nela no Windows Explorer. O Windows Media Player deve abrir e iniciar o streaming do conteúdo de mídia. Depois de confirmar que a lista de reprodução funciona, salve-a em seu servidor Web junto com as páginas da Webe vincule-o por meio de um elemento **href** ou incorpore-o em uma página da Web usando o elemento de **objeto** do Windows Media Player.

As seções a seguir contêm mais informações:

-   [Aninhando metaarquivos](nesting-metafiles.md)
-   [Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Exemplos de playlist**](example-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




