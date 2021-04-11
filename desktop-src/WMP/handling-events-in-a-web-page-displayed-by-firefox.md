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
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="85d1e-128">Manipulando eventos em uma página da Web exibida pelo Firefox</span><span class="sxs-lookup"><span data-stu-id="85d1e-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="85d1e-129">Ao inserir o controle do Windows Media Player em uma página da Web, você pode escrever um script que manipule eventos.</span><span class="sxs-lookup"><span data-stu-id="85d1e-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="85d1e-130">Para obter uma lista de eventos gerados pelo controle de jogador, consulte [objeto Player](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="85d1e-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="85d1e-131">Se o tipo MIME associado a um controle player incorporado for application/x-MS-WMP, você poderá escrever manipuladores de eventos que tenham o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="85d1e-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="85d1e-132">em que *EventName* é o nome de um evento do Windows Media Player, e *params* é uma lista dos parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="85d1e-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="85d1e-133">Por exemplo, o código a seguir tem um manipulador para o evento [PlayStateChange](player-player-playstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="85d1e-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="85d1e-134">Se você tiver várias instâncias do controle Player em uma página da Web e se usar o formato mostrado no exemplo anterior, cada manipulador de eventos será vinculado a uma instância específica do controle Player.</span><span class="sxs-lookup"><span data-stu-id="85d1e-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="85d1e-135">No exemplo anterior, o manipulador de eventos é chamado somente quando o estado de reprodução é alterado para o controle que tem a ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="85d1e-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="85d1e-136">Se o tipo MIME associado a um controle player incorporado não for application/x-MS-WMP, você poderá escrever manipuladores de eventos que tenham o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="85d1e-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="85d1e-137">em que *EventName* é o nome de um evento do Windows Media Player, e *params* é uma lista dos parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="85d1e-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="85d1e-138">Por exemplo, o código a seguir tem um manipulador para o evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="85d1e-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


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



<span data-ttu-id="85d1e-139">Se você tiver várias instâncias do controle Player em uma página da Web e se usar o formato mostrado no exemplo anterior, cada manipulador de eventos será vinculado a todas as instâncias do controle Player e o manipulador de eventos será chamado quando o estado de reprodução for alterado para qualquer controle de Player na página.</span><span class="sxs-lookup"><span data-stu-id="85d1e-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="85d1e-140">Se o tipo MIME não for application/x-MS-WMP, o evento **DoubleClick** será enviado como OnDSDblClickEvt (não OnDSDoubleClickEvt) para compatibilidade com a versão 6,4 do controle Player.</span><span class="sxs-lookup"><span data-stu-id="85d1e-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="85d1e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85d1e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85d1e-142">**Usando o controle do Windows Media Player com o Firefox**</span><span class="sxs-lookup"><span data-stu-id="85d1e-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




