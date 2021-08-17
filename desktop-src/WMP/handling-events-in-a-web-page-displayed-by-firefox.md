---
title: Manipulando eventos em uma página da Web exibida pelo Firefox
description: Manipulando eventos em uma página da Web exibida pelo Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player, inserindo controle de ActiveX
- modelo de objeto Windows Media Player, inserindo ActiveX controle
- modelo de objeto, inserindo ActiveX controle
- Windows Media Player controle de ActiveX móvel, incorporando
- Windows Media Player controle de ActiveX, inserindo
- Windows Media Player controle de ActiveX móvel, incorporando
- controle de ActiveX, inserindo
- controle de ActiveX de Windows Media Player, páginas da Web
- Windows Media Player controle de ActiveX móvel, páginas da Web
- controle de ActiveX, páginas da Web
- controle de ActiveX de Windows Media Player, manipulação de eventos
- Windows Media Player controle de ActiveX móvel, manipulação de eventos
- controle de ActiveX, manipulação de eventos
- inserindo, páginas da Web
- Incorporação de página da Web, manipulação de eventos
- Windows Media Player, Firefox
- modelo de objeto Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Móvel, Firefox
- controle de ActiveX de Windows Media Player, Firefox
- Windows Media Player controle de ActiveX móvel, Firefox
- controle de ActiveX, Firefox
- Firefox, manipulação de eventos
- Incorporação de página da Web, Firefox
- eventos, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748411"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Manipulando eventos em uma página da Web exibida pelo Firefox

ao inserir o controle de Windows Media Player em uma página da web, você pode escrever um script que manipule eventos. Para obter uma lista de eventos gerados pelo controle de jogador, consulte [objeto Player](player-object.md).

Se o tipo MIME associado a um controle player incorporado for application/x-MS-WMP, você poderá escrever manipuladores de eventos que tenham o seguinte formato:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



em que *eventname* é o nome de um evento Windows Media Player, e *params* é uma lista dos parâmetros do evento. Por exemplo, o código a seguir tem um manipulador para o evento [PlayStateChange](player-player-playstatechange.md) .


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Se você tiver várias instâncias do controle Player em uma página da Web e se usar o formato mostrado no exemplo anterior, cada manipulador de eventos será vinculado a uma instância específica do controle Player. No exemplo anterior, o manipulador de eventos é chamado somente quando o estado de reprodução é alterado para o controle que tem a ID = "Player".

Se o tipo MIME associado a um controle player incorporado não for application/x-MS-WMP, você poderá escrever manipuladores de eventos que tenham o seguinte formato:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



em que *eventname* é o nome de um evento Windows Media Player, e *params* é uma lista dos parâmetros do evento. Por exemplo, o código a seguir tem um manipulador para o evento **PlayStateChange** .


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



Se você tiver várias instâncias do controle Player em uma página da Web e se usar o formato mostrado no exemplo anterior, cada manipulador de eventos será vinculado a todas as instâncias do controle Player e o manipulador de eventos será chamado quando o estado de reprodução for alterado para qualquer controle de Player na página.

> [!Note]  
> Se o tipo MIME não for application/x-MS-WMP, o evento **DoubleClick** será enviado como OnDSDblClickEvt (não OnDSDoubleClickEvt) para compatibilidade com a versão 6,4 do controle Player.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**usando o controle de Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




