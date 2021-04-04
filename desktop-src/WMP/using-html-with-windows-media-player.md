---
title: Usando HTML com o Windows Media Player
description: Usando HTML com o Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Modelo de objeto do Windows Media Player, HTML
- modelo de objeto, HTML
- Controle ActiveX do Windows Media Player, HTML para modelo de objeto
- Controle ActiveX, HTML para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, HTML para modelo de objeto
- Windows Media Player Mobile, HTML para modelo de objeto
- HTML com o Windows Media Player
- Inserção de página da Web, HTML
- inserindo, páginas da Web
- comandos de script
- Inversão de URL
- streaming de mídia avançada
- suporte a navegador
- exibindo páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822691"
---
# <a name="using-html-with-windows-media-player"></a>Usando HTML com o Windows Media Player

## <a name="overview"></a>Visão geral

O uso de HTML com o Windows Media Player é uma excelente maneira de combinar áudio e vídeo com texto e gráficos. Você pode inserir o controle do Windows Media Player em uma página da Web quando desejar complementar seu conteúdo estático ou criar aplicativos da Internet com mídia digital. Quando você deseja complementar sua mídia digital com HTML, por outro lado, você pode exibir páginas da Web no modo completo do Player referenciando-as nas listas de reprodução do metarquivo do Windows Media.

Se você escrever programas personalizados que incorporam o controle do Windows Media Player no modo remoto, também poderá controlar as páginas da Web exibidas nos vários painéis do modo completo do Player quando os usuários desencaixam o controle. Isso permite preservar a continuidade entre os Estados encaixados e desencaixados.

## <a name="web-embedding"></a>Inserção na Web

Você pode usar o controle do Windows Media Player como parte de uma página da Web criada por você. Consulte [inserindo o controle do Windows Media Player em uma página da Web](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Comandos de script e inversão de URL

Comandos de script são pares de texto/valor que você pode inserir em seus arquivos de mídia digital ou fluxos. Você pode usar comandos de script personalizados exclusivamente para disparar código de script, enquanto permite que o Windows Media Player manipule outros comandos de script automaticamente.

Quando você tem várias páginas da Web que acompanham uma apresentação de mídia digital, os comandos de script de URL podem alterar automaticamente a página em um quadro enquanto o controle do Windows Media Player continua a reproduzir mídia digital em outro quadro. Isso é chamado de inversão de URL e é uma maneira excelente de criar uma apresentação de slides multimídia. Outros comandos de script manipulados automaticamente permitem alternar a reprodução para um arquivo de mídia ou fluxo diferente, exibir texto de legenda ou disparar eventos como inserções de anúncios definidas em uma lista de reprodução do metarquivo do Windows Media.

Para obter mais informações sobre a inversão de URL, consulte [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Streaming de mídia avançada

A inversão de URL funciona melhor com páginas simples que são carregadas rapidamente. Com páginas mais complexas, vários componentes são transferidos individualmente, dificultando a sincronização da exibição de página com mídia digital. Para permitir apresentações de mídia sofisticadas complexas, as páginas da Web podem ser adicionadas a um fluxo de mídia e entregues ao Player da mesma maneira que áudio e vídeo. Isso permite que você sincronize os componentes da sua apresentação com muito mais facilidade, especialmente em conexões de baixa velocidade.

Para obter mais informações sobre streaming de mídia avançada, consulte [criando Web-Based apresentações](creating-web-based-presentations.md).

## <a name="browser-support"></a>Suporte do navegador

Você pode inserir o controle do Windows Media Player no Microsoft Internet Explorer, no Firefox e no Netscape Navigator, embora o processo seja um pouco diferente para cada um. Você também pode criar páginas da Web projetadas para funcionar com todos os três navegadores.

Com o Internet Explorer e o Firefox, você insere o controle usando o elemento de objeto HTML. O navegador requer uma abordagem diferente, no entanto, porque ele não oferece suporte diretamente a controles ActiveX. Com o navegador, você usa o elemento APPLET para inserir um miniaplicativo Java especial na página. Este applet manipula a comunicação com o controle ActiveX do Player.

Para obter mais informações sobre o suporte do Firefox, consulte [usando o controle do Windows Media Player com o Firefox](using-the-windows-media-player-control-with-firefox.md).

Para obter mais informações sobre o suporte ao Netscape Navigator, consulte [usando o Windows Media Player com o Netscape 7,1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Exibindo páginas da Web no modo completo do Player

Você pode estender a funcionalidade do Windows Media Player ou fornecer uma exibição personalizada das informações que acompanham a mídia digital exibindo páginas da Web no modo completo do Player. Esse é o recurso HTMLView de metaarquivos do Windows Media. Os metaarquivos oferecem um grande controle sobre o conteúdo da lista de reprodução, permitindo que você faça a transição diretamente entre os clipes, insira anúncios e exiba imagens ainda no Windows Media Player. Para exibir as páginas da Web no modo completo do Player, use o elemento PARAM para adicionar referências de URL às suas entradas de playlist ou a listas de reprodução inteiras.

Para obter mais informações sobre o uso de páginas da Web em metaarquivos, consulte [exibindo páginas da Web no Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




