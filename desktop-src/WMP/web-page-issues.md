---
title: Problemas de página da Web
description: Problemas de página da Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Listas de reprodução do metarquivo do Windows Media, páginas da Web
- listas de reprodução, páginas da Web
- listas de reprodução de metarquivo, páginas da Web
- Playlists do metarquivo do Windows Media, personalizando HTMLView
- listas de reprodução, personalizando HTMLView
- listas de reprodução de metarquivo, personalizando HTMLView
- Playlists do metarquivo do Windows Media, personalização de HTMLView
- listas de reprodução, personalização de HTMLView
- listas de reprodução de metarquivo, personalização de HTMLView
- Personalizando o HTMLView
- Windows Media Player, páginas da Web
- Windows Media Player, personalizando o HTMLView
- Windows Media Player, HTMLView Personalizando
- HTMLView, personalizando
- HTMLView, páginas da Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636869"
---
# <a name="web-page-issues"></a>Problemas de página da Web

Há algumas coisas a serem consideradas quando você cria uma página da Web a ser exibida no recurso que **agora está executando** o Windows Media Player. Esta seção aborda alguns dos problemas que você pode encontrar ao criar seu conteúdo baseado na Web.

## <a name="customizing-htmlview"></a>Personalizando o HTMLView

Sua página da Web do HTMLView pode ser tão simples ou complexa quanto você desejar. Você pode incluir qualquer um dos elementos que geralmente usa em seu conteúdo baseado na Web. Se você inserir o controle do Windows Media Player, poderá exibir uma das interfaces de usuário fornecidas pelo controle, criar sua própria interface de usuário usando HTML e código de script, ou não fornecer nenhuma interface de usuários (o que significa que o usuário pode usar os controles de transporte do player de modo completo).

O tamanho recomendado para páginas da Web exibidas usando o recurso HTMLView é 575 x 345 pixels. O usuário, no entanto, tem a capacidade de redimensionar o Windows Media Player e escolher a resolução da tela. Se a página da Web HTMLView for maior do que o tamanho acomodado pelo recurso em **execução** , o Player exibirá as barras de rolagem horizontal e vertical que permitem que o usuário veja a página inteira. Você deve testar o conteúdo do HTMLView usando uma variedade de resoluções de tela e tamanhos de Player para determinar o melhor tamanho para sua página da Web.

O Windows Media Player não fornece um método que permite que você especifique um tamanho para o player de modo completo.

## <a name="web-page-navigation"></a>Navegação de página da Web

O Windows Media Player não fornece uma barra de ferramentas de navegação para páginas da Web exibidas no recurso **agora em execução** . Isso significa que você tem controle total sobre se os usuários podem navegar para fora da sua página da Web do HTMLView. Se você quiser permitir que os usuários naveguem para outras páginas da Web, você deve incluir elementos em seu código HTML para fornecer essa funcionalidade.

## <a name="retrieving-the-parent-window"></a>Recuperando a janela pai

Se o código de script existente usar **Window. pai** para recuperar o objeto de janela pai, esse código não funcionará na sua página da Web HtmlView. Quando você usa HTMLView, não há nenhum objeto de janela pai; Portanto, esse recurso de script não está disponível.

## <a name="about-the-embedded-browser"></a>Sobre o navegador incorporado

Como o Windows Media Player usa uma instância incorporada do Internet Explorer para exibir o conteúdo do HTMLView, as configurações do usuário e as políticas do Internet Explorer se aplicam a qualquer página da Web exibida no Player. Por exemplo, se o usuário tiver configurado o Internet Explorer para impedir que as páginas da Web baixem cookies para o computador, sua página da Web do HTMLView também será impedida de fazer isso.

As páginas da Web abertas usando o recurso HTMLView sempre são executadas na zona de segurança da **Internet** do Internet Explorer.

O controle de navegador da Web incorporado usa as mesmas regras para armazenar em cache as páginas a partir da versão autônoma do Internet Explorer. É uma boa ideia usar páginas de Active Server (ASP) ao criar seu conteúdo para garantir que o conteúdo seja entregue do seu servidor Web cada vez que o Windows Media Player acessar a página Web HTMLView. O uso de páginas ASP pode ser tão simples quanto renomear sua página da Web para usar uma extensão de nome de arquivo. ASP.

## <a name="about-local-web-content"></a>Sobre o conteúdo da Web local

O recurso HTMLView não permite que você abra páginas da Web armazenadas no computador do usuário.

## <a name="prompting-the-user"></a>Solicitando ao usuário

Você pode usar **Window. prompt** para solicitar informações ao usuário. No entanto, **Window. Alert** e **Window. Confirm** não estão disponíveis ao usar HtmlView.

## <a name="timing-issues"></a>Problemas de tempo

Você pode encontrar problemas de tempo ao usar um controle do Windows Media Player inserido em sua página da Web do HTMLView. No HTMLView, um controle player incorporado compartilha seu mecanismo de reprodução com o Windows Media Player autônomo. É possível que o Player autônomo possa abrir e começar a reproduzir a primeira entrada da playlist antes da página da Web (e, portanto, o controle do jogador) concluir o carregamento. Isso significa que, se você manipular os eventos **OpenStateChange** ou **PlayStateChange** , o código do script não receberá notificações de eventos para esses eventos até que o controle do jogador e seus objetos associados sejam carregados.

Você pode executar etapas em seu código para atrasar a reprodução até que o controle do Windows Media Player seja instanciado. Uma maneira de fazer isso é fazer com que a primeira entrada em sua lista de reprodução de metarquivo aponte para um arquivo de imagem e defina a duração do arquivo com um período de tempo que permita a carga do controle do jogador. O código de exemplo a seguir demonstra essa opção:


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Quando a lista de reprodução anterior é aberta, o Windows Media Player aguarda a primeira entrada da lista de reprodução por até um minuto, enquanto o Player carrega a página da Web HTMLView.

Em seguida, em sua página da Web do HTMLView, escreva o código de script para manipular o evento **OnLoad** para o elemento **Body** . Na função do manipulador de eventos, chame o método do Player **. Next** para iniciar a reprodução da segunda entrada na lista de reprodução.


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



Quando a página da Web no exemplo anterior termina de carregar, o Windows Media Player avança imediatamente para a segunda entrada na lista de reprodução. Isso substitui a duração especificada para o primeiro elemento na lista de reprodução, o que significa que o usuário não precisa aguardar um minuto completo antes de ver o conteúdo desejado; Ele só precisa aguardar a conclusão do carregamento da página da Web. Como o controle do jogador é completamente instanciado neste ponto, os eventos **OpenStateChange** e **PlayStateChange** podem ser tratados da maneira usual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 




