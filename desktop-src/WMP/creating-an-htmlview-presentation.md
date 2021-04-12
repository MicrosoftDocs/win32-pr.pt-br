---
title: Criando uma apresentação do HTMLView
description: Criando uma apresentação do HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Playlists do metarquivo do Windows Media, apresentações do HTMLView
- listas de reprodução, apresentações HTMLViews
- listas de reprodução de metarquivo, apresentações HTMLView
- Playlists do metarquivo do Windows Media, criando apresentações do HTMLView
- listas de reprodução, criando apresentações do HTMLView
- listas de reprodução de metarquivo, criando apresentações do HTMLView
- Criando apresentações do HTMLView
- Windows Media Player, criando apresentações do HTMLView
- Windows Media Player, apresentações do HTMLView
- HTMLView, criando apresentações
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364155"
---
# <a name="creating-an-htmlview-presentation"></a>Criando uma apresentação do HTMLView

Para criar uma apresentação HTMLView básica, você precisa de pelo menos três elementos:

-   **Conteúdo de mídia digital.** Este é um ou mais arquivos de áudio ou vídeo que o Windows Media Player reproduz.
-   **Uma página da Web.** Esse é o conteúdo baseado na Web que é exibido no recurso de **agora em execução** da interface do usuário do Player.
-   **Um metarquivo do Windows Media.** Esta é a lista de reprodução de metarquivo que direciona o Windows Media Player para combinar o conteúdo de mídia digital com a página da Web.

Um arquivo. asx é um arquivo de texto que fornece informações sobre um fluxo de arquivos e sua apresentação. Com base na sintaxe de linguagem XML (XML), os arquivos. asx podem conter uma variedade de elementos, cada um identificado por uma marca com atributos associados. O elemento **param** fornece uma maneira de associar um parâmetro personalizado a uma entrada específica em uma lista de reprodução de metarquivo ou a todo o metarquivo. Um dos nomes de parâmetro predefinidos disponíveis para seu uso é "HTMLView". Esse é o parâmetro que faz com que a página da Web especificada pelo valor da URL seja exibida no Windows Media Player.

O código de exemplo a seguir mostra um arquivo. asx que combina um único arquivo de mídia digital com uma única página da Web:


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Quando o Windows Media Player abre o arquivo. ASX no exemplo anterior, ele reproduz o áudio do arquivo chamado content1. WMA e abre a página da Web chamada htmlview.htm no recurso de **agora em execução** do player de modo completo. O usuário pode pausar, buscar e parar o conteúdo de áudio usando os controles do Windows Media Player.

Você pode alterar facilmente a página da Web que é exibida para cada parte do conteúdo associando um elemento **param** a cada entrada, como mostra o exemplo de código a seguir:


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



No exemplo anterior, o Windows Media Player primeiro exibe a página da Web htmlview1.htm ao reproduzir o arquivo de áudio digital content1. WMA. Quando o Player abre a próxima entrada na lista de reprodução, content2. WMA, a página da Web exibida em **agora executa** alterações no htmlview2.htm. Dessa forma, você pode especificar qual página da Web o usuário vê para cada parte do conteúdo de mídia digital.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




