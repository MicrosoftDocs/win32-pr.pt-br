---
title: Manipulando eventos em uma página da Web exibida pelo Firefox
description: Manipulando eventos em uma página da Web exibida pelo Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Controle ActiveX do Windows Media Player, manipulação de eventos
- Controle ActiveX móvel do Windows Media Player, manipulação de eventos
- Controle ActiveX, manipulação de eventos
- inserindo, páginas da Web
- Incorporação de página da Web, manipulação de eventos
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX móvel do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Firefox, manipulação de eventos
- Incorporação de página da Web, Firefox
- eventos, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104292908"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Manipulando eventos em uma página da Web exibida pelo Firefox

Ao inserir o controle do Windows Media Player em uma página da Web, você pode escrever um script que manipule eventos. Para obter uma lista de eventos gerados pelo controle de jogador, consulte [objeto Player](player-object.md).

Se o tipo MIME associado a um controle player incorporado for application/x-MS-WMP, você poderá escrever manipuladores de eventos que tenham o seguinte formato:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



em que *EventName* é o nome de um evento do Windows Media Player, e *params* é uma lista dos parâmetros do evento. Por exemplo, o código a seguir tem um manipulador para o evento [PlayStateChange](player-player-playstatechange.md) .


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



em que *EventName* é o nome de um evento do Windows Media Player, e *params* é uma lista dos parâmetros do evento. Por exemplo, o código a seguir tem um manipulador para o evento **PlayStateChange** .


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

[**Usando o controle do Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




