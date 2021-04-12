---
title: Vantagens de usar o HTMLView
description: Vantagens de usar o HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Playlists do metarquivo do Windows Media, vantagens do HTMLView
- listas de reprodução, vantagens HTMLViews
- listas de reprodução de metarquivo, vantagens HTMLViews
- Playlists do metarquivo do Windows Media, vantagens do HTMLView
- listas de reprodução, vantagens do HTMLView
- listas de reprodução de metarquivo, vantagens de HTMLView
- vantagens do HTMLView
- Windows Media Player, vantagens do HTMLView
- Windows Media Player, vantagens do HTMLView
- HTMLView, vantagens
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364218"
---
# <a name="advantages-of-using-htmlview"></a>Vantagens de usar o HTMLView

O recurso HTMLView facilita a criação de uma experiência de usuário integrada baseada na Web que reproduz o conteúdo de mídia digital usando a aparência familiar da Web. Quando você combina conteúdo baseado na Web com conteúdo de mídia digital na interface do usuário do Windows Media Player (IU), o resultado pode ter um maior impacto sobre o usuário do que quando os elementos são exibidos separadamente. O conteúdo de mídia digital é aprimorado por informações relacionadas interessantes, enquanto a página da Web pode fornecer links para conteúdo semelhante, criando assim novas oportunidades de negócios.

## <a name="htmlview-provides-a-better-user-experience"></a>O HTMLView fornece uma experiência de usuário melhor

Os usuários desejam e gostam de acessar as informações que podem ser oferecidas com conteúdo de mídia digital, mas não querem lidar com uma série aparentemente interminável de anúncios pop-up. Usar janelas de navegador pop-up para exibir anúncios na Web se tornou tão comuns que agora há software que impede que essas janelas sejam abertas. Esse software pode ter o efeito colateral indesejado de impedir que páginas da Web legítimas sejam exibidas, às vezes suprimindo uma apresentação de mídia digital inteira.

Quando você usa o recurso HTMLView, os usuários não precisam mais lidar com janelas pop-up. Em vez de ter que abrir uma janela separada do navegador para fornecer informações adicionais ao usuário, você pode exibir conteúdo personalizado baseado na Web no recurso em **execução** da interface do usuário do Windows Media Player enquanto o player reproduz o conteúdo de áudio ou vídeo que o usuário deseja. Os usuários podem controlar a reprodução usando os controles do Windows Media Player. Como o conteúdo é reproduzido no player de modo completo, o software projetado para impedir anúncios pop-up não impede que os usuários aproveitem o conteúdo.

## <a name="htmlview-content-is-easy-to-create"></a>O conteúdo do HTMLView é fácil de criar

Como o nome do recurso implica, você cria o conteúdo baseado na Web exibido usando o recurso HTMLView usando o linguagem HTML (HTML). Se você já criar conteúdo para a Web, isso significa que você não precisa aprender uma nova linguagem de programação para criar conteúdo rico com facilidade com o recurso HTMLView. Se você já tiver páginas da Web com um controle ActiveX incorporado do Windows Media Player, poderá fazer com que essas páginas sejam exibidas na interface do usuário do Player simplesmente apontando para essas páginas da Web de um metarquivo do Windows Media (arquivo. asx) usando um parâmetro especial.

O Windows Media Player usa uma instância incorporada do Microsoft Internet Explorer para exibir o conteúdo do HTMLView. Isso significa que você não precisa considerar diferentes navegadores da Internet, vários modelos de script ou linguagens de script diferentes ao criar páginas da Web. Mesmo que o usuário não use o Internet Explorer como seu navegador padrão, sua página da Web ainda será exibida corretamente no Player.

É possível que um programa diferente do Windows Media Player possa se registrar como programa padrão para abrir arquivos. asx. O modelo de objeto do Windows Media Player 9 Series ou posterior inclui um novo método, **openPlayer**, que permite especificar um URL (localizador de recursos uniforme) para o conteúdo que você deseja reproduzir. Quando você usa o método **openPlayer** , o Windows Media Player sempre é aberto em modo completo para reproduzir o conteúdo especificado. Usando esse método, você pode garantir que o conteúdo do HTMLView seja exibido no Windows Media Player, em vez de algum outro aplicativo que tenha feito a associação de tipo de arquivo. asx.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




