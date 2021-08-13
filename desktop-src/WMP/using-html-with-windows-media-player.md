---
title: Usando HTML com Windows Media Player
description: Usando HTML com Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player,HTML
- Windows Media Player modelo de objeto,HTML
- modelo de objeto,HTML
- Windows Media Player ActiveX controle,HTML para o modelo de objeto
- ActiveX controle,HTML para o modelo de objeto
- Windows Media Player Controle ActiveX dispositivo móvel,HTML para o modelo de objeto
- Windows Media Player Mobile,HTML para o modelo de objeto
- HTML com Windows Media Player
- Incorporação de página da Web,HTML
- incorporação, páginas da Web
- comandos de script
- Invertia de URL
- streaming de mídia rica
- suporte ao navegador
- exibindo páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72185dec8ae9a2119d8c3218478e7ebb5a2df4d7740b25c9f4ecc016aa392e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465916"
---
# <a name="using-html-with-windows-media-player"></a>Usando HTML com Windows Media Player

## <a name="overview"></a>Visão geral

Usar HTML com Windows Media Player é uma excelente maneira de combinar áudio e vídeo com texto e elementos gráficos. Você pode inserir o controle Windows Media Player em uma página da Web quando quiser complementar seu conteúdo estático ou criar aplicativos Web com mídia digital. Quando quiser complementar sua mídia digital com HTML, por outro lado, você poderá exibir páginas da Web no modo completo do Player referenciando-as em playlists de metadados de mídia Windows Mídia.

Se você escrever programas personalizados que incorporam o controle Windows Media Player no modo remoto, também poderá controlar as páginas da Web exibidas nos vários painéis do modo completo do Player quando os usuários desencaixam o controle. Isso permite preservar a continuidade entre os estados encaixados e desencaixados.

## <a name="web-embedding"></a>Incorporação da Web

Você pode usar o Windows Media Player como parte de uma página da Web que você cria. Consulte [Incorporação do controle Windows Media Player em uma página da Web.](embedding-the-windows-media-player-control-in-a-web-page.md)

## <a name="script-commands-and-url-flipping"></a>Comandos de script e invertia de URL

Comandos de script são pares de texto/valor que você pode inserir em seus arquivos de mídia digital ou fluxos. Você pode usar comandos de script personalizados exclusivamente para disparar o código de script, enquanto permite Windows Media Player manipular outros comandos de script automaticamente.

Quando você tem várias páginas da Web que acompanham uma apresentação de mídia digital, os comandos de script de URL podem alterar automaticamente a página em um quadro, enquanto o controle Windows Media Player continua a reprodução de mídia digital em outro quadro. Isso é chamado de inverta de URL e é uma excelente maneira de criar uma apresentação de slides multimídia. Outros comandos de script manipulados automaticamente permitem que você alternar a reprodução para um arquivo de mídia ou fluxo diferente, exibir texto de legenda ou disparar eventos, como inserções de ad definidas em uma playlist de metadados Windows Mídia.

Para obter mais informações sobre a invertia de URL, consulte [Criando Web-Based apresentações](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Rich Media Streaming

A invertia de URL funciona melhor com páginas simples que são carregadas rapidamente. Com páginas mais complexas, vários componentes são transferidos individualmente, dificultando a sincronização da exibição da página com a mídia digital. Para permitir apresentações de mídia complexas, as páginas da Web podem ser adicionadas a um fluxo de mídia e entregues ao Player da mesma maneira que áudio e vídeo. Isso permite sincronizar os componentes de sua apresentação muito mais facilmente, especialmente em conexões de baixa velocidade.

Para obter mais informações sobre streaming de mídias rich, consulte [Criando Web-Based apresentações](creating-web-based-presentations.md).

## <a name="browser-support"></a>Suporte do navegador

Você pode inserir o controle Windows Media Player no Microsoft Internet Explorer, Firefox e Netscape Navigator, embora o processo seja ligeiramente diferente para cada um. Você também pode criar páginas da Web projetadas para funcionar com todos os três navegadores.

Com Internet Explorer e Firefox, você pode inserir o controle usando o elemento HTML OBJECT. No entanto, o navegador requer uma abordagem diferente, pois não dá suporte diretamente a ActiveX controles. Com o Navegador, você usa o elemento APPLET para inserir um applet Java especial na página. Esse applet lida com a comunicação com o controle player ActiveX controle.

Para obter mais informações sobre o suporte ao Firefox, [consulte Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).

Para obter mais informações sobre o suporte ao Netscape Navigator, consulte [Usando Windows Media Player com o Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Exibindo páginas da Web no modo completo do player

Você pode estender a funcionalidade do Windows Media Player ou fornecer uma exibição personalizada das informações que acompanham sua mídia digital exibindo páginas da Web no modo completo do Player. Esse é o recurso HTMLView dos metadados Windows Mídia. Os metadados dão um ótimo controle sobre o conteúdo da playlist, permitindo a transição direta entre clipes, inserir anúncios e exibir imagens ainda no Windows Media Player. Para exibir páginas da Web no modo completo do Player, use o elemento PARAM para adicionar referências de URL às suas entradas de playlist ou a playlists inteiras.

Para obter mais informações sobre como usar páginas da Web em metadados, consulte [Exibindo páginas da Web no Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> </dl>

 

 




