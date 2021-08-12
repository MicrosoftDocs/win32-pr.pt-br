---
title: Vantagens de usar HTMLView
description: Vantagens de usar HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Playlists de metadados de mídia, vantagens de HTMLView
- playlists, vantagens de HTMLView
- playlists de metadados, vantagens de HTMLView
- Windows Playlists de metadados de mídia, vantagens de HTMLView
- playlists, vantagens de HTMLView
- playlists de metadados, vantagens de HTMLView
- vantagens do HTMLView
- Windows Media Player,vantagens de HTMLView
- Windows Media Player,vantagens de HTMLView
- HTMLView,vantagens
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6019ec83466be9f4eca649d870422dce640fddc3ff011c46c6f918a1a09faa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583263"
---
# <a name="advantages-of-using-htmlview"></a>Vantagens de usar HTMLView

O recurso HTMLView facilita a criação de uma experiência de usuário integrada baseada na Web que reproduz conteúdo de mídia digital usando a aparência familiar da Web. Quando você combina conteúdo baseado na Web com conteúdo de mídia digital na interface do usuário do Windows Media Player, o resultado pode ter um impacto maior no usuário do que quando os elementos são exibidos separadamente. O conteúdo da mídia digital é aprimorado por informações relacionadas interessantes, enquanto a página da Web pode fornecer links para conteúdo semelhante, criando novas oportunidades de negócios.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView fornece uma melhor experiência do usuário

Os usuários querem e gostam de acessar as informações que podem ser oferecidas com conteúdo de mídia digital, mas não querem lidar com uma série aparentemente infinita de anúncios pop-up. Usar janelas do navegador pop-up para exibir anúncios na Web tornou-se tão comum que agora há software que impede que essas janelas se abrem. Esse software pode ter o efeito colateral indesejado de impedir a exibição de páginas da Web legítimas, às vezes suprimindo uma apresentação de mídia digital inteira.

Quando você usa o recurso HTMLView, os usuários não têm mais que lidar com janelas pop-up. Em vez de precisar abrir uma janela separada do navegador para fornecer informações adicionais  ao usuário, você pode exibir conteúdo personalizado baseado na Web no recurso Agora Reproduzindo da interface do usuário do Windows Media Player enquanto o Player reproduz o conteúdo de áudio ou vídeo que o usuário deseja. Os usuários podem controlar a reprodução usando os controles Windows Media Player dados. Como o conteúdo é reproduzindo no Player de modo completo, o software projetado para impedir anúncios pop-ups não impedirá que os usuários aproveitem o conteúdo.

## <a name="htmlview-content-is-easy-to-create"></a>O conteúdo htmlView é fácil de criar

Como o nome do recurso implica, você cria conteúdo baseado na Web exibido usando o recurso HTMLView usando linguagem HTML (HTML). Se você já criar conteúdo para a Web, isso significa que você não precisa aprender uma nova linguagem de programação para criar conteúdo rico facilmente com o recurso HTMLView. Se você já tiver páginas da Web com um controle Windows Media Player ActiveX inserido, poderá fazer com que essas páginas apareçam na interface do usuário do Player simplesmente apontando para essas páginas da Web de um metadado de mídia do Windows (arquivo .asx) usando um parâmetro especial.

Windows Media Player usa uma instância inserida do Microsoft Internet Explorer para exibir o conteúdo htmlView. Isso significa que você não precisa considerar diferentes navegadores da Internet, vários modelos de script ou linguagens de script diferentes ao criar suas páginas da Web. Mesmo que o usuário não use Internet Explorer como seu navegador padrão, sua página da Web ainda será exibida corretamente no Player.

É possível que um programa diferente de Windows Media Player possa se registrar como o programa padrão para abrir arquivos .asx. O Windows Media Player série 9 ou modelo de objeto posterior inclui um novo método, **openPlayer**, que permite especificar uma URL (Uniform Resource Locator) para o conteúdo que você deseja reproduzir. Quando você usa o **método openPlayer,** Windows Media Player sempre é aberto no modo completo para reproduzir o conteúdo especificado. Usando esse método, você pode garantir que o conteúdo htmlView seja exibido no Windows Media Player, em vez de algum outro aplicativo que tenha assumido a associação de tipo de arquivo .asx.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




